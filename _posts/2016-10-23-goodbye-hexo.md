---
layout: post
title: 再见， Hexo
tags: [Software, Hexo]
categories: Opinion
---

其实我现在的心情比较复杂。
Hexo 我从大一的暑假就开始用，大二的时候加入了 Hexo 的团队，一直到现在，关于 Hexo 的文章都是我博客点击率最高的文章。
但是由于我实在是精力有限，没有时间去维护Hexo的相关项目，因此只能与Hexo说再见了，希望能有更多人可以加入Hexo的开发团队，希望Hexo能够发展的更好。
下面简单地分享一下自己在Hexo团队中做的工作和学到的东西。

<!-- more -->

## 我给Hexo带来了什么

- 版本更新时的反馈。得益于`Travis CI`的自动构建能力，我可以在版本推送的第一时间进行构建并得到反馈。事实上，作者就是使用我的库进行测试的。
- Pull Request的Review与Merge。其实这个方面在最开始的时候不是做的特别好，因为对`Node.js`不熟悉，向`master`分支导入了很多ugly的代码。不过做的多了就开始对`Node.js`有了自己的感觉。
- Issues的回复与维护。在我进入Team之前，Issues区有上千个没有回复或处理的问题。在Team成立之后，在我们团队成员的努力之下，这个数字减少到了300+。
- BUG的Fix。学会了一点`Node`之后我开始尝试自己修复`BUG`，有一个`BUG`确认修好了，但是很可惜没有能推到`NPM`上。
- **一次官方网站的完全宕机。** 这个涉及到`Travis CI`的一个`BUG`，导致我的自动构建任务在出错之后没有停止反而是直接进行了一次提交，从而导致官网直接挂了。详情可以参考： <https://github.com/hexojs/site/issues/134> 。

## 我从Hexo中学到了什么

我使用Hexo的这三年，是我精力最旺盛，时间最宽裕的三年。在这期间，我掌握了如下的东西：

### 技术

- `Node.js`初步入门，能用`Node`写一些简单的轮子，能看懂源代码并修复BUG。
- `HTML`，`CSS`初步入门，能对设计稿进行切分并实现相应效果，了解了几个比较常见的`CSS`框架：`Bootstrap`，`Semantic UI`等

### 技巧

- 学习使用了几个常见前的前端工具，比如：`Grunt`，`Gulp`，`Bower`等
- 学会了`Git`，可以熟练使用`Git`的`branch`，`rebase`等功能来进行协作
- 掌握了域名解析的全部过程，申请了自己的第一个域名

### 技能

- 能够熟练运用`Travis CI`来实现自动构建与持续集成
- 英文的书面表达能力在和外国友人沟通的时候有了很大的提高

### 思想

- 开源的习惯：喜欢开源自己的代码，喜欢去学习别人的代码，喜欢使用开源产品，喜欢在社区反馈并尝试修复自己发现的问题。
- 遇到问题不会再想着推给别人，而是首先考虑自己能不能修复，或者有没有别的解决方案。


## 如何从Hexo迁移到Jekyll

非常有趣的一点是，网上非常多人都是从Jekyll迁移到Hexo，但是很少人有反向迁移的。
从Hexo迁移到Jekyll其实非常简单，Hexo和Jekyll基本兼容，只需要读取文章的日期，并修改文件名为`YYYY-MM-DD-<post_name>.md`即可。根据情况，还需要给文章添加`layout: post`，并修改文章内容中一些不兼容的格式。
我用Python写了一个简单的脚本，稍微整理整理之后会开源在Github并推送到Pypi上。

## 更新日志

- 2016年10月23日 首次发布
