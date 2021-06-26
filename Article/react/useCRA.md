## 使用CRA创建react项目

> 从这篇文章开始，我们重新来学习一下React的官网。本文从经典的Hello World示例未开始，给大家介绍下react应用的创建，通过本文的介绍，我们学会新建一个react应用。

### 概述

React其实就是一个JS文件库，本质上跟我们的jQuery这些JS库是一样的，所以大家在开始的时候不要有任何的心理负担，觉得它很难，其实它一点都不难。这篇文章我们先来新建第一个react应用。

### React使用方法

React使用方法有两种，第一种就跟jQuery一样，在我们的HTML页面中通过`<script>`标签引入；第二种是借助npm这个包管理工具，将它通过`npm install react`的方式安装到我们的项目中。

在我们这个系列的文章中我们采用第二种方式来给大家介绍，因为第一种方法虽然说是行得通的，但是目前我们前端开发基本都是清一色的SPA单页面应用，项目底层全部是采用webpack这些主流的打包工具来构建的，所以第一种方法在实际项目开发中用的不是很多。

### React应用创建

采用第二种方式来创建一个react的项目应用的话，是需要在项目中配置一些webpack的简单配置，还要配置babel这些转义工具什么的，特别麻烦。若果你对这个过程感兴趣的话，可以在我的博客分类【React进阶】中查看"如何从零创建一个react应用"这一篇文章，里面有详细的记录。我们在此处就不耽误时间来介绍这些东西，刚开始学习react的话这些东西大家可以先不用关注，把精力放在react上就行。

我们在这里创建react项目应用的时候直接使用react官方提供的一个脚手架工具，叫`create-react-app`。通过这个工具，我们可以使用一行命令就可以创建一个基础的、配置好的、可以直接拿来就用的react项目。这个工具使用的前提是你的电脑上已经安装了node环境。

我们新建一个文件夹之后通过在终端输入命令`npx create-react-app reactbasic`来创建第一个react应用。

### Hello World编写

react应用创建完成之后，在终端会提示我们通过命令"cd reactbasic"进入项目目录，然后通过命令"npm start"来启动项目。我们依次输入这两个命令来启动项目，如果你看到如下所示的面板，说明我们的react应用创建成功，它会自动打开我们的浏览器并且监听3000端口：

![react1](https://raw.githubusercontent.com/xuqwCloud/Blog/main/Images/react/react1.png)

有了一个基础的项目应用之后，我们接下来编写第一个react应用程序——Hello World。

我们先用代码编辑器打开新建的项目，然后删除掉src目录下除了index.js文件以外的所有文件，最后项目的文件目录及index.js文件里的代码如下：

![react2](https://raw.githubusercontent.com/xuqwCloud/Blog/main/Images/react/react2.png)

`index.js`文件代码：

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);
```

然后我们将下面的代码替换到`index.js`文件中保存后，查看页面，发现Hello World成功展示在了我们的浏览器页面中：

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(<span>Hello World</span>, document.getElementById('root'));
```

至此，我们的Hello World应用编写成功。到目前为止，你肯定有一大堆疑惑：明明是一份js后缀的文件，为啥里面可以写`<span>`标签？import导进来的React都没有使用，为啥最上面这一行删掉后会报错？我代码复制粘贴后按保存，浏览器页面都没有点击刷新按钮，页面怎么自动刷新了？这些项目里我就改了改`index.js`这一个文件，那其他文件是做什么的……

如果你有上述的问题，请保留你的疑问，接下来的文章中我们会一一解答。本文就到此结束了，这一篇文章其实大家只需要知道react的两种使用方式，并且学会使用`create-react-app`创建react应用即可。