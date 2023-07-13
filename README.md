#### webpack - ModuleFederationPlugin

#### vite - vite-plugin-federation

#### webpack5 模块联邦（Module Federation）
Webpack 5 增加了一个新的功能 “模块联邦”，它允许多个 webpack 构建一起工作。 从运行时的角度来看，多个构建的模块将表现得像一个巨大的连接模块图。 从开发者的角度来看，模块可以从指定的远程构建中导入，并以最小的限制来使用。

多个独立的构建可以组成一个应用程序，这些独立的构建之间不应该存在依赖关系，因此可以单独开发和部署它们。这通常被称作微前端，但并不仅限于此。

Webpack5 模块联邦让 Webpack 达到了线上 Runtime 的效果，让代码直接在项目间利用 CDN 直接共享，不再需要本地安装 Npm 包、构建再发布了！ 我们知道 Webpack 可以通过 DLL 或者 Externals 做代码共享时 Common Chunk， 但不同应用和项目间这个任务就变得困难了，我们几乎无法在项目之间做到按需热插拔。

模块联邦可以将一个应用的包应用于另一个应用，同时具备整体应用一起打包的公共依赖抽取能力。
