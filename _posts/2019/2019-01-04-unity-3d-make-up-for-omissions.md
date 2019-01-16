---
layout: article
title: Unity 拾遗（一）
date: '2019-01-04 16:36:00 +08:00'
key: '2019-01-04_16:09'
tags:
  - Unity
---

Overview

![picture](/images/2018/09/post-hi-DinoTossing.jpg)

从网上整理的一些有关 Unity 的，大多数新手可能都未曾注意到的细节。

<!--more-->

## 操作篇

### 1.按网格移动

按住Ctrl拖动物体可以按照网格移动或者旋转，Edit—Snap Settings可以设置移动大小和旋转的幅度。

![MoveObject](/images/2019/01/ctrlMove.png)

调整到合适的数据

![adjust](/images/2019/01/adjust.png)

### 2.Debug 模式

大家知道，只有在脚本中定义为public的变量才可以在Inspector面板中看到，private类型的变量是看不到的。但是调整Inspector面板的Debug模式可以看到私有变量，更好的在游戏运行的过程中观察私有变量。

如下：一个public，一个private

![Debug](/images/2019/01/debug.png)

选择debug模式：

![selectdebug](/images/2019/01/selectdebug.png)

Public类型的var1和private类型的var2都可以看到：

![4-display](/images/2019/01/4-display.png)

### 3.在 Inspector 中显示 float 变量

float 类型的变量可以再 Inspector 面板中设置成滑块的样式。（ int 类型的好像不行）

![SetRange](/images/2019/01/setrange.png)

![4-display-2](/images/2019/01/4-display-2.png)

### 4.保存 Play 模式中调整的属性值

在 play 模式中改变 Inspector 面板中的属性值，在运行结束后属性并不会改变。如果你在 play 模式中找到了合适的参数，可以点击组件右上角的小齿轮，选择 copy Component 。在运行结束后，再次点击小齿轮，选择 Copy Component Values 将属性值粘贴上去。

### 5.给Inspector面板的属性分组并添加标题

![addtitle](/images/2019/01/addtitle.png)

效果呈现如下，管理脚本和数据更方便。

![4-dispaly-3](/images/2019/01/4-dispaly-3.png)

## 代码篇

有时候项目出现麻烦，可能这些麻烦并不是因为项目本身，而是因为糟糕的编程习惯，使你的项目像一团毛线球，越缠越乱。你有没有养成这些习惯？

### 1. 注释。

别让这么尴尬的事情发生在你身上：读不懂前一段时间自己写的代码。尤其是大量的代码，即使是你自己写的，从头再读也不是一件舒服的事情。

### 2. 经常性Ctrl+S保存

意外可能会来临，说不定就是在你头上。电脑死机程序崩溃是不得不预防的一件倒霉事，而Ctrl+S就是预防针。

### 3. 清晰明了的命名规则

名字是对物体进行的信息标注，别让名字那么随心所欲，往往通过名字，我们就能大概获得一系列相关的信息，使得程序的可读性、可维护性大大提升。

### 4. 函数

函数应该尽可能简单精巧，便于调试；一个函数实现一个功能；函数通过名称说明其功能，并隐藏函数的细节。

### 5. 处理错误

软件存在错误正常的，因此正确合适的处理错误也就成为了非常重要的一部分。而且错误通常是不可预知的，所以要尽可能为可能发生的错误安排好处理计划，否则，错误严重可能导致程序崩溃。尽可能不要返回和传递NULL的值，因为这样会导致很多问题，可能导致函数出错。

### 6. 代码简化

第一次写出来的代码并不一定是最佳代码，回头看一下，稍微思考一下，就会发现还会有更简单更简洁更明了的写法。

以上的内容并不完善，欢迎大家评论补充！让我们从干净整洁的代码写起！