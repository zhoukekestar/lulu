<p align="center">
  <img src="https://imgservices-1252317822.image.myqcloud.com/image/093020210104728/9999e481.svg" width="227" height="98">
</p>
<p align="center">追本溯源，穿越沉浮</p>
<p align="center">
    <img src="https://img.shields.io/npm/v/lu2.svg" height="20"> <img src="https://img.shields.io/apm/l/vim-mode.svg" height="20">
</p>

# LuLu UI

LuLu UI 是阅文集团荣誉出品的前端 UI 组件库。

形象气质如下图，更柔软，更亲近，同时简单灵活，对用户侧非常友好，非常适合<strong>面向外部用户的 PC 网站</strong>，或者需要轻量与敏捷的项目。

<img src="https://qidian.gtimg.com/lulu/theme/modern/css/common/images/temp/figure.png" width="122" height="137">

## 文档

* <a href="https://l-ui.com/">LuLu UI API 中文文档</a>（GitHub托管，访问有延迟）
* <a href="https://www.zhangxinxu.com/sp/lulu/mockup/">LuLu UI API 中文文档</a>（国内服务器托管，速度可以）

## 教程

* <a href="https://www.zhangxinxu.com/sp/lulu/guide/edge/">LuLu UI 中文教程</a>

## 上手简单

LuLu 整个项目就是提供一些 UI 组件的 JS 和 CSS，很纯粹的 JS 和 CSS，贴近原生，简单直白。

LuLu UI 支持直接引入 CSS 和 JS 文件地址，所有主题通用，例如下面的代码引用了全部的 UI 组件库：

```html
<link rel="stylesheet" href="https://qidian.gtimg.com/lulu/pure/css/common/ui.css">
```
```html
<script src="https://qidian.gtimg.com/lulu/pure/js/common/all.js"></script>
```

您也可以直接单独引入某一个组件，例如：

```html
<link rel="stylesheet" href="https://qidian.gtimg.com/lulu/pure/css/common/ui/Dialog.css">
```
```html
<script src="https://qidian.gtimg.com/lulu/pure/js/common/ui/Dialog.js"></script>
```

Edge 主题还支持浏览器原生的 import 引入，例如：

```html
<script type="module">
import Dialog from 'https://qidian.gtimg.com/lulu/edge/js/common/ui/Dialog.js';
</script>
```

LuLu UI 基于原生 HTML 特性构建，因此使用的时候 HTML 还是原来的 HTML，CSS 还是原来的 CSS，无需掌握流行概念，参照文档，复制复制，粘贴粘贴，效果就出来了。

由于 LuLu UI 中的代码基础，结构简单，没有炫技成分，也没有复杂技巧，因此非常适合新人的学习。

## 使用场景广泛

LuLu UI 既保留了传统插件即插即用的特性，也支持适合多人合作的模块化加载方式，因此适用场景更加广泛。

* 单人完成的某个简单运营活动页，需要个弹框提示功能，可以直接引入 LuLu UI 中的 Dialog.js，就可以使用了。
* 某网站看中了 LuLu UI 某一个组件，例如日期选择功能，想拿过来使用，`<script>` 引入日期选择JS，然后就可以使用了。
* 对于多人合作大型项目，可以基于 AMD/CMD 规范，或者 ES6 原生的 import/export 进行模块化加载与开发。
* 对于 Vue 或者 React 项目，想要使用某个组件，但又不希望引入一大堆东西，则 LuLu UI 非常合适，支持 Vue/React 单独引入（见下方使用示意）。

#### 在Vue/React中使用

安装：
```js
npm install lu2
```

在 Vue-CLI 环境中：
```html
<script>
import Dialog from 'lu2/theme/pure/js/common/ui/Dialog'
</script>
```
```html
<style src="lu2/theme/pure/css/common/ui/Dialog.css"></style>
```

React 框架中：

```js
import "lu2/theme/edge/css/common/ui/Button.css";
import "lu2/theme/edge/css/common/ui/Dialog.css";
import Dialog from "lu2/theme/edge/js/common/ui/Dialog.js";
```

## 成熟

LuLu UI 诞生于 2015 年，非 KPI 项目，服务于真实业务场景，会一直不断迭代，不要担心遇到问题会无人问津。

开源是件严肃的事情，LuLu UI 一直认为，如果组件还没有达到不动如山的境地，那就应该继续埋头打磨。这么多年过去了，LuLu UI 经过阅文集团对内对外近20个大中小型项目的实践与打磨，无论是交互细节还是代码本身细节，LuLu UI 现在都已经可以做到不显山露水了。

## 体验

LuLu UI 支持高清屏幕，支持辅助阅读设备无障碍访问，以及不少 UI 框架忽略的键盘无障碍访问。

借助扎实的前端基础知识，LuLu UI 有着很多创新的细节打磨，举个例子：如果用户是通过鼠标点击按钮打开的弹框，则弹框界面平平无奇；如果用户是通过 ENTER 回车键点击按钮打开的弹框，则弹框中的按钮默认会<code>outline</code>高亮！

<img src="https://qidian.qpic.cn/qidian_common/349573/851af9151027efc7e412e456f379263e/0" width="748" height="558">

这样的细节处理对于 C 端产品颇有价值。

## 快速了解项目目录结构

所有资源都在 <code>/theme/</code> 目录下，目前支持4个主题：

* Modern 主题<br>
  基于 jQuery，兼容 IE7+，针对 PC 网站。分 sass, css 和 js 3个目录，如果你不想要 sass，那这个文件夹就不用管。图片资源在 css 目录下。
* Peak 主题<br>
  基于 jQuery，兼容 IE8+，针对PC网站。分 sass, css 和 js 3个目录，如果你不想要 sass，那这个文件夹就不用管。图片资源在 css 目录下。
* Pure 主题<br>
  原生 JavaScript 编写，兼容 IE9+，PC，Mobile 网站通用。分 css 和 js 2个目录，没有图片资源目录，所有图像 CSS 内联。
* Edge 主题<br>
  原生 JavaScript 编写，ES6 module，兼容现代浏览器，PC，Mobile 网站通用，Vue、Preact、React全兼容，是面向未来的现代 Web 组件库。

组件分 ui 和 comp 两个目录，前者是 UI 组件，后者是基于 UI 组件整合的前端解决方案。

更具体信息可以参见：
* <a href="https://l-ui.com/pure/about.use.html">文档-使用与发布（Pure主题）</a>
* <a href="https://l-ui.com/edge/about.use.html">文档-使用与发布（Edge主题）</a>

文档在 gh-pages 分支。

另外，本 git 只展示了输出版本，原始 git 项目在公司内部，测试和开发目录并未对外，并不是说本项目没有测试用例。

## 项目成员

排名不分先后：nanaSun，ziven27，lennonover，wiia, popeyesailorman, 5ibinbin, littleLionGuoQing, peter006qi, HSDPA-wen, ShineaSYR, xiaoxiao78

## 其他说明

因为 IE7 大势已去，目前 modern 主题已停止维护。

组件均有测试，不过在内部项目中，没有对外。

LuLu UI 的设计理念、使用方式完全不同于常规 UI 组件库。

LuLu UI 没有版本概念，发包均已发包日期作为版号。

<hr>

MIT License
