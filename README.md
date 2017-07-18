# pea-app-specification
A new javascript app, between web and browser

# pea-app是什么

pea-app（以下简称PA）是介于页面js与浏览器扩展之间的新型应用，由HTML、CSS、JS组成。

你可以将你的PA打包成油猴脚本来使用，也可以在你的网站中静态引用一个PA，还可以打包成浏览器扩展来使用。而跨浏览器兼容、浏览器扩展与页面JS中的迁移，全部由PA官方工具来为你自动完成。

也就是说，你开发的PA，可以成为JS库、油猴脚本、浏览器扩展，让开发者与小白用户共同使用！

# PA模块组成

- 应用模块依赖管理
  - 依赖加载
    - 静态加载
    - 动态加载
  - 崩溃处理
    - 后续处理：版本切换/终止运行
    - 崩溃报告
      - 自动报告
      - 提示用户报告
- 运行生命周期管理
- 应用Add-on
  - 依赖管理：仅静态
  - 崩溃处理：仅报告
- 更新
  - 静态PA的更新：更简单，低频率
  - 动态PA的更新：更强大，热更新
- 用户配置管理

# PA分类

- TYPE_A：静态加载、更新，不支持Add-on
- TYPE_B：动态加载、更新，不支持Add-on
- TYPE_C：动态加载、更新，支持Add-on

# 官方提供

- pea-app：框架主程序
- pa-cli：脚手架工具，已向导方式快速搭建一个pea-app，并提供build功能
- pa-tpl-[TYPE\_X]：各种类型的pea-app的模板
- zoom-font：符合PA规范的TYPE_A类型的app
- Pxer：符合PA规范的TYPE_C类型的app

# PA文件结构

- pea.json - 必选，存放PA配置
- \_pa - 可选，pa框架代码。若项目不包含此目录，则必须静态引用pea.js
  - index.js 框架入口文件
- pea.js  - 可选，完整的PA框架代码

