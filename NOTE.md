# 前端（h5+css3）  

---  

## 1. Web标准

1. 结构 ——> HTML  
2. 表现 ——> CSS
3. 行为 ——> JavaScript  

---  

## 2. HTML标签
> 大部分是双标签有头有尾  

### 2.1 HTML基本标签  
- HTML标签： 叫做根标签，是页面里面最大的标签  ——> **\<html>\</html>**
- 头部标签： 里面必须设置的标签是title ——> **\<head>\</head>**
- 标题标签： 让页面有一个自己的网页标题 ——>**\<title>\</title>**
- 主体标签： 页面内容基本都放在里面 ——> **\<body>\</body>**  
  
  ![alt text](image.png)

参考：*01-HTML.html 的 2.1*  

创建网页时候一个 ***！*** 可补全基本结构  

- **\<!Doctype html>**  是文档类型声明，告诉browser用哪种HTML版本来解析(HTML5)，写在最前面。
- **\<html lang="en">**  是语言种类定义，zh-CN表示中文，en表示英文。（不影响显示多语言）
- **\<meta charset="utf-8">**  是字符集，便于计算机能够识别各种文字，比如 GBK、UTF-8(万国码) 等。

---

### 2.2 HTML常用标签  
- **标题标签：** \<h1> 到 \<h6>，重要性递减
- **段落标签：** \<p>\</p>
- **换行标签：** \<br>  
- **加粗标签：** \<b>\</b>   or  \<strong>\</strong>
- **斜体标签：** \<i>\</i>   or  \<em>\</em>
- **下划线标签：** \<u>\</u> or  \<ins>\</ins>
- **删除线标签：** \<s>\</s> or  \<del>\</del>
  
![alt text](image-1.png)
参考：*01-HTML.html 的 2.2* 

**\<div> 和 \<span> 标签**  
- \<div>\</div> 是一个大盒子（占一行），一行只有一个div标签
- \<span>\</span> 是一个小盒子，一行可以有多个span标签  

**图像标签**
- **\<img src="image.png" alt="图片说明" title="提示文本" width="100" height="100" border="0">**  
- src属性指定图片的源文件 (必需)
- alt是当图片无法显示时，显示的文字 (可选)
- title是鼠标悬停时显示的文字 (可选)
- width和height属性指定图片的宽度和高度 (可选)
- border属性指定图片的边框宽度 (可选)

**相对路径和绝对路径**
- 相对路径：同级是**直接写**文件名，上一级是**../**，下一级是**/**。
> 比如：
> 1. index.html**同级**的图片是img.png，那么img.png的相对路径是 **img.png**。
> 2. index.html**上一级**的图片是img.png，那么img.png的相对路径是 **../img.png** 。
> 3. index.html**下一级**的图片是img.png，那么img.png的相对路径是 **/img.png** 。

- 绝对路径：就是你的pc的绝对路径，比如："D:/Users/Administrator/Desktop/img.png" 。  
  



**超链接标签**
- \<a href="目标" target="打开方式"> 链接内容 \</a>
- href：指定链接目标（必需），值可以是：
  -  外部网址（需带 http/https，如 "https://baidu.com"）
  -  本地页面路径（如 "page.html"）
  -  锚点（如 现在有一个id为"top"的元素 然后再把href="#top"）
  -  特殊链接（mailto: 邮箱 /tel: 电话）
  -  空链接（#）
  -  下载链接（具体到文件后缀名）
  
- target：指定打开方式
   - _self（默认，当前窗口）
   -  _blank（新窗口）

**其他特殊标签**
![alt text](image-2.png)

---

### 2.3 表格标签  

> 用来展示数据的

- **\<table>\</table>:**   用于定义表格，在最外围。
- **\<tr>\</tr>:** 用于定义行，在表格里面。（table row）
- **\<td>\</td>:** 用于定义单元格，在行里面。（table data）
- **\<th>\</th>:** 用于定义表头单元格，在行里面。(table header) 会居中和加粗 

后续开发用css定义 不太用这些标签  

**表格属性**  
- align：定义表格对齐方式，有 left、center、right 三个值
- border：定义表格边框宽度，默认为""，表示无边框
- cellpadding：定义单元格内边距（单元边沿和内容之间的空白），默认为 1px
- cellspacing：定义单元格间距（单元格之间的空白），默认为 2px
- width：定义表格宽度  

**表格结构标签**
- \<thead>\</thead> 表示表头结构  
- \<tbody>\</tbody> 表示表体结构  

![alt text](image-3.png)

