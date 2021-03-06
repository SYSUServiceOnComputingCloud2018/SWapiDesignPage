# SWapiDesignPage

#### 成员信息

| 小组成员 | 学号     | 姓名   | 分工 |
| -------- | -------- | ------ | ---- |
| 组长     | 16340240 | 吴天扬 | 后端 |
| 组员     | 16340226 | 王迎旭 | 后端 |
| 组员     | 16340232 | 王泽浩 | 后端 |
| 组员     | 16340243 | 吴梓溢 | 前端 |
| 组员     | 16340224 | 王显淼 | 前端 |
| 组员     | 16340239 | 吴良澔 | 前端 |

## 项目介绍
本次项目我们团队选择了复制https://swapi.co/ 网站这一项目。该网站主要功能为：用户输入一个Star War系列电影中的人物名字，后端查询并返回一个json数据包给前端，前端网页解析该数据包并把其中的内容反馈到网站界面上。

分析项目需求后，本次项目主要分为两个大部分---前端部分和后端部分。
   - 前端负责使用富客户端js架构完成相关网页的界面实现，并调用后端实现的api接口获取到相关的数据包进行解析并在网页上完成动态更新；
   - 后端负责利用boltDB数据库作为数据库基础，利用前端网页返回的客户输入作为查询依据返回储存在数据库中的相关人物的信息的json数据包。

## 前端部分的实现
前端部分采用Vue.js语言完成实现。Vue是一套用于构建用户界面的渐进式框架，相较于其他的网页语言，它更容易上手，同时功能也十分丰富。在了解了Vue.js相关的语法和用法之后，根据原网站所提供的css文件和html文件，我们用Vue.js实现了自己的界面。

## 后端部分的实现
- 数据库的选择：

   本次项目选择boltDBzuo作为我们的数据库基础，最开始固然是因为实验要求我们使用boltDB数据库，可是我们在使用这个数据库后，发现它是一款成功的轻量级数据库，它成功的地方在于提供了一个足够开发者使用的基本功能与可以很方便开发高级功能的接口。这样子有几个好处：

   1. 因为源代码的长度有限，开发和维护成本被降低了。这使得它可以以很快的速度跟上软件开发的潮流，始终使用最新的技术，如果有的话。

   2. 足够的自由与轻量化。大多数时候开发者其实并不需要很复杂的功能，无论是python还是go，它们与传统的C与Java的区别就是足够方便。绝大多数情况下，C语言都是够用的，但为什么不用C语言，就是因为C语言过于复杂。C语言的开发的过程不算简单，但是维护成本异常的高，而且更接近汇编语言而不是人类思维。而go语言则不同，方便易得的多线程和异步调用使得开发过程大大降低，很多优化也更贴近于开发者的视角而不是编译器的视角。因此boltdb是更适合于go的一款数据库，它足够的简洁、轻量却又功能强大。

- api的实现：
  
   利用boltDB数据库技术，参考https://swapi.co/documentation#base 网页所提供的api文档完成相关api的开发设计。在开发过程中，参考 github v3 或 v4 overview 标准。
