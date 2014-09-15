---
layout: post
title: JavaScript 编码风格
date: 2014-09-15T19:20:13+08:00
description: "mac系统下锁屏"
tags: [lock mac]
image:
  background: triangular.png
comments: true
share: true
---
>来自支付宝的《JavaScript 编码风格》
---

下面是一些常用注意点：


## 编码

统一用 utf-8


## 长度

长度不超过 80 个字符。别小看这一条规则，如果严格去遵循，你会发现代码变清晰了。而且，你一定能做到的。

参考:

1. pep8 为 79 个字符
2. npm 为 80 个字符
3. google 为 80 个字符


## 缩进

缩进使用 2个 或 4个 空格，组件内保持统一，不混用。禁用 tab。

参考：

1. npm 为 2 空格
2. pep8 为 4 空格
3. google 为 2 空格( gjslint 没规定)
4. 大部分前端工程师习惯 4 空格

Vim 设置 tab 为 4 空格：

{% highlight js %}
set tabstop=4
set shiftwidth=4
set expandtab
{% endhighlight %}


## 花括号

### 花括号不换行

好

{% highlight js %}
if (foo) {
}
{% endhighlight %}

坏

{% highlight js %}
if (foo)
{
}
{% endhighlight %}

**不允许一行判断，一律换行**

坏

{% highlight js %}
if (foo) return;
{% endhighlight %}

##命名约定

1. 常量 UPPERCASE_WORD
2. 变量 camelName
3. 类名 CamelName


## 空格

### 操作符之间需要空格

好

{% highlight js %}
var x = y + z
{% endhighlight %}

坏

{% highlight js %}
var x=y+z
{% endhighlight %}

### 只空一格

好

{% highlight js %}
{
    a: 'short',
    looooongname: 'long'
}
{% endhighlight %}

坏

{% highlight js %}
{
    a           : 'short',
    looooongname: 'long'
}
{% endhighlight %}

## 逗号与换行

建议用自然人的处理方法

{% highlight js %}
{
   a: 'a',
   b: 'b',
   c: 'c'
}
{% endhighlight %}

不建议使用 npm 风格的逗号与换行，即

{% highlight js %}
{
   a: 'a'
  ,b: 'b'
  ,c: 'c'
}
{% endhighlight %}


## 变量声明

首先，**变量在使用前必须声明**。

对于单 var 模式和多 var 模式，不做强行约定，但同一个文件里，风格必须一致。



## 相关链接
- [JavaScript 编码风格](https://github.com/aralejs/aralejs.org/wiki/JavaScript-编码风格)
- [编码与文档风格讨论](https://github.com/aralejs/aralejs.org/issues/36)