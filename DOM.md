
## API

### 选择符API

#### querySelector()

接收一个css选择符，返回匹配的第一个元素

```js
var body = document.querySelector("body");

var myDiv = document.querySelector("#myDiv");

var selected = document.querySelector(".selected");

var img = document.body.querySelector("img.button");

```

#### querySelectorAll()

接受一个css选择符，返回一个NodeList的实例

```js
var ems = document.getElementById("myDiv").querySelectorAll("em");

var selecteds = document.querySelectorAll(".selected");

var strongs = document.querySelectorAll("p strong");
```

#### matchesSelector()

接收一个css选择符，如果调用元素匹配，返回true

```js
if (document.body.matchesSelector("body.page1")) {
  // true ...
}
```
### 元素遍历

* childElementCount: 返回子元素(不包括文本节点和注释)的个数
* firstElementChild: 指向第一个子元素; firstChild的元素版
* lastElementChild: 指向最后一个子元素; lastChild的元素版
* previousElementSibling: 指向前一个同辈元素; previousSibling的元素版
* nextElementSibling: 指向后一个同辈元素; nextSibling的元素版


### HTML5

#### getElementsByClassName()

接收一个或多个类名的字符串，返回带有指定类的所有元素的NodeList。类名先后顺序不重要

```js
var allCurrentUsername = document.getElementsByClassName("username current");

var selected = document.getElementById("myDiv").getElementsByClassName("selected");
```

#### classList

* add(value): 添加;
* contains(value): 是否存在，true or false
* remove(value): 删除和;
* toggle(value): 有就删，无就加;

```js
div.classList.remove("user");
div.classList.add("current");
div.classList.toggle("user");

if (div.classList.contains("bd") &&　!div.classList.contains("disabled")) {
   // 执行操作
   
}

for (var i = 0, len=div.classList.length;i < len; i++) {
  doSomething(div.classList[i]);
}
```

#### document.activeElement

引用DOM中当前获得了焦点的元素

```js
var button = document.getElementById("myButton");
button.focus();
alert(document.activeElement === button) //true
```
#### document.hasFocus()

确定文档是否获得了焦点

```js
var button = document.getElementById("myButton");
button.focus();
alert(document.hasFocus()) //true
```