#README.md 测试文件
# JavaScript

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    //头文件引入
    <script src="./test.js"></script>
    <title>Document</title>
</head>

<body>
    //内部写入
    <script>alert("猪鼻把")
        //两个script标签中间不许写内容
    </script>

    //内联JavaScript写法，主要用于vue
    <input name="btn" type="button" value="弹出消息框" onclick="javascript:alert('我是你爷');" />
</body>
</html>
```



## 字面量

概念：在计算机科学中，字面量是在计算机中描述 事/物

比如：我们的工资是：1000，此时1000就是数字字面量；

​			'黑马程序员' 字符串字面量；

​			还有例如[]数组字面量，{}对象字面量 等等；

就像Java中的变量的值；

# 变量

```html
//变量的声明和赋值
let age = 18
const 关键字来定义一个常量，不可变

<body>
    <script>
        let age = prompt('你也私募了？')
        let name = '我是你爷'
        console.log(age)
        console.log(name)
    </script>
</body>

```

注意：var也可以声明变量，但是：

1、可以先使用再声明

2、var声明过的变量可以反复声明

3、没有比如变量提升，全局变量，极块作用域等功能；

所以不推荐使用

## JavaScript语句

 JavaScript 语句向浏览器发出的命令。语句的作用是告诉浏览器该做什么。 

```html
<body>

    <h1>我的第一个 Web 页面</h1>

    <p id="demo">我的第一个段落</p>

    <button id="button" onclick="myfunction()">点我</button>
    <script>
        function myfunction() {
            document.getElementById('demo').innerHTML = "yes"
            document.getElementById('button').innerHTML = "yes"
        }
    </script>
</body>

//点下按钮 功能内的两条语句可以向html文档内写入字符串yes；

//可以在代码中使用反斜杠对代码行进行换行
document.write("你好 \
世界!");
```

## JavaScript 数据类型

值类型(基本类型)：字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）、Symbol。

引用数据类型（对象类型）：对象(Object)、数组(Array)、函数(Function)，还有两个特殊的对象：正则（RegExp）和日期（Date）。

JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。 

```html
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;

-----------------------
Javascript拥有动态类型，这意味着相同的变量可用作不同的类型：
var x;               // x 为 undefined
var x = 5;           // 现在 x 为数字
var x = "John";      // 现在 x 为字符串
```

## JavaScript 对象

```html
//在 JavaScript中，几乎所有的事物都是对象。
//对象也是一个变量，但对象可以包含多个值（多个变量），每个值以 name:value 对呈现。
//定义对象
let car = {name:"Fiat", model:500, color:"white"};


<body>
  <button id="demo" onclick="abc()" )">点我</button>
</body>

<script>
  function abc() {
    for (let i = 1; i < 10; i++) {
      for (let j = 1; j <= i; j++) {
        document.write(i + "*" + j + "=" + i * j + "&nbsp;&nbsp;");
      }
      document.write("<br>");
    }
  }
</script>
```

## JavaScript 函数

 函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块。 

```html
//无参函数
<script>
  function abc() {
    for (let i = 1; i < 10; i++) {
      for (let j = 1; j <= i; j++) {
        document.write(i + "*" + j + "=" + i * j + "&nbsp;&nbsp;");
      }
      document.write("<br>");
    }
  }
</script>

//有参函数
<script>
function myFunction(name,job){
    alert("Welcome " + name + ", the " + job);
}
</script>

