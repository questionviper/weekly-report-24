## 网页
网站是指在因特网上根据一定的规则，使用HTML等制作的用于展示特定内容相关的网页集合
网页时网站中的一页，通常是HTML格式的文件，它主要通过浏览器来解析阅读。它是由网页元素组成的，这些元素利用html标签描述出来，然后通过浏览器解析并显示给用户
网页是构成网站的基本元素，它通常由图片、链接、文字、声音、视频等元素组成。通常我们看到的网页常以.htm或者.html后缀结尾的文件，俗称HTML文件
#### HTML
HTML指的是超文本标记语言（Hyper Text Markup Language），它是用来描述网页的一种语言。所谓超文本，就是它不仅可以在文本层面上进行内容编辑，也可以加入图片、声音、动画、多媒体等内容，还可以从一个文件跳转到另一个文件，与世界各地主机的文件连接（超级链接文本）
#### 浏览器内核
浏览器内核/渲染引擎：负责读取网页内容，整理讯息，计算网页的显示方式并显示页面
Trident：IE，360，百度
Gecko：火狐
Webkit：Safari
Blink：chrome，opera（Blink其实是Webkit的分支）
#### Web标准
Web标准是W3C组织（万维网联盟）和其他标准化组织制定的一系列标准的集合。浏览器不同，它们显示的页面或者排版就有可能有些许差异，遵循Web标准除了可以让不同的开发人员写出的页面更标准、更统一，而且还能让Web发展前景更广阔，可以被更广泛的设备访问，更容易被搜索引擎搜索，还可以降低网站流量费用，使网站更易于维护并提高页面浏览速度
#### Web标准的构成
主要包括结构、表现和行为
结构：结构用于对页面元素进行整理和分类，主要是HTML
表现：表现用于设置页面元素的版式、颜色、大小等外观样式，主要是CSS
行为：行为指王爷模型的定义以及交互的编写，主要是JS
Web标准提倡结构、样式、行为相分离，就是说结构就写在HTML文件中，表现就写在CSS文件中，行为就写在JS文件中。在这三者中，最基础的结构是最重要的
## HTML规范
#### 基本语法
HTML标签是由尖括号包围的关键词，HTML标签一般是成对出现的，我们成为双标签。标签对中的第一个叫开始标签，第二个叫结束标签。有些特殊的标签必须是单个标签，比如
，称之为单标签
双标签可以分为两类：包含关系（父子关系）和并列关系
#### 基本结构
每个网页都会有一个基本的结构标签（骨架标签），页面内容也是在这些基本标签上写
HTML标签：页面中最大的标签，我们称之为根标签
文档头部head：在head标签中我们必须要设置title标签
文档标题title：让页面拥有一个属于自己的网页标题
文档主体body：该元素包含文档的所有内容，页面内容基本都是放到body标签里面的
#### 网页开发工具
文档类型声明标签：作用就是告诉浏览器使用哪种HTML版本，`<!DOCTYPE html>`指我们使用HTML5显示页面。它声明位于文档最前面的位置，在HTML标签之前，并且它不是一个HTML的标签，它是文档类型声明标签
html的lang属性：用来定义当前文档显示的语言，en指英语，zh-CN指中文，不过，就算定义成英文网页当然也可以显示中文。主要是给浏览器和搜索引擎用
字符集charset：在head标签内，通过<meta>标签的charset属性来规定HTML文档应该使用哪种字符编码，meta是单标签`<meta cahrset="UTF-8" />`，常用的有GB2312、BIG5、GBK和UTF-8（万国码）
#### 常用标签
**标题**：<h1> - <h6>，head，依据重要性递减
**段落**：<p>，用于定义段落，可以把文字有条理地显示出来，分段显示，paragraph
**换行**：
，让某段文本强制换行显示，break，是个单标签。它和段落不一样，段落之间会插入一些垂直的间距
**文本格式化**：<strong>加粗<b>语义较弱、<em>斜体<i>语义较弱、<del>删除线<s>语义较弱、<ins>下划线<u>语义较弱。可以突出重要性。
**盒子**：<div>和<span>，没有语义。division分割一行只能放一个，是大盒子；span跨距，一行可以放多个span，是小盒子
**图像**：<img src="URL" />，src是img标签必须要有的属性，它用于指定图像文件的路径和文件名；alt替换文本，当图像不能显示的时候出现的文字；title提示文本，鼠标放到图像上提示的文字；width宽度，height高度，border边框。图像标签拥有多个属性，必须写在标签名的后面。属性之间不分先后，其间均以空格隔开。采取键值对的格式
**路径**：同一级路径`./`或留空都是同一级路径，下一级路径`/`，上一级路径`.../`。绝对路径比较少用，因为每个人电脑内容结构不一样。绝对路径分隔用斜杠`\`，相对路径或网络绝对地址用反斜杠`/`
**超链接**：<a href="URL">，从一个页面链接到另一个页面，anchor锚。href用于指定链接目标的url地址（必须属性），target属性用于指定链接页面的打开方式，其中`_self`为默认值（就是在当前窗口打开），`_blank`是在新窗口中打开
**内部链接**：把<a>标签的href属性内容定为内部页面名称即可，如`<a href="index.html"></a>`。如果当前没有确定的链接目标，可以指定href为`#`
**下载链接**：如果href里面是个文件或者压缩包，会下载这个文件
**网页元素链接**：网页中的各种网页元素，如文本、图像、表格、音频、视频等都可以添加超链接。`<a href="URL"><img src=""></a>`这样就会给图片添加超链接
**锚点链接**：点击链接可以快速定位到页面的某个位置。在链接href中，设置属性为#名字的形式，点击它就会找到id属性为#名字的目标位置，如`<a href="#intro">123</a>`就会找到页面中`<div id="intro">123</div>`的位置
**注释标签**：`<!--`开头`-->`结束。在HTML文档中添加的一些便于阅读理解但又不需要显示在页面中的注释文字
**特殊字符**：像空格字符，小于大于号字符等不方便使用的特殊字符可以用字符代码来替代

