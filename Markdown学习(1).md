# 学习markdown #
<style>
  .center {
    width: auto;
    display: table;
    margin-left: auto;
    margin-right: auto;
  }
</style>
## 一、概述说明 ##
&emsp;&emsp;Markdown&nbsp;&nbsp;是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。[^1]  
&emsp;&emsp;目前markdown可以在多种网站上进行交互，例如cnblog、cdsn、github，这些网站都支持&nbsp;&nbsp;markdown&nbsp;&nbsp;格式。所以有其学习的必要性。  
&emsp;&emsp;本文基于博客园展示效果来简述markdown的一些语法及其使用。
## 二、编辑器选择 ##
&emsp;&emsp;为了更好的书写markdown格式的纯文本，本文推荐 widonws 平台下使用软件 markdownpad，下载地址：[https://markdownpad.com/download.html](https://markdownpad.com/download.html)。安装后可能遇到错误提示“HTML Render Error”，可通过安装插件 awesomium 来修复。[^2]  
<div align="center"><img align="middle" src="http://tiebapic.baidu.com/forum/w%3D580/sign=9369d84ba41bb0518f24b320067ada77/b532682dd42a28340e85e2624cb5c9ea15cebf20.jpg"></img></div>  

## 三、语法介绍 ##
&emsp;&emsp;语法糖：当一些格式无法实现时请借助 html 标签，基本可以搞定。  
### 1、标题格式  ###
&emsp;&emsp;标题格式是通过 "#"+空格 实现的。
&emsp;&emsp;一级标题: "#&nbsp;&nbsp;一级标题&nbsp;&nbsp;#" (两个空格)  
&emsp;&emsp;一级标题: "##&nbsp;&nbsp;二级标题&nbsp;&nbsp;##" (两个空格)  
&emsp;&emsp;一级标题: "###&nbsp;&nbsp;三级标题&nbsp;&nbsp;###" (两个空格)  
&emsp;&emsp;当然，如果使用&nbsp;&nbsp;MarkdownPad&nbsp;&nbsp;编辑器，工具栏有内置的 H1 和 H2。  
### 2、段落格式  ###
####  &emsp;&emsp;段落换行  
&emsp;&emsp;a、行尾添加两个以上空格加换行符实现。  
&emsp;&emsp;b、用一个空行简单的将两段落隔开。  
&emsp;&emsp;c、可以借助"<p\></p\>"标签实现。  
####  &emsp;&emsp;段落缩进  
&emsp;&emsp;段落缩进借助&nbsp;html&nbsp;标签实现  
&emsp;&emsp;a、&emsp\;来表示一个全角空格；  
&emsp;&emsp;b、&ensp\;表示一个半角空格。  
&emsp;&emsp;c、&nbsp\;表示行中间的空格。  
###  3、字体格式  ###
&emsp;&emsp;a、斜体文本，\*斜体文本\*：*斜体文本*；  
&emsp;&emsp;b、粗体文本，\*\*粗体文本\*\*：**粗体文本**;    
&emsp;&emsp;c、粗斜体文本，\*\*\*粗斜体文本\*\*\*：___粗斜体文本___;   
&emsp;&emsp;d、分割线，一行中用三个以上的星号、减号、底线来建立一个分隔线：  

---  

&emsp;&emsp;e、删除线，用s标签实现 <s\>删除线\<\/s\>：<s>删除线</s>  
&emsp;&emsp;f、文本居中，<center\>居中文本</center\>: <center>居中文本</center>  
&emsp;&emsp;&emsp;&ensp;注意，在使用center后的文本独占一行。  
&emsp;&emsp;g、脚注，首先要定义脚注: "[^LABEL]: "，在引用处使用[^LABEL]即可。上文中的[1]、[2]都是以此方法实现。
###  4、插入图片  ###
&emsp;&emsp;a.借助&ensp;Markdown&ensp;提供的&ensp;alt&ensp;标签实现：\!\[alt 属性文本\]\(图片地址 "可选标题"\) 可选标题项可省略。  
&emsp;&emsp;b.借助&ensp;html&ensp;提供的&ensp;<img\>&ensp;标签实现： \<img src="图片地址"\></img\>，可以添加 img 标签支持的样式及属性。  
&emsp;&emsp;c.借助&ensp;html&ensp;提供的&ensp;<img\>&ensp;标签和&ensp;<div\>&ensp;标签实现图片居中。本文章节二中就是如此实现。  
###  5、插入代码块  ###
&emsp;&emsp;a.行内插入某个函数或这一行代码，用"\`"括起来即可。\`printf()\`: `printf()`  
&emsp;&emsp;b.一整块代码，可以在每行代码前加4个空格或1个tab。注意：起止行要与其他部分加空行隔开      

		#!/usr/bin/python  
		# -*- coding: utf-8 -*-  
	
	
		def main():
	    	print('hello world')
	
		main()

###  5、插入表格  ###
&emsp;&emsp;在Markdown中，用 | 分割前后单元格，用-来分隔表头行和其他行。  

	<div class="center">  
	|表头|表头|表头|  
	|---|---|---|  
	|内瓤|内容|内容|  
	</div>  

显示效果如下:
<div class="center">

|表头|表头|表头|   
|---|---|---|  
|内瓤|内容|内容| 
 
</div>  

&emsp;&emsp;在分割表头行和数据行时可以用&emsp;:--- 表示左对齐;&emsp;:---:表示居中对齐;&emsp;---: 表示右对齐。  
&emsp;&emsp;如果要实现整个表格的居中，可以在文档开头定义类选择器，设置好居中格式，然后将表格写入&ensp;div&ensp;标签，并为标签设置class属性。本文开头有全局的style，并且为表格设置了格式。此方法对于所有不可实现的格式都可用。甚至表格本身都可以用&ensp;table&ensp;标签实现。  

	<style>.center {
	  width: auto;
	  display: table;
	  margin-left: auto;
	  margin-right: auto;
	}
	</style>

###  6、插入区块  ###
&emsp;&emsp;笔者理解这里的区块就类似文章标题的缩进，可以用">"加空格实现。  

	\> 1、概述说明  
	\> 2、编辑器选择
	\> 3、语法介绍  
	\>  
	\> \> 3.1、标题格式  
	\> \> 3.2、段落格式  

显示效果如下：   
> 1、概述说明  
> 2、编辑器选择
> 3、语法介绍  
> > 3.1、标题格式  
> > 3.2、段落格式 
>  
> 4、本篇博客效果  
###  6、插入列表  ###
&emsp;&emsp;无序列表使用星号(*)、加号(+)或是减号(-)作为列表标记。  
&emsp;&emsp;有序列表使用数字并加上 . 号来表示。

	<div class="center">
	* 星期一
	* 星期二
	* 星期三
	
    1. 第一行
	2. 第二行
	3. 第三行
	</div>

&emsp;&emsp;显示效果：  

<div class="center">
* 星期一
* 星期二
* 星期三

1. 第一行
2. 第二行
3. 第三行
</div>

###  7、插入公式  ###
###  8、插入流程图  ##
## 四、本篇博客效果 ##
&emsp;&emsp;本文的文本效果可以参考博客园[https://www.cnblogs.com/mengrui291/p/12807050.html](https://www.cnblogs.com/mengrui291/p/12807050.html "学习markdown")
&emsp;&emsp;文本文档全内容可以参考
## 五、注意事项  ##
&emsp;&emsp;如果使用了 div 标签，请注意标签前后各留一空行。
## 六、参考资料 ##
[^1]: https://baike.baidu.com/item/markdown/3245829?fr=aladdin
[^2]: https://blog.csdn.net/Z1272633296/article/details/104613743
[^3]: https://www.runoob.com/markdown/md-tutorial.html  
1、 https://baike.baidu.com/item/markdown/3245829?fr=aladdin  
2、 https://blog.csdn.net/Z1272633296/article/details/104613743  
3、 https://www.runoob.com/markdown/md-tutorial.html  