//带有返回值的函数
function myFunction()
{
    var x=5;
    return x;
}
```

##         **事件**  

| **名称**    | **说明**                   |
| ----------- | -------------------------- |
| onload      | 一个页面或一幅图像完成加载 |
| onlick      | 鼠标单击某个对象           |
| onmouseover | 鼠标指导移到某元素上       |
| onkeydown   | 某个键盘按键被按下         |
| onchange    | 域的内容被改变             |

#      JavaScript操作BOM对象

## BOM模型

BOM：浏览器对象模型（Browser Object Model）

BOM提供了独立于内容的、可以与浏览器窗口进行互动的对象结构

##      window对象  

| **属性名称** | **说   明**                       |
| ------------ | --------------------------------- |
| **history**  | 有关客户访问过的URL的信息         |
| **location** | **有关当前**  **URL**  **的信息** |

##      window对象的常用方法



| **方法名称**   | **说   明**                                                  |
| -------------- | ------------------------------------------------------------ |
| **prompt(  )** | **显示可提示用户输入的对话框**                               |
| **alert(  )**  | 显示带有一个提示信息和一个确定按钮的警示框                   |
| confirm( )     | **显示一带有提示信息、确定和取消按钮的对话框**               |
| **close(  )**  | **关闭浏览器窗口**                                           |
| **open(  )**   | **打开一个新的浏览器窗口，加载给定**  **URL**  **所指定的文档** |
| setTimeout( )  | **在指定的毫秒数后调用函数或计算表达式**                     |
| setInterval()  | **按照指定的周期（以毫秒计）来调用函数或表达式**             |

##      history对象

| **名称**      | **说   明**                                  |
| ------------- | -------------------------------------------- |
| **back()**    | **加载** **history** 对象列表中的前一个URL   |
| **forward()** | **加载** **history** 对象列表中的下一个URL   |
| **go()**      | **加载** **history** 对象列表中的某个具体URL |

##      **location**对象  

**常用属性**:

| **名称**     | **说   明**                       |
| ------------ | --------------------------------- |
| **host**     | 设置或返回主机名和当前URL的端口号 |
| **hostname** | 设置或返回当前URL的主机名         |
| **href**     | 设置或返回完整的URL               |

**常用方法**

| **名称**      | **说   明**                |
| ------------- | -------------------------- |
| **reload()**  | **重新加载当前文档**       |
| **replace()** | **用新的文档替换当前文档** |

##      **Document对象**  

**常用属性**

| **名称**     | **说   明**               |
| ------------ | ------------------------- |
| **referrer** | **返回载入当前文档的URL** |
| **URL**      | **返回当前文档的URL**     |

常用方法

| **名称**                   | **说   明**                                  |
| -------------------------- | -------------------------------------------- |
| **getElementById()**       | **返回对拥有指定id的第一个对象的引用**       |
| **getElementsByName()**    | **返回带有指定名称的对象的集合**             |
| **getElementsByTagName()** | **返回带有指定标签名的对象的集合**           |
| **write()**                | **向文档写文本、HTML表达式或JavaScript代码** |

##      **JavaScript内置对象**  

**Array：用于在单独的变量名中存储一系列的值**

**String：用于支持对字符串的处理**

**Math**：用于执行常用的数学任务，它包含了若干个数字常量和函数

**Date：用于操作日期和时间**

**常用方法**

| **方法**          | **说 明**                                                  |
| ----------------- | ---------------------------------------------------------- |
| **getDate()**     | **返回** **Date**对象的一个月中的每一天，其值介于1～31之间 |
| **getDay()**      | **返回** **Date** 对象的星期中的每一天，其值介于0～6之间   |
| **getHours()**    | **返回** **Date** 对象的小时数，其值介于0～23之间          |
| **getMinutes()**  | **返回** **Date** **对象的分钟数，其值介于0～59之间**      |
| **getSeconds()**  | **返回** **Date** 对象的秒数，其值介于0～59之间            |
| **getMonth()**    | **返回** **Date** **对象的月份，其值介于0～11之间**        |
| **getFullYear()** | **返回** **Date** **对象的年份，其值为4位数                |
| **getTime()**     | 返回自某一时刻（1970年1月1日）以来的毫秒数                 |

​     **定时函数**  ：

**setTimeout()**

setTimeout("调用的函数",等待的毫秒数)

**setInterval**()

**setInterval("调用的函数",间隔的毫秒数)**

​     **清除函数**  ：

**clearTimeout**()

**clearInterval** **()**

#      **JavaScript操作DOM对象**  

##      **DOM：Document Object Model**  

**节点属性**：

| **属性名称**    | **描述**                                                   |
| --------------- | ---------------------------------------------------------- |
| parentNode      | 返回节点的父节点                                           |
| childNodes      | 返回子节点集合，childNodes[i]                              |
| firstChild      | 返回节点的第一个子节点，最普遍的用法是访问该元素的文本节点 |
| lastChild       | 返回节点的最后一个子节点                                   |
| nextSibling     | 下一个节点                                                 |
| previousSibling | 上一个节点                                                 |

element属性：

| **属性名称**           | **描述**                                                   |
| ---------------------- | ---------------------------------------------------------- |
| firstElementChild      | 返回节点的第一个子节点，最普遍的用法是访问该元素的文本节点 |
| lastElementChild       | 返回节点的最后一个子节点                                   |
| nextElementSibling     | 下一个节点                                                 |
| previousElementSibling | 上一个节点                                                 |

​     **节点信息**  ：

**nodeName：节点名称**

**nodeValue：节点值**

**nodeType：节点类型**

| **节点类型** | **NodeType****值** |
| ------------ | ------------------ |
| 元素element  | 1                  |
| 属性attr     | 2                  |
| 文本text     | 3                  |
| 注释comments | 8                  |
| 文档document | 9                  |

​     **操作节点的属性**  

**getAttribute("属性名")**

**setAttribute("属性名","属性值")**
