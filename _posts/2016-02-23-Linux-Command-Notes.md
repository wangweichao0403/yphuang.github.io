---
layout: post
title: "Linux常用命令备忘录（持续更新）"
author: "yphuang"
date: 2016-02-23
categories: blog
tags: [Linux,备忘录]

---


## vi编辑器的基本操作

在Linux系统中，熟练使用文本编辑器来编辑Linux参数配置文件是一件极其重要的事情。

vi作为Linux内的一款文本编辑器，具有以下几点不可不学的理由：

- 所有UNIX Like系统均内置了vi文本编辑器；

- 很多软件编辑接口主动调用vi；

- vim（高级版的vi）具有程序编辑的能力，方便debug；

- 简单，快速。

### 认识vi

vi共有三种模式：

- 一般模式
    + 进行删除，复制，粘贴等操作

- 编辑模式
    + 对文本内容进行编辑

- 命令行模式
    + 提供数据查找，读取，保存，大量替换字符，离开vi，显示行号等操作
    

### 三种模式之间的切换

一张图看懂：

<center>
    <p><img src="https://raw.githubusercontent.com/yphuang/yphuang.github.io/master/img/vi_switch.jpg" align="center"></p>
</center>


### 常用按键

#### 一般模式

| 移动光标操作 | 功能说明 |
|--------------|:--------:|
| h（或左箭头） | 光标左移 |
| j（或下箭头）| 光标下移 |
| k （或上箭头）|光标上移 |
|l（或右箭头）|光标右移|
|[Ctrl]+f| 屏幕向下移动一页|
|[Ctrl]+b|屏幕向上移动一页|
|0或功能键[Home]|移动到这一行的最前面字符处|
|$或功能键[End]|移动到这一行的最后面字符处|
|G|移动到文件的最后一行|
|gg|移动到文件的第一行，与1G等价|
|n+[Enter]|n为数字，光标向下移动n行|

***


| 查找与替换操作 | 功能说明 |
|--------------|:--------:|
| /word | 向下查找'word'字符串 |
|?word|向上查找'word'字符串|
|n|向下重复前一个查找操作|
|N|与n相反，反向进行前一个查找|
|:1,\$s/word1/word2/g|从第一行到最后一行查找word1，并将该字符串替换为word2|
|:1,\$s/word1/word2/gc|从第一行到最后一行查找word1，并将该字符串替换为word2,替换前提示是否替换|

***

| 删除，复制与粘贴操作 | 功能说明 |
|--------------|:--------:|
|x,X|x为向后删除一个字符（相当于[Del]按键），X为向前删除一个字符（相当于[Backspace]）|
|dd|删除光标所在的那一整行|
|ndd|n为数字。删除光标所在的向下n行|
|yy|复制光标所在的那一行|
|nyy|n为数字。复制光标所在的向下n行|
|p,P|p为将已复制的数据在光标的下一行粘贴，P为粘贴在光标的上一行|
|u|复原前一个操作|
|[Ctrl]+r|重做上一个操作|
|.|小数点。重复前一个操作|


***

#### 一般模式切换到编辑模式


| 切换操作 | 功能说明 |
|--------------|:--------:|
|i,I|进入插入模式。i为从目前的光标所在处插入，I为在目前所在行的第一个非空格处开始插入|
|a,A|进入插入模式。a为从目前光标所在处的下一个字符处插入，A为从光标所在行的最后一个字符处开始插入|
|o,O|进入插入模式。o为在目前光标所在的下一行出插入新的一行，O为在目前光标所在处的上一行插入新的一行|
|r,R|进入替换模式。r替换光标所在那一个字符一次；R会一直替换光标所在的文字，直到按下[Esc]按键|
|[Esc]|退出编辑模式，回到一般模式|


***

#### 一般模式切换到命令行模式


| 切换操作 | 功能说明 |
|--------------|:--------:|
|:w|将编辑的数据写入硬盘文件中|
|w!|若文件为“只读”，可强制写入该文件|
|:q|离开vi|
|:q!|强制离开而不保存|
|:wq|保存后离开，若为":wq!",则是强制保存后离开|





## 其它常用命令

### c

- `cd`:

- `chmod`:
    + 格式：`chmod [-cfvR] [--help] [--version] mode file  `
    + <http://www.cnblogs.com/peida/archive/2012/11/29/2794010.html>
    
### m

- `mv`:

### r

- `rz`:传入文件

### s

- `sudo su`:以root身份登录 

- `sz`:导出文件

### v

- `vi`:进入vim编辑器


## 参考文献

- 『鸟哥的Linux私房菜』