**合并单元格**
- **跨行合并：** 将居于两行的单元格合并成一个单元格，rowspan属性指定合并的行数(从上开始数)
- **跨列合并：** 将居于两列的单元格合并成一个单元格，colspan属性指定合并的列数(从左开始数)

参考：*02-HTML.html*  

---

### 2.4 列表标签
> 用来给元素布局的  

**无序列表：** \<ul>\</ul> 里面放 \<li>\</li> 作为列表元素  （ul里面只能放li，li里面都可以放）
**有序列表：** \<ol\>\</ol\> 里面放 \<li>\</li> 作为列表元素
**定义列表：** \<dl\>\</dl\> 放 \<dt\>\</dt\> 作为列表项，\<dd\>\</dd\> 作为列表项的描述

参考：*02-HTML.html*  

---
### 2.5 表单标签
> 用来收集用户信息  

**\<form>\</form>**  定义表单域
- action 属性：表单提交到的地址
- method 属性：表单提交方式(get/post)
- name 属性：表单名称

**\<input />** 定义输入表单元素 
- type属性：指定输入字段的形式
  ![alt text](image-4.png)

- name 属性：表单元素的名称(单选框和复选框需要相同的name)
- value 属性：输入字段的默认值 or 指定该元素的值
- checked 属性：指定该元素在首次加载时候被选中
- maxlength 属性：指定输入字段的最大长度

**\<label>\</label>** 
- 用于绑定一个表单元素（当点击到这个label时候就自动连接到对应的表单元素），*label的for属性* 对应 *表单元素的id属性*

**\<select>\</select>** 
- 定义下拉列表表单元素，里面用\<option>\</option>定义选项

**\<textarea>**
- 定义文本域表单元素，rows属性定义行数，cols属性定义列数



参考：*02-HTML.html*  

---

## 3.CSS 样式  
> css全称为Cascading Style Sheets，即层叠样式表，也是一种标记语言。  

**语法** 选择器+多条声明（键值对+分号） 写在head标签里面
![alt text](image-5.png)  

### 3.1 选择器  
> 选中特定的标签  

选择器分为**基础选择器**和**复合选择器**  
**基础选择器**包括：**标签选择器**、**类选择器**、**ID选择器**、**通配符选择器**  

**标签选择器：** 使用标签名称作为选择器，比如`<div>`标签，选择器为`div`  
**类选择器：** 使用类属性作为选择器，比如`<div class="box">`标签，选择器为`.box`  
**ID选择器：** 使用ID属性作为选择器，比如`<div id="box">`标签，选择器为`#box`  
**通配符选择器：** 选择所有标签，选择器为`*`  

**注意**
1. 一个标签可以有多个类名，比如 `<div class="box1 box2 box3">`  
2. id选择器只能被标签调用一次，如果有多个标签有相同id，则只被第一个调用
3. 通配符选择器通常用于样式重置，比如`* {margin:0;padding:0;}`  

参考：*03-CSS.html*  

---

### 3.2 字体样式
- **font-family：** 指定字体比如微软雅黑 `font-family: 'Microsoft Yahei','Times New Roman'`  
- **font-size：** 指定字体大小,比如 `font-size: 20px`  
- **font-weight：** 指定字体粗细，比如 `font-weight: bold` （normal、bold、bolder、lighter、number）   
  or 直接指定权重 `font-weight: 700`
- **font-style：** 斜体 `font-style: italic`
- **复合字体样式：** `font: font-style font-weight font-size/line-height font-family`  （不可颠倒顺序，size和famil不可省略）

参考：*03-CSS.html*  

---

### 3.3 文本样式
- **color：** 字体颜色，可以用预定义的颜色，也可以用十六进制和RGB表示
- **text-align：** 文本对齐方式，比如 `text-align: center` （left是左对齐，right是右对齐，center是居中对齐）
- **text-decoration：** 文本修饰，比如 `text-decoration: underline` （underline是下划线，overline是上划线，line-through是删除线，none是不加修饰这个可以让链接去掉下划线）
- **text-indent：** 文本缩进，比如 `text-indent: 2em` （em是相对单位，比如1em等于当前字体的宽度，2em等于当前字体的宽度的2倍）  
  
参考：*03-CSS.html*  

--- 

### 3.4 外部样式表
> 外部样式表（External Style Sheet）是把样式表保存在单独的文件中，然后通过 `<link>` 标签引入，从而实现样式的复用。

在HTML的 **\<head>** 当中用 **\<link>** 标签引入CSS文件，比如：` <link rel="stylesheet" href="style.css"> `  

![alt text](image-6.png)
