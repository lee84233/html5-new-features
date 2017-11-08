# HTML5新特性

标签（空格分隔）： html

---
***相关链接：***
1. [HTML5 教程](https://www.w3cschool.cn/html5/)
2. [HTML5 编码规范](http://codeguide.bootcss.com/)
3. [HTML5 支持查询](https://caniuse.com/)
4. [HTML5 移动设备支持查询](http://mobilehtml5.org/)

---

***目录：***

HTML5新特性  
1. [HTML5简介](#1.HTML5简介)  
  1.1 什么是html5  
  1.2 html5新特点  
  1.3 html5兼容性  
    1.3.1 IE兼容模式  
2. HTML5的新特性HTML5的新特性  
  2.1 语义化  
    2.1.1 语义化意义  
    2.1.2 语义化标签  
  2.2 CSS3  
    2.2.1 转换、变形和过渡  
      2D新转换属性  
      2D转换方法  
      3D新转换属性  
      3D转换方法  
      过渡  
    2.2.2 动画  
    2.2.3 伸缩布局盒模型  
    2.2.4 CSS3 多媒体查询  
    2.2.5 伪类、伪元素  
    2.2.6 其他新特性  
  2.3 本地存储  
    2.3.1 永久本地存储：localStorage  
    2.3.2 会话级别的本地存储：sessionStorage  
    2.3.4 Web SQL Database  
    2.3.5 Indexeddb  
    2.3.6 离线缓存（Application Cache）  
  2.4 三维、图形及特效  
    2.4.1 Canvas  
    2.4.2 SVG  
    2.4.3 WebGL  
  2.5 网页多媒体  
    2.5.1 Video  
    2.5.2 Audio  
  2.6 设备访问、性能与集成  
    2.6.1 桌面通知 (Notifications)  
    2.6.2 Camera API  
    2.6.3 全屏(Fullscreen)API  
    2.6.4 WebSocket  
    2.6.5 Web Worker  
    2.6.6 更多属性  
3. 周边  
  3.1 当下流行的 js 框架  
  3.2 当下流程的UI框架  
  3.3 构建工具&自动化 相关  
4.写在后面，错误和不足之处欢迎指正:smile:  

---

# 1.HTML5简介

## 1.1 什么是html5
万维网的核心语言、标准通用标记语言下的一个应用超文本标记语言（HyperText Markup Language）的第五次重大修改。目标是取代1999年12月发布的HTML4.01标准。
2014年10月29日，万维网联盟宣布，经过接近8年的艰苦努力，该标准规范终于制定完成。

## 1.2 html5新特点
1. HTML5 是最新的 HTML 标准。
2. HTML5 是专门为承载丰富的 web 内容而设计的，并且无需额外插件（flash等）。
3. HTML5 拥有新的语义、图形以及多媒体元素。
4. HTML5 提供的新元素和新的 API 简化了 web 应用程序的搭建。
5. HTML5 是跨平台的，被设计为在不同类型的硬件（PC、平板、手机、电视机等等）之上运行。

## 1.3 html5兼容性
兼容IE9+、所有的现代浏览器。
>支持Html5的浏览器包括Firefox（火狐浏览器），IE9及其更高版本，Chrome（谷歌浏览器），Safari，Opera等；国内的傲游浏览器（Maxthon），以及基于IE或Chromium（Chrome的工程版或称实验版）所推出的360浏览器、搜狗浏览器、QQ浏览器、猎豹浏览器等国产浏览器同样具备支持HTML5的能力。

### 1.3.1 IE兼容模式
1. 让 IE 浏览器运行最新的渲染模式：`<meta http-equiv="X-UA-Compatible" content="IE=edge">`
2. 让部分国产浏览器默认采用高速模式渲染页面：（目前仅360浏览器支持）`<meta name="renderer" content="webkit">`
3. 引入 [Respond.js](https://github.com/scottjehl/Respond) 配合，实现对媒体查询（media query）的支持。
4. 引入 [html5shiv.js](https://github.com/aFarkas/html5shiv) 解决HTML5提出的新的元素不被IE6-8识别，这些新元素不能作为父节点包裹子元素，并且不能应用CSS样式。
```html
<!--[if lt IE 9]>
  <script type="text/javascript" src="你的js路径/Respond.js"></script>
  <script type="text/javascript" src="你的js路径/html5shiv.js"></script>
<![endif]-->
```

*相关链接:*
1. [W3C官方html5相关APIs](https://www.w3.org/TR/html5/)
2. [html5百度百科](https://baike.baidu.com/item/html5/4234903?fr=aladdin#reference-[1]-951383-wrap)

# 2. HTML5的新特性HTML5的新特性
1. 语义化
2. CSS3
3. 本地存储
4. 三维、图形及特效
5. 网页多媒体
6. 设备访问
7. 性能与集成

## 2.1 语义化
### 2.1.1 语义化意义
![语义化](http://lee.yiger.com.cn/assets/images/html5-img1.jpg)
1. 为了在没有CSS的情况下，页面也能尽可能好的呈现出内容结构、代码结构:为了裸奔时好看；
2. 用户体验：例如title、alt用于解释名词或解释图片信息、label标签的活用；
3. 有利于SEO：和搜索引擎建立良好沟通，有助于爬虫抓取更多的有效信息：爬虫依赖于标签来确定上下文和各个关键字的权重；
4. 便于团队开发和维护，语义化更具可读性，是下一步吧网页的重要动向，遵循W3C标准的团队都遵循这个标准，可以减少差异化。
5. 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以意义的方式来渲染网页；

### 2.1.2 语义化标签
```html
<!-- 常用的语义化标签 -->
<header>定义页眉</header>
<nav>定义导航</nav>
<section> 定义文档中的区段</section>
<article>定义文章</article>
<aside>定义文章的侧边栏</aside>
<figure>一组媒体对象以及文字</figure>
<figcaption>定义 figure 的标题</figcaption>
<hgroup>定义对网页标题的组合</hgroup>
<time>定义日期和时间</time>
<footer>定义页脚</footer>

<!-- 废弃的标签 -->
<acronym>、<applet>、<basefont>、<big>、<center>、<dir>、<font>、<frame>、 <s>、<isindex>、<noframes>、 <frameset> 、<strike>、<tt>、<u>和<xmp>
```
*相关链接:*
1. [HTML5新增的标签和属性归纳](http://blog.csdn.net/garvisjack/article/details/54754928)
2. [HTML5 标签列表](http://www.w3chtml.com/html5/tag/)

## 2.2 CSS3
### 2.2.1 转换、变形和过渡
#### 2D新转换属性
| 属性    | 描述   |
| :----   | :----- |
| transform     | 适用于2D或3D转换的元素 |
| transform-origin |   允许您更改转化元素位置   |

#### 2D转换方法
| 函数    | 描述   |
| :----   | :----- |
| matrix(n,n,n,n,n,n)	| 定义 2D 转换，使用六个值的矩阵。 |
| translate(x,y)	| 定义 2D 转换，沿着 X 和 Y 轴移动元素。 |
| translateX(n)	| 定义 2D 转换，沿着 X 轴移动元素。 |
| translateY(n)	| 定义 2D 转换，沿着 Y 轴移动元素。 |
| scale(x,y)	| 定义 2D 缩放转换，改变元素的宽度和高度。 |
| scaleX(n)	| 定义 2D 缩放转换，改变元素的宽度。 |
| scaleY(n)	| 定义 2D 缩放转换，改变元素的高度。 |
| rotate(angle)	| 定义 2D 旋转，在参数中规定角度。 |
| skew(x-angle,y-angle)	| 定义 2D 倾斜转换，沿着 X 和 Y 轴。 |
| skewX(angle)	| 定义 2D 倾斜转换，沿着 X 轴。 |
| skewY(angle)	| 定义 2D 倾斜转换，沿着 Y 轴。 |

#### 3D新转换属性
| 属性    | 描述   |
| :----   | :----- |
| transform | 向元素应用 2D 或 3D 转换。 |
| transform-origin | 允许你改变被转换元素的位置。 |
| transform-style | 规定被嵌套元素如何在 3D 空间中显示。 |
| perspective | 规定 3D 元素的透视效果。 |
| perspective-origin | 规定 3D 元素的底部位置。 |
| backface-visibility | 定义元素在不面对屏幕时是否可见。 |

#### 3D转换方法
| 函数    | 描述   |
| :----   | :----- |
| matrix3d(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n) | 定义 3D 转换，使用 16 个值的 4x4 矩阵。 |
| translate3d(x,y,z) | 定义 3D 转化。 |
| translateX(x) | 定义 3D 转化，仅使用用于 X 轴的值。 |
| translateY(y) | 定义 3D 转化，仅使用用于 Y 轴的值。 |
| translateZ(z) | 定义 3D 转化，仅使用用于 Z 轴的值。 |
| scale3d(x,y,z) | 定义 3D 缩放转换。 |
| scaleX(x) | 定义 3D 缩放转换，通过给定一个 X 轴的值。 |
| scaleY(y) | 定义 3D 缩放转换，通过给定一个 Y 轴的值。 |
| scaleZ(z) | 定义 3D 缩放转换，通过给定一个 Z 轴的值。 |
| rotate3d(x,y,z,angle) | 定义 3D 旋转。 |
| rotateX(angle) | 定义沿 X 轴的 3D 旋转。 |
| rotateY(angle) | 定义沿 Y 轴的 3D 旋转。 |
| rotateZ(angle) | 定义沿 Z 轴的 3D 旋转。 |
| perspective(n) | 定义 3D 转换元素的透视视图 |

#### 过渡
| 属性    | 描述   |
| :----   | :----- |
| transition | 简写属性，用于在一个属性中设置四个过渡属性。 |
| transition-property | 规定应用过渡的 CSS 属性的名称。 |
| transition-duration | 定义过渡效果花费的时间。默认是 0。 |
| transition-timing-function | 规定过渡效果的时间曲线。默认是 "ease"。 |
| transition-delay | 规定过渡效果何时开始。默认是 0。 |

### 2.2.2 动画
要创建CSS3动画，你需要了解@keyframes规则。@keyframes规则是创建动画。 @keyframes规则内指定一个CSS样式和动画将逐步从目前的样式更改为新的样式。

| 属性    | 描述   |
| :----   | :----- |
| @keyframes | 规定动画。 |
| animation | 所有动画属性的简写属性，除了 animation-play-state 属性。 |
| animation-name | 规定 @keyframes 动画的名称。 |
| animation-duration | 规定动画完成一个周期所花费的秒或毫秒。默认是 0。 |
| animation-timing-function | 规定动画的速度曲线。默认是 "ease"。 |
| animation-delay | 规定动画何时开始。默认是 0。 |
| animation-iteration-count | 规定动画被播放的次数。默认是 1。可取值：n/infinite |
| animation-direction | 规定动画是否在下一周期逆向地播放。默认是 "normal"。可取值：normal/alternate |
| animation-play-state | 规定动画是否正在运行或暂停。默认是 "running"。 |

```css
/* 定义动画 */
.animated{
  animation-name: myfirst;
  animation-duration:5s;
  animation-timing-function: linear;
  animation-delay:2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-play-state: running;
}

/* 动画规则 */
@keyframes myfirst{
  0%  {background: red;}
  25% {background: yellow;}
  50% {background: blue;}
  75% {background: black;}
  100%{background: green;}
}
```

### 2.2.3 伸缩布局盒模型
| 属性    | 描述   |
| :----   | :----- |
| display | 指定 HTML 元素盒子类型。 |
| flex-direction | 指定了弹性容器中子元素的排列方式。 |
| justify-content | 设置弹性盒子元素在主轴（横轴）方向上的对齐方式。 |
| align-items | 设置弹性盒子元素在侧轴（纵轴）方向上的对齐方式。 |
| flex-wrap | 设置弹性盒子的子元素超出父容器时是否换行。 |
| align-content | 修改 flex-wrap 属性的行为，类似 align-items, 但不是设置子元素对齐，而是设置行对齐 |
| flex-flow | flex-direction 和 flex-wrap 的简写 |
| order | 设置弹性盒子的子元素排列顺序。 |
| align-self | 在弹性子元素上使用。覆盖容器的 align-items 属性。 |
| flex | 设置弹性盒子的子元素如何分配空间。 |

*相关链接：*
1. [Flex 布局教程](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)

### 2.2.4 CSS3 多媒体查询
```html
<!-- 设置meta标签 -->
<meta name="viewport" content="width=device-width,initial-scale=1.0,maximun-scale=1.0">
```
这段代码的几个参数解释：
1. width = device-width：宽度等于当前设备的宽度
2. initial-scale：初始的缩放比例（默认设置为1.0）
3. minimum-scale：允许用户缩放到的最小比例（默认设置为1.0）
4. maximum-scale：允许用户缩放到的最大比例（默认设置为1.0）
5. user-scalable：用户是否可以手动缩放（默认设置为no，因为我们不希望用户放大缩小页面）

```html
<!-- 使用媒体类型 -->
<link rel="stylesheet" type="text/css" media="screen and(max-width:960px)" href="phone.css">

<!-- 样式表中的CSS媒体查询 -->
<style>
@media (max-width: 960px) {
  .facet_sidebar {
    width:80px;
    height:80px;
  }
}
</style>
```
*相关链接：*
1. [CSS3 @media 查询](http://www.runoob.com/cssref/css3-pr-mediaquery.html)
2. [Bootstrap栅格系统](http://v3.bootcss.com/css/#grid)
3. [响应式检测](http://responsivedesignchecker.com/#1Q2JeB6d6qKFN)

### 2.2.5 伪类、伪元素
**伪类**:用于当已有元素处于的某个状态时，为其添加对应的样式，这个状态是根据用户行为而动态变化的。比如：`:hover`、`:active`、`:focus`等。
**伪元素**:用于创建一些不在文档树中的元素，并为其添加样式。比如说，我们可以通过:before来在一个元素前增加一些文本，并为这些文本添加样式。虽然用户可以看到这些文本，但是这些文本实际上不在文档树中。比如：`:before`、`:after`等。

*相关链接：*
1. [CSS伪类和伪元素](https://catouse.github.io/css-magic/#selection-style)

### 2.2.6 其他新特性
css3还有选择器、文字效果、阴影和反射、渐变效果等。[详情](https://www.ibm.com/developerworks/cn/web/1202_zhouxiang_css3/)

## 2.3 本地存储
在Html4的时代在浏览器端存储点网站的数据，一般只能存储在`Cookie`中，但是大多是浏览器对于`Cookie`的限制。
1. 大多数浏览器支持最大为 `4M` 字节的 `Cookie`。
2. 浏览器还限制站点可以在用户计算机上存储的 `Cookie` 的数量。大多数浏览器只允许每个站点存储 `20` 个 `Cookie`；如果试图存储更多 `Cookie`，则最旧的 `Cookie` 便会被丢弃。
3. 有些浏览器还会对它们将接受的来自所有站点的 `Cookie` 总数作出绝对限制，通常为 `300` 个。
4. `Cookie`默认情况都会随着`Http`请求发送到后台服务器，但并不是所有请求都需要`Cookie`的。

### 2.3.1 永久本地存储：localStorage
在最新的JS的API中增加了`localStorage`对象，以便于用户存储永久存储的Web端的数据。而且数据不会随着Http请求发送到后台服务器。
```javascript
// 添加本地存储数据，两个参数
localStorage.setItem("userName", "Lee");

// 通过key获取相应的Value
localStorage.getItem("userName");

// 通过key删除本地数据
localStorage.removeItem("userName");

// 清空数据
localStorage.clear();
```

### 2.3.2 会话级别的本地存储：sessionStorage
通过此对象可以直接操作存储在浏览器中的会话级别的WebStorage。存储在`sessionStorage`中的数据首先是Key-Value形式的，另外就是它跟浏览器当前会话相关，当会话结束后，数据会自动清除，跟未设置过期时间的`Cookie`类似。
```javascript
// 添加会话数据，两个参数
sessionStorage.setItem("userName", "Lee");

// 通过key获取相应的Value
sessionStorage.getItem("userName");

// 通过key删除会话数据
sessionStorage.removeItem("userName");

// 清空会话数据
sessionStorage.clear();
```

### 2.3.4 Web SQL Database
html5引入`Web SQL Database`概念，它使用 SQL 来操纵客户端数据库的 API，这些 API 是异步的。是随着HTML5规范加入的在浏览器端运行的轻量级数据库。

*相关链接：*
1. [HTML5本地存储——Web SQL Database](http://www.cnblogs.com/dolphinX/p/3405335.html)
2. [HTML5 Web SQL 数据库](http://www.runoob.com/html/html5-web-sql.html)

### 2.3.5 Indexeddb
`IndexedDB`是一个为了能够在客户端存储可观数量的结构化数据，并且在这些数据上使用索引进行高性能检索的 API。
对于在浏览器里存储数据，你可以使用`cookies`或`local storage`，但它们都是比较简单的技术，而`IndexedDB`提供了类似数据库风格的数据存储和使用方式。存储在`IndexedDB`里的数据是永久保存，不像`cookies`那样只是临时的。`IndexedDB`里提供了查询数据的功能，在online和offline模式下都能使用。你可以用`IndexedDB`存储大型数据。

*相关链接：*
1. [HTML5本地存储——IndexedDB](http://www.cnblogs.com/dolphinX/p/3415761.html)
2. [使用 HTML5 IndexedDB API](https://www.ibm.com/developerworks/cn/web/wa-indexeddb/)

### 2.3.6 离线缓存（Application Cache）
我们通常使用浏览器缓存在用户磁盘上存储web单页，在用户再次浏览的时候已节省带宽，但即便这样，依然无法在没有Internet的情况下访问Web。为了让web应用程序在离线状态也能被访问。html5通过`application cache API`提供离线存储功能。前提是你需要访问的web页面至少被在线访问过一次。

***慎用：*** `application cache`会默认缓存当前页面，不好清除。

*相关链接：*
1. [HTML5离线缓存（Application Cache）](http://www.cnblogs.com/lovesong/p/5021992.html)
2. [HTML5 Application Cache](http://blog.csdn.net/fwwdn/article/details/8082433)

## 2.4 三维、图形及特效
### 2.4.1 Canvas
使用`canvas`(通常为`JavaScript`)在其中绘制图形的 HTML 元素。
```html
<!-- 标签定义图形，比如图表和其他图像，必须使用脚本来绘制图形 -->
<canvas id="myCanvas" width="500px" height="500px"></canvas>

<script type="text/javascript">
  var canvas=document.getElementById('myCanvas');
  var ctx=canvas.getContext('2d');
  ctx.fillStyle='#FF0000';
  ctx.fillRect(0,0,80,100);
</script>
```
*相关链接：*
1. [Canvas 教程](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API/Tutorial)
2. [<canvas> 标签详解](http://www.w3school.com.cn/html5/html5_canvas.asp)
3. [Echarts-基于canvas的丰富图表](http://echarts.baidu.com/)

### 2.4.2 SVG
`SVG`是"Scalable Vector Graphics"的简称。中文可以理解成“可缩放矢量图形”。
1. SVG是指可伸缩矢量图形。
2. SVG用来定义用于网络的基于矢量的图形。
3. SVG使用XML格式定义图形。
4. SVG图像在放大或缩小（改变尺寸）的情况下，其图形质量不会受受损失。
5. SVG是W3C的一个标准。

```html
<!-- svg画个半径为50的圆 -->
<svg enable-background="new 0 0 145 145" id="Layer_1" version="1.1" viewBox="0 0 145 145" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
  <circle id="redcircle" cx="50" cy="50" r="50" fill="red" />
</svg>
```
*相关链接：*
1. [SVG 入门教程](http://blog.csdn.net/lily1995030512/article/details/47264413)
2. [HTML5 SVG 详解1](http://www.w3school.com.cn/html5/html_5_svg.asp)
3. [HTML5 SVG 详解2](http://www.runoob.com/svg/svg-inhtml.html)
4. [D3-基于svg的丰富图表1](https://github.com/d3/d3)
5. [PykCharts-基于svg的丰富图表1](https://github.com/pykih/PykCharts.js)

### 2.4.3 WebGL
1. `WebGL` 是一种 3D 绘图标准，这种绘图技术标准允许把 `JavaScript` 和 `OpenGL ES 2.0` 结合在一起，通过增加 `OpenGL ES 2.0` 的一个 `JavaScript` 绑定，`WebGL` 可以为 `HTML5 Canvas` 提供硬件 3D 加速渲染，这样 Web 开发人员就可以借助系统显卡来在浏览器里更流畅地展示3D场景和模型了，还能创建复杂的导航和数据视觉化。
2. 适用于开发 3D 模型和场景的程序员。

*相关链接：*
1. [WebGL api 中文版](http://wiki.jikexueyuan.com/project/webgl/)
2. [WebGL 自学教程](http://blog.csdn.net/tiewen/article/details/6895582)
3. BabylonJS：一个运用 HTML5 和 WebGL 构建 3D 游戏的框架。[GitHub](https://github.com/BabylonJS/Babylon.js)、[官网](http://www.babylonjs.com/)
4. Cesium：开源的、基于 WebGL 实现的虚拟地球仪和地图引擎。[GitHub](https://github.com/AnalyticalGraphicsInc/cesium)、[官网](https://cesiumjs.org/)

## 2.5 网页多媒体
多媒体指的是音效、音乐、视频和动画。
### 2.5.1 Video
```html
<!-- 标签中的Controls,可以使得播放器工具栏可见 -->
<video controls width="500px" id="vid">
  <source src="vid.mp4" />
</video>
```
支持的格式：`MP4`,`webm`,`3gpp`,`m4v`,`mpeg`,`ogg` ,`quicktime`,`x-ms-wmvright`格式。
| 属性    | 值     | 描述   |
| :----   | :----- | :----- |
| autoplay | autoplay | 如果出现该属性，则视频在就绪后马上播放。 |
| controls | controls | 如果出现该属性，则向用户显示控件，比如播放按钮。 |
| height | pixels | 设置视频播放器的高度。 |
| loop | loop | 如果出现该属性，则当媒介文件完成播放后再次开始播放。 |
| muted | muted | 规定视频的音频输出应该被静音。 |
| poster | URL | 规定视频下载时显示的图像，或者在用户点击播放按钮前显示的图像。 |
| preload | preload | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
| src | url | 要播放的视频的 URL。 |
| width | pixels | 设置视频播放器的宽度。 |

### 2.5.2 Audio
```html
<!-- 简单的 HTML 5 音频 -->
<audio src="someaudio.wav">
  您的浏览器不支持 audio 标签。
</audio>
```
| 属性    | 值     | 描述   |
| :----   | :----- | :----- |
| autoplay | autoplay | 如果出现该属性，则音频在就绪后马上播放。 |
| controls | controls | 如果出现该属性，则向用户显示控件，比如播放按钮。 |
| loop | loop | 如果出现该属性，则每当音频结束时重新开始播放。 |
| muted | muted | 规定视频输出应该被静音。 |
| preload | preload | 如果出现该属性，则音频在页面加载时进行加载，并预备播放。 如果使用 "autoplay"，则忽略该属性。 |
| src | url | 要播放的音频的 URL。 |

*相关教程：*
1. [HTML5-多媒体使用](http://blog.csdn.net/powertoolsteam/article/details/50727731)

## 2.6 设备访问、性能与集成
### 2.6.1 桌面通知 (Notifications)
有点类似于显示器右下角蹦出的QQ弹框，跟浏览器是脱离的，消息是置顶的。

**效果图：**
![桌面通知效果图](http://lee.yiger.com.cn/assets/images/html5-img2.jpg)

*相关链接：*
1. [HTML5中的Web Notification桌面通知](http://www.zhangxinxu.com/wordpress/2016/07/know-html5-web-notification/)

### 2.6.2 Camera API
通过`Camera API`,你可以使用手机的摄像头拍照,然后把拍到的照片发送给当前网页.这些操作主要是通过一个input元素来实现的,其中该元素的type属性必须为"file",accept属性要允许图片格式。
```html
<input type="file" id="take-picture" accept="image/*">
```

*相关链接：*
1. [Camera API教程](https://developer.mozilla.org/zh-CN/docs/Web/Guide/API/Camera)

### 2.6.3 全屏(Fullscreen)API
可以全屏显示,交互完成,随时可以退出全屏状态。
```javascript
// 全屏
var elem = document.getElementById("content");
if (elem.requestFullscreen) {
  elem.requestFullscreen();
}
```

*相关链接：*
1. [全屏 API教程](http://blog.csdn.net/xiao190128/article/details/51105903)

### 2.6.4 WebSocket
`WebSocket`是HTML5开始提供的一种在单个 TCP 连接上进行全双工通讯的协议。
在`WebSocket` API中，浏览器和服务器只需要做一个握手的动作，然后，浏览器和服务器之间就形成了一条快速通道。两者之间就直接可以数据互相传送。
```javascript
// webSocket
var webSocket = new WebSocket('ws://localhost:8080/WebSocket/websocket');

// 与WebSocket建立连接
webSocket.onopen = function(event) { ...};

// 处理服务器返回的信息
webSocket.onmessage = function(event) { ...};

// 错误处理
webSocket.onerror = function(event) { ...};
```

*相关链接：*
1. [HTML5 WebSocket教程1](http://www.runoob.com/html/html5-websocket.html)
2. [HTML5 WebSocket教程2](http://www.cnblogs.com/shizhouyu/p/4975409.html)

### 2.6.5 Web Worker
Web Worker为Web内容在后台线程中运行脚本提供了一种简单的方法。线程可以执行任务而不干扰用户界面。

*相关链接：*
1. [Web Workers Api](https://developer.mozilla.org/zh-CN/docs/Web/API/Web_Workers_API/Using_web_workers)
2. [HTML 5 Web Workers 教程](http://www.w3school.com.cn/html5/html_5_webworkers.asp)

### 2.6.6 更多属性
1. `XMLHttpRequest Level 2`：允许异步读取页面的某些部分，允许其显示动态内容，根据时间和用户行为而有所不同。这是在 Ajax背后的技术。[参考教程](https://developer.mozilla.org/zh-CN/docs/Web/API/XMLHttpRequest)
2. `History API`：允许对浏览器历史记录进行操作。这对于那些交互地加载新信息的页面尤其有用。[参考教程](https://segmentfault.com/a/1190000002447556)
3. `contentEditable`：把你的网站改变成 wiki！HTML5 已经把 contentEditable 属性标准化了。[参考教程](https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/Content_Editable)
4. `拖放`：HTML5 的拖放 API 能够支持在网站内部和网站之间拖放项目。同时也提供了一个更简单的供扩展和基于 Mozilla 的应用程序使用的 API。[参考教程](http://www.cnblogs.com/jscode/archive/2013/05/10/3575024.html)
5. `使用 Camera API`：允许使用和操作计算机的摄像头，并从中存取照片。[参考教程](https://developer.mozilla.org/zh-CN/docs/Web/Guide/API/Camera)
6. `触控事件`：对用户按下触控屏的事件做出反应的处理程序。[参考教程](https://developer.mozilla.org/zh-CN/docs/Web/API/Touch_events)
7. `使用地理位置定位`：让浏览器使用地理位置服务定位用户的位置。[参考教程](https://developer.mozilla.org/zh-CN/docs/Web/API/Geolocation/Using_geolocation)
8. `检测设备方向`：让用户在运行浏览器的设备变更方向时能够得到信息。这可以被用作一种输入设备（例如制作能够对设备位置做出反应的游戏）或者使页面的布局跟屏幕的方向相适应（横向或纵向）。[参考教程](https://developer.mozilla.org/zh-CN/docs/Web/API/Detecting_device_orientation)

## 3. 周边
### 3.1 当下流行的 `js` 框架
1. `jQuery`：老牌框架，丰富的社区和插件支持。[教程](http://www.w3school.com.cn/jquery/)、[API手册](http://jquery.cuishifeng.cn/)
2. `Zepto.js`：移动端的`jQuery`。[GitHub](https://github.com/madrobby/zepto)、[API手册](http://www.css88.com/doc/zeptojs_api/)
3. `Angular.js`：优秀的前端JS框架，有着诸多特性，最为核心的是：MVVM、模块化、自动化双向数据绑定、语义化标签、依赖注入等等。[官网](https://www.angular.cn/)、[中文社区](http://www.angularjs.cn/)、[Angular1教程](https://code.ziqiangxuetang.com/angularjs/angularjs-include.html)
4. `react.js`：更多的是处理view层，反正挺火的。[官网](https://doc.react-china.org/)、[中文社区](http://react-china.org/)
5. `Vue.js`：MVVM框架，反正挺火的。[官网](http://cn.vuejs.org/v2/guide/)
6. `San.js`：百度团队历时2年开发的MVVM框架，可兼容到IE6。[官网](https://ecomfe.github.io/san/)
7. `Backbone.js`：为复杂WEB应用程序提供模型(models)、集合(collections)、视图(views)的结构。[API文档](http://www.css88.com/doc/backbone/)
8. 还有更多优秀的前端`javascript`框架：[requirejs](http://requirejs.org/)、[Ionic](http://www.ionic.wang/js_doc-index.html)、[JQuery Mobile](http://jquerymobile.com/)......

### 3.2 当下流程的UI框架
1. `Bootstrap`：[官网](http://www.bootcss.com/)
2. `Layui`：[官网](http://www.layui.com/)
3. `妹子UI`：[官网](http://amazeui.org/css/)
4. `EasyUI`：[官网](http://www.jeasyui.net/)
5. `ZUI`：[官网](http://zui.sexy/)
6. `Pure`：[官网](https://www.purecss.cn/)
7. `HUI`：[官网](http://www.h-ui.net/index.shtml)
8. `ANT DESIGN`：[官网](https://ant.design/index-cn)
9. `移动端UI框架-SUI`：[官网](http://m.sui.taobao.org/)
10. `移动端UI框架-WUI`：适用微信的UI框架。[GitHub](https://github.com/Tencent/weui)
11. `移动端UI框架-MUI`：[官网](http://dev.dcloud.net.cn/mui/)
12. `移动端UI框架-AUI`：[官网](http://www.auicss.com/)
13. 还有更多优秀的UI框架......

### 3.3 构建工具&自动化 相关
1. `NodeJS`：[中文网](http://nodejs.cn/)
2. `Node Packages(npm)`：nodeJS的包管理器。[官网](http://npmsearch.com/)
3. `bower`：包管理器。[官网](http://bower.io/)、[bower简明入门教程](https://segmentfault.com/a/1190000002971135)
4. `npm国内镜像`：[官网](https://npm.taobao.org/)
5. `Grunt`：[官网](http://www.gruntjs.net/)、[教程示例](http://blog.csdn.net/wangfupeng1988/article/details/46418203)
6. `Gulp`：[官网](http://www.gulpjs.com.cn/)
7. `Webpack`：[官网](https://webpack.github.io/)、[中文网](http://webpackdoc.com/)、[入门教程](http://www.jianshu.com/p/42e11515c10f)
8. `NodeJS`：[官网](http://nodejs.cn/)
9. `NodeJS`：[官网](http://nodejs.cn/)
10. 还有更多优秀的前端工具......

## 4.写在后面，错误和不足之处欢迎指正:smile:。
1. 知识太多，难免有遗漏和不足支持，欢迎指正:clap:。
2. 本文初衷仅是喜欢和分享，不作其他用途，参考借鉴之处如有侵权请联系删除:feet:。