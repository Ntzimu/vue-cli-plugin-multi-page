# VUE-CLI-MUILT-PAGE VUE多页开发构建插件 [![Downloads](https://img.shields.io/npm/dt/vue-cli-plugin-multi-page.svg)](https://www.npmjs.com/package/vue-cli-plugin-multi-page) [![Version](https://img.shields.io/npm/v/vue-cli-plugin-multi-page.svg)](https://www.npmjs.com/package/vue-cli-plugin-multi-page)
该插件为*vue-cli3*的*cli-plugin*插件，依赖*vue-cli3*运行环境(*系统需要安装**vue-cli 3.x**版本*)。<br>
## 前期准备
1. 创建项目: *vue create [project]* <br>
2. 进入项目根目录: *cd [project]* <br>
3. 安装此插件:  *vue add multi-page（或者 vue add vue-cli-plugin-multi-page）* <br>
## 常用命令
**新建开发模块使用** *npm run add module*<br>
**本地启动开发模块** *npm run serve module*<br>
**本地构建一个模块** *npm run build module*<br>
**本地构建多个模块** *npm run build m1 m2 m3...*<br>
**本地构建所有模块** *npm run build*<br>

## 多页结构
```
src  // 源码目录
│  ├─assets // 资源目录
│  │      logo.png
│  │
│  ├─components // 公用组件库
│  │      Hello.vue
│  │
│  └─modules // 多模块目录
│      ├─m1 // 模块1 （结构类似vue官方开发目录结构）
│      │  │  App.vue // 根路由页面
│      │  │  index.html // 启动文件
│      │  │  main.js // 根配置文件
│      │  │
│      │  ├─assets // 资源目录
│      │  │      logo.png
│      │  │
│      │  ├─components // 组件目录
│      │  │      Hello.vue
│      │  │
│      │  └─router // 路由目录
│      │          index.js
│      │
│      └─m2  // 模块1 （结构类似vue官方开发目录结构）
│      │  │  App.vue // 根路由页面
│      │  │  index.html // 启动文件
│      │  │  main.js // 根配置文件
│      │  │
│      │  ├─assets // 资源目录
│      │  │      logo.png
│      │  │
│      │  ├─components // 组件目录
│      │  │      Hello.vue
│      │  │
│      │  └─router // 路由目录
│      │          index.js
```
## 以下是该插件的愿景（最终完成目标）

## 1.在vue-cli3项目中使用该插件 ✅
在插件安装后会自动修改项目目录结构为该插件要求的运行环境（参见要求的项目结构）<br>
注意：目前还不支持自动删除文件操作 (**请手动删除src目录下*App.vue*和*main.js***) ❌
```
vue add vue-cli-plugin-multi-page 
```
***或者你可以可以这样做***<br>
1.列表内容先clone本项目到本地<br>
2.按该插件要求修改项目目录结构<br>
3.在项目package.json文件中引入本插件<br>
4.*在本地开发模式中使用npm run add modulue 命令可能会出现找不到vue-cli-plugin-multi-page路径的问题，先使用vue add vue-cli-plugin-multi-page 解决*
</span>
``` json
  # pageckage.json

  { ...

    ,"vuePlugins": {
      "service": ["../vue-cli-plugin-multi-page"]
    }
  }
```

## 2.新建模块 ✅
```npm
npm run add [module]
```
## 3.本地启动模块 ✅
```npm
npm run serve [module] 
```
## 4.本地启动所有模块 ❌
```npm
npm run serve
```
## 5.构建一个或者多个模块 ✅
```npm
npm run build [module] [m2] [...]
```
## 6.构建所有模块 ✅
```npm
npm run build
```
