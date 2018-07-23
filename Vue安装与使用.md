### 开发环境搭建

#### `node.js`环境

在[官方下载地址](https://nodejs.org/en/download/)下载对应版本的安装包。

#### 安装淘宝`npm`镜像

`npm`为`node.js`使用的包依赖管理器，由于天朝的某些限制，依赖下载比较慢，可以选择使用[淘宝`npm`镜像](https://npm.taobao.org/)。

```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

#### vue命令行工具`vue-cli`介绍

##### 安装

```
npm install -g vue-cli
```

##### 创建一个新的vue项目脚手架

```
vue init <template-name> <project-name>
```

例如：

```
vue init webpack my-project
```

### 新建vue项目

#### 搭建并运行


```
$ npm install -g vue-cli
$ vue init webpack my-project
$ cd my-project
$ npm install
$ npm run dev
```

#### 项目目录结构介绍

```
.
├── build/                      # webpack 配置文件
│   └── ...
├── config/
│   ├── index.js                # 主要项目配置
│   └── ...
├── src/
│   ├── main.js                 # app 入口文件
│   ├── App.vue                 # 主要 app 组件
│   ├── components/             # ui 公共组件
│   │   └── ...
│   └── views/                  # 视图页面（自己添加的）
│   │   ├── ...                 # 视图文件夹
│   │   |   ├── js/
│   │   |   ├── css/
│   │   |   └── *.vue
│   │   ├── js/                 # 主要视图js
│   │   ├── css/                # 主要视图css
│   │   └── Main.vue            # 主要视图
│   └── assets/                 # 静态资源文件，包括字体、图片等 (processed by webpack)
│       └── ...
├── static/                     # 纯粹的静态资源文件 (directly copied)
├── test/
│   └── unit/                   # unit tests
│   │   ├── specs/              # test spec files
│   │   ├── eslintrc            # config file for eslint with extra settings only for unit tests
│   │   ├── index.js            # test build entry file
│   │   ├── jest.conf.js        # Config file when using Jest for unit tests
│   │   └── karma.conf.js       # test runner config file when using Karma for unit tests
│   │   ├── setup.js            # file that runs before Jest runs your unit tests
│   └── e2e/                    # e2e tests
│   │   ├── specs/              # test spec files
│   │   ├── custom-assertions/  # custom assertions for e2e tests
│   │   ├── runner.js           # test runner script
│   │   └── nightwatch.conf.js  # test runner config file
├── .babelrc                    # babel config
├── .editorconfig               # indentation, spaces/tabs and similar settings for your editor
├── .eslintrc.js                # eslint config
├── .eslintignore               # eslint ignore rules
├── .gitignore                  # sensible defaults for gitignore
├── .postcssrc.js               # postcss config
├── index.html                  # index.html 模板，编译打包的结果会注入到这里
├── package.json                # 构建脚本和依赖
└── README.md                   # Default README file
```

#### 构建命令介绍


- **npm run dev** ：启动一个本地`node.js`服务器，编译并运行该单页面应用。

- **npm run build**： 构建该单页面应用，构建结果保存在`./dist`目录下

- **npm run unit**： 运行单元测试

- **npm run e2e**： 运行端到端测试