| **字符** | **描述** | **代码** |
| --- | --- | --- |
|   | 空格 | &nbsp; |
| < | 小于号 | &lt; |
| > | 大于号 | &gt; |
| & | 和 | &amp; |
| ￥ | 人民币 | &yen; |
| © | 版权 | &copy; |
| ® | 注册商标 | &reg; |
| ° | 摄氏度 | &deg; |
| ± | 正负号 | &plusmn; |
| × | 乘 | &times; |
| ÷ | 除 | &divide; |
| ² | 平方 | &sup2; |
| ³ | 立方 | &sup3; |

#### 表格标签
表格主要用来显示、展示数据，它可以让数据显示的非常规正，可读性强。table用于定义表格的标签，tr标签定义表格中的行且嵌套在table标签中，td标签（table data）定义表格中的单元格，嵌套在tr标签中。
表头单元格标签：表格的第一行或者第一列，用th（table head）表示表格的表头部分
表格结构标签：为了更好地表示表格的语义，可以把表格分割成表头和表格主题两个部分，分别是thead和tbody
合并单元格：跨行合并属性`rowspan="合并的个数"`，跨列合并`colspan="合并的个数"`（跨行是竖着合并，跨列是横着合并），如果我们跨行就在上侧单元格写合并代码，如果是跨列则在左侧单元格写合并代码。合并后要将多余的单元格删除，比如一行有三个单元格，如果我们把第一个和第二个合并（也就是给第一个写`colspan="2"`），那我们就要把第三个td删除
列表标签：整洁整齐有序，分为无序列表、有序列表和自定义列表。

- 无序列表ul一般以项目符号呈现列表项，而列表项使用li标签定义，各个列表项之间是并列的，ul里面只能放li，但是li就可以容纳任何元素了
- 有序列表ol用于显示数字排序，每个小选项还是用li
- 自定义列表dl与dt（定义项目/名字）和dd（描述项目）一起使用。dt和dd的个数没有限制，但是一般一个dt对应多个dd
#### 表单标签
收集用户信息。一个完整的表单通常由表单域、表单控件（表单元素）和提示信息三个部分组成
表单域form实现用户信息的收集和传递，会把它范围内的表单元素信息提交给服务器。`<form action="URL" method="提交方式" name="表单域名称">表单元素控件</form>`。action里面指定接收并处理表单数据的服务器程序的url地址，method指定提交表单数据的方式，有get和post；name指定表单名称来区分不同的表单域
表单元素有input输入型，select下拉型，textarea文本域型。`<input type="" />`，其中，type属性有：

| **属性值** | **描述** |
| --- | --- |
| button | 定义点击按钮（一般绑定脚本） |
| checkbox | 定义复选框 |
| file | 输入字段和浏览按钮，供文件上传 |
| hidden | 隐藏输入字段 |
| image | 图像形式的提交按钮 |
| password | 密码字段，内容将会被隐藏 |
| radio | 单选按钮 |
| reset | 重置按钮，会清除表单中的数据 |
| submit | 提交按钮，会把表单数据发送到服务器 |
| text | 单行输入字段，默认宽度20字符 |

给单选、复选等添加相同的name属性才会发挥单选和复选的作用，如果想要数据发送到后台，我们还需要给标签添加value元素（value元素会在文本框等内部显示出来）。给选择框元素添加checked会规定这个input元素加载时直接被选中。maxlength元素可以规定字符的最大长度
标注标签label：label可以绑定一个表单元素，当我们点击label标签内的文本的时候，浏览器会自动将焦点转到或者直接选择对应的表单元素，可以增加用户体验。label中要加特有的for属性来对应表单的id属性，如`<label for="p1"></label>`和`<input id="p1" type="radio">`的绑定、
下拉列表：select标签可以给出多个选项，并且可以节约页面空间。父标签select，子标签多个option。当option中定义属性`selected="selected"`时，表示此为默认选项
文本框：textarea可以提供给用户来输入较多的内容，这种情况我们不能使用文本框表单input-text而是用textarea。可以输入更多的文字，常见于留言板，评论等。属性`cols="行字符数"`和`rows="行数"`，一般不使用，实际开发用css来改变文本框大小
