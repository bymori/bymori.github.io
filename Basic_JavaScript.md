<!--
 * @Author: by_mori
 * @website: https://www.ioinn.cn
 * @Github: https://github.com/bymori
 * @LastEditors: by_mori
 * @Date: 2019-05-08 16:09:18
 * @LastEditTime: 2019-05-11 17:49:36
 -->
[toc]
## freeCode Camp JavaScript
### 注释
JavaScript中的注释方式有以下两种：
单行注释使用` // `

`// This is an in-line comment.`
多行注释以`/*开始，用*/`来结束
```JavaScript
/* This is a 
   multi-line comment */
```

### 变量
JavaScript提供七种不同的`data types`(数据类型)，它们是`undefined`（未定义）, `null`（空）, `boolean`（布尔型）, `string`（字符串）, `symbol`(符号), `number`（数字）,  `object`（对象）

#### 声明变量
创建或者 `declare`（声明）一个变量
`var ourName;`
上面代码的意思是创建一个名为`ourName`的`variable`（变量），在JavaScript中我们使用`分号`来结束一段声明。

`Variable` （变量）的名字可以由数字、字母、`$` 或者 `_`组成，但是不能包含空格或者以数字为首。

#### 赋值变量
通过`assignment`(分配)操作符把一个值存储到变量中
赋值过程是`从右到左`进行的。所有` = `操作符右边的值都会被赋到左边的变量。
```JavaScript
myVar = 5;
myNum = myVar;
```
数值` 5 `被赋给变量` myVar `中， 然后变量` myVar `又赋给变量` myNum `，这样子` myNum `变量中的值也是` 5 `了。

#### 变量赋值初始值
```JavaScript
var myVar = 0;
```
创建一个名为` myVar `的变量并指定一个初始值` 0`

#### 未初始化的变量
当 JavaScript 中的变量被声明的时候，程序内部会给它一个初始值 `undefined`。当你对一个值为 `undefined` 的变量进行运算操作的时候，算出来的结果将会是` NaN，NaN `的意思是` "Not a Number"(不是数字)`。当你用一个没有` 定义 `的变量来做字符串连接操作的时候，它会如实的输出`"undefined"(未定义)`

```JavaScript
// 初始化变量
var a=5;
var b=10;
var c="I am a";

a = a + 1;
b = b + 5;
c = c + " String!";
```

#### 变量中的大小写敏感度
在 JavaScript 中所有的变量都是大小写敏感的。这意味着你要区别对待大写字母和小写字母。

`MYVAR`与`MyVar`和`myvar` 是截然不同的变量。这就有可能导致多个截然不同的变量却有着有相似的名字。正是由于以上原因所以强烈地建议你, 不要 使用这一特性。（以免给自己带来麻烦）

**最佳实践**
使用` 驼峰命名法 `来书写一个 Javascript 变量，在 `驼峰命名法` 中，变量名的第一个单词的首写字母小写，后面的单词的第一个字母大写。

```JavaScript
var someVariable;
var anotherVariableName;
var thisVariableNameIsTooLong;
```

### JavaScript运算符
JavaScript 中使用` + `来做加法运算。

```JavaScript
myVar = 5 + 10; // 等于 15
```

JavaScript 中使用` - `来做减法运算。
```JavaScript
myVar = 12 - 6; // 等于 6
```

JavaScript 使用这个` * `符号来让两个数字相乘。
```JavaScript
myVar = 13 * 13; // 把 169 赋值给 myVar
```

JavaScript 中使用` / `符号做除法运算。
```JavaScript
myVar = 16 / 2; // 把 8 赋值给 myVar
```

#### 自增 自减数字
使用` ++ `,` -- `,我们可以很容易地对变量进行`+1`或者`-1`运算。

`i++;`等效于`i = i + 1;`
`i--;`等效于`i = i - 1;`
`i++;`,`i--;`这种写法，省去了书写`=`符号的必要

```JavaScript
var myVar = 87;
myVar++;

var myVar = 11;
myVar --;
```

#### 小数(浮点数)
我们也可以把小数存储到变量中。小数也被称作` 浮点数 `

不是所有的实数都可以用` 浮点数 `来表示。因为可能存在四舍五入的错误，[详情在这儿](https://en.wikipedia.org/wiki/Floating_point#Accuracy_problems)
```JavaScript
var myDecimal =5.7;
```

#### 小数计算

```JavaScript
var product = 2.0 * 2.5;  //小数乘法
```

```JavaScript
var quotient = 4.4 / 2.0;  //小数除法
```
#### 取余（用%号）

取余只能整数除以整数，若除数比被除数大，直接除数就是余数，若除数比被除数小，被除数就除以除数直到剩下的数比除数小，则这个数就是余数，而且注意余数的符号要与被除数的符号一致
```JavaScript
var remainder=11%3;
```

#### Plus Equals +=计算

通常通过赋值来修改变量的内容。请记住，先计算`=`右边，然后把计算出来的结果赋给左边。
```JavaScript
myVar = myVar + 5;
```
以上是最常见的运算赋值语句，先运算、再赋值。
还有一类操作符是一步到位既做运算也赋值的。
这类操作符的其中一种就是` += `运算符。
`myVar += 5; `也是把数值` 5 `加到变量` myVar`上

```JavaScript
var a = 3;
var b = 17;
var c = 12;

a += 12;
b += 9;
c += 7;
```

#### Minus Equals -=计算

与 += 操作符类似，-= 操作符用来对一个变量进行减法赋值操作。
```JavaScript
myVar = myVar - 5;
```
将会从变量` myVar `中减去数值` 5`。也可以写成这种形式：`myVar -= 5;`

```JavaScript
var a = 11;
var b = 9;
var c = 3;

a -= 6;
b -= 15;
c -= 1;
```

#### Times Equals *=计算
`*= `操作符是让变量与一个数相乘并赋值。
```JavaScript
myVar = myVar * 5;
```
将会把变量` myVar `与数值`5`相乘。也可以写作这样的形式:`myVar *= 5;`

```JavaScript
var a = 5;
var b = 12;
var c = 4.6;

a *= 5;
b *= 3;
c *= 10;
```

#### Divided by Equals /=计算
`/= `操作符是让变量与另一个数相除并赋值。
```JavaScript
myVar = myVar / 5;
```
会把变量` myVar `的值除于` 5` 等价于:`myVar /= 5;`

```JavaScript
var a = 48;
var b = 108;
var c = 33;

a /= 12;
b /= 4;
c /= 11;
```

### 应用
#### 摄氏度转华氏度
从`Celsius`摄氏度转换为`Fahrenheit`华氏度的算法是：摄氏度的温度乘于9除于5，再加上32。

创建一个变量` fahrenheit`，然后计算出摄氏度对应的华氏度。

```JavaScript
function convert(celsius) {
  // 请把你的代码写在这条注释以下
  var Fahrenheit=celsius*9/5+32; //华氏度
  // 请把你的代码写在这条注释以上
    return Fahrenheit;
}
convert(10);  // 你可以修改这一行来测试你的代码
```

#### 造句函数
通过使用提供的变量参数：名词`myNoun`、形容词`myAdjective`、动词`myVerb`、副词`myAdverb`，来创建一个新的句子` result`。

请注意，在英文中，句中的单词是必须用空格来分隔的

举个例子，如果名词为` "dog"`，形容词为` "big"`，动词为` "run"`，副词为`"quickly"`，那么函数返回值为` "dog big run quickly" `就是没问题的

此外，为了句子通顺，你可以在包含所有传入单词的前提下自己添加一些其他单词。对于上面的例子，函数返回值为` "That big brown dog just run quickly" `也是没问题的

```JavaScript
function wordBlanks(myNoun, myAdjective, myVerb, myAdverb) {
  var result = "";
  // 请把你的代码写在这条注释以下
  result = myNoun + " " + myAdjective + " " + myVerb +  " " + myAdverb;

  // 请把你的代码写在这条注释以上
  return result;
}

wordBlanks("dog", "big", "ran", "quickly");  // 你可以修改这一行来测试你的代码
```

### 声明字符串变量
`var myName = "your name";`

`"your name" `被称作` 字符串`。 字符串是用单或双引号包裹起来的一连串的零个或多个字符。

```JavaScript
// 举例
var firstName = "Alan";
var lastName = "Turing";

// 请把你的代码写在这条注释以下
var myFirstName = "名";
var myLastName ="姓";
```

### 字符串转义
当你定义一个字符串必须要用单引号或双引号来包裹它。那么当你需要在字符串中使用一个:` " `或者` ' `时该怎么办呢?

在 JavaScript 中，你可以通过在引号前面使用` 反斜杠 (\) `来转义引号。
```JavaScript
var sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```
这标志着提醒 JavaScript 单引号或双引号并不是字符串的结尾，而是出现在字符串内的字符。所以，如果你要打印字符串到控制台，你将得到：
```JavaScript
Alan said, "Peter is learning JavaScript".
```

```JavaScript
var myStr="I am a \"double quoted\" string inside \"double quotes\""; // 请修改这一行
```

### 单引号引用字符串
在 JavaScript 中的` 字符串 `要用单引号或双引号来包裹它，只要你在开始和结束都使用相同类型的引号，单引号和双引号的功能在JavaScript中是相同的。
```JavaScript
"This string has \"double quotes\" in it"
```
当我们需要在字符串中使用与开头结尾相同的引号时，我们需要对引号进行` 转义 `。如果你有很多双引号的字符串，使用转义字符可能导致难以阅读。这时候可以使用单引号。
```JavaScript
'This string has "double quotes" in it. And "probably" lots of them.'
```

```JavaScript
var myStr = '<a href="http://www.ioinn.cn" target="_blank">Link</a>';
```

### 字符串转义序列
引号不是字符串中唯一的可以被转义字符。下面是常见的转义序列列表:

|Code|Output|
|--------|--------|
|\\' |单引号|
|\\"	|双引号|
|\\\	|反斜杠符|
|\n	|换行符|
|\r	|回车符|
|\t	|制表符|
|\b	|退格符|
|\f	|换页符|

```JavaScript
var myStr="\\ \t \b \r \n"; // 请修改这一行
```

### Plus Operator 字符串拼接
在 JavaScript 中，当 + 操作符与 字符串 一起使用的时候，它被称作 连接 操作符。你可以通过和其他字符串连接 来创建一个新的字符串。

```JavaScript
'My name is Alan,' + ' I concatenate.'
```
**注意**
当心空格。连接操作不会添加两个字符串之外的空格，所以想加上空格的话，你需要自己在字符串里面添加。

```JavaScript
// 举例
var ourStr = "I come first. " + "I come second.";

// 请只修改这条注释以下的代码

var myStr="This is the start. " +'This is the end.';
```

### Plus Equals Operator +=拼接字符串
我们还可以使用` += `运算符来` 连接 `字符串到现有字符串的结尾。对于那些非常长的字符串来说，这一操作是非常有用的。

```JavaScript
// 举例
var ourStr = "I come first. ";
    ourStr += "I come second.";

// 请只修改这条注释以下的代码

var myStr = "This is the first sentence. ";
    myStr += "This is the second sentence.";
```

### 用变量构造字符串
通过使用连接运算符` + `，你可以插入一个或多个变量来组成一个字符串。
```JavaScript
// 举例
var ourName = "Free Code Camp";
var ourStr = "Hello, our name is " + ourName + ", how are you?";

// 请只修改这条注释以下的代码
var myName = "myNameme";
var myStr = "this " + myName + " ioinn.cn";
```

### 将变量附加到字符串
我们不仅可以创建出多行的字符串，还可以使用加等号`(+=)`运算符来追加变量到字符串上。
```JavaScript
// 举例
var anAdjective = "awesome!";
var ourStr = "Free Code Camp is ";
ourStr += anAdjective;

// 请只修改这条注释以下的代码

var someAdjective = "ioinn.cn";
var myStr = "Learning to code is ";
myStr += someAdjective;
```

### 检查字符串的长度

你可以通过在字符串变量或字符串后面写上` .length `来获得字符串变量` 字符串 `值的长度。
```JavaScript
"Alan Peter".length; // 10
```
例如，我们创建了一个变量` var firstName = "Charles"`，我们就可以通过使用` firstName.length `来获得 "Charles" `字符串的长度。

```JavaScript
// 举例
var firstNameLength = 0;
var firstName = "Adaaaaaa";

firstNameLength = firstName.length;

// 初始化变量
var lastNameLength = 0;
var lastName = "Lovelace";

// 请只修改这条注释以下的代码

lastNameLength = lastName.length;
```

### 使用括号表示法查找字符串中的第一个字符

`[]`叫中括号，`{}`叫大括号，`()`叫小括号。

JavaScript中只有字符串类型，没有字符类型。那么如何获取到字符串中的某个字符呢？

我们通过`[索引] `来获得对应的字符。

大多数现代编程语言，如JavaScript，不同于人类从1开始计数。它们是`从0开始`计数，这被称为` 基于零 `的索引。

例如, 在单词 `"Charles" `中索引0上的字符为 "C"，所以在` var firstName = "Charles" `中，你可以使用` firstName[0] `来获得第一个位置上的字符。

```JavaScript
// 举例
var firstLetterOfFirstName = "";
var firstName = "Ada";

firstLetterOfFirstName = firstName[0];

// 初始化变量
var firstLetterOfLastName = "";
var lastName = "Lovelace";

// 请只修改这条注释以下的代码
firstLetterOfLastName = lastName[0];
```

### 理解字符串不变性

理解字符串的不可变性！当你搞懂不可变性后`immutable.js`对于你就是小菜一碟了。

在 JavaScript 中，`字符串 `的值是` 不可变的`，这意味着一旦字符串被创建就不能被改变。

例如，下面的代码：
```JavaScript
var myStr = "Bob";
myStr[0] = "J";
```
是不会把变量` myStr `的值改变成 "Job" 的，因为变量` myStr `是不可变的。注意，这 并不 意味着` myStr `永远不能被改变，只是字符串字面量` string literal `的各个字符不能被改变。改变` myStr `中的唯一方法是重新给它赋一个值，就像这样：
```JavaScript
var myStr = "Bob";
myStr = "Job";
```
```JavaScript
// 初始化变量
var myStr = "Jello World";

// 请只修改这条注释以下的代码

myStr = "Hello World"; // 请修改这一行
```

### 使用括号表示法查找字符串中的第N个字符
你也可以使用` [索引]`来获得一个字符串中的其他位置的字符。

请记住，程序是从` 0 `开始计数，所以获取第一个字符实际上是`[0]`。
```JavaScript
// 举例
var firstName = "Ada";
var secondLetterOfFirstName = firstName[1];

// 初始化变量
var lastName = "Lovelace";

// 请只修改这条注释以下的代码
var thirdLetterOfLastName = lastName[2];
```

### 使用括号表示法查找字符串中的最后一个字符
为了得到一个字符串的最后一个字符，你可以用`[字符串的长度减去一]`。

例如，在` var firstName = "Charles" `中，你可以这样操作 `firstName[firstName.length - 1] `来得到字符串的最后的一个字符。

```JavaScript
// 举例
var firstName = "Ada";
var lastLetterOfFirstName = firstName[firstName.length - 1];

// 初始化变量
var lastName = "Lovelace";

// 请只修改这条注释以下的代码
var lastLetterOfLastName = lastName[lastName.length-1];
```

### 使用括号表示法在字符串中查找倒数第N个字符

我们既可以获取字符串的最后一个字符，也可以用获取字符串的倒数第N个字符。

例如，你可以这样` firstName[firstName.length - 3]` 操作来获得` var firstName = "Charles" `字符串中的倒数第三个字符。

```JavaScript
// 举例
var firstName = "Ada";
var thirdToLastLetterOfFirstName = firstName[firstName.length - 3];

// 初始化变量
var lastName = "Lovelace";

// 请只修改这条注释以下的代码
var secondToLastLetterOfLastName = lastName[lastName.length -2];
```

### 使用JavaScript数组在一个变量中存储多个值
使用 `数组`，我们可以在一个地方存储多个数据。

你以左方括号`[开始定义一个数组，以右方括号]`结束定义，并把每个条目之间用逗号隔开，就像这样：`
var sandwich = ["peanut butter", "jelly", "bread"]。`

```JavaScript
// 举例
var array = ["John", 23];

// 请只修改这条注释以下的代码
var myArray = ["ioinn",23333];
```

### 将一个Array(数组)嵌套在另一个Array(数组)中
你也可以在数组中包含其他数组，就像这样: `[["Bulls", 23], ["White Sox", 45]]`。这被称为一个 多维数组。
```JavaScript
// 举例
var ourArray = [["the universe", 42], ["everything", 101010]];

// 请只修改这条注释以下的代码
var myArray = [["ioinn.cn",233],["blog.ioinn.cn",2444]];
```

### 使用索引访问数组数据

我们可以像操作字符串一样通过数组索引`[index]`来访问数组中的数据。

数组索引的使用与字符串索引一样，不同的是，通过字符串的索引得到的是一个字符，通过数组索引得到的是一个条目。与字符串类似，数组也是` 基于零 `的索引，因此数组的第一个元素的索引是` 0`。

```JavaScript
// 举例
var ourArray = [1,2,3];
var ourData = ourArray[0]; // ourData 的值为 1

// 初始化变量
var myArray = [1,2,3];

// 请把你的代码写在这条注释以下
var myData = myArray[0];
```
### 使用索引修改数组数据

与字符串的数据不可变不同，数组的数据是可变的，并且可以自由地改变。

例如:
```JavaScript
var ourArray = [3,2,1];
ourArray[0] = 1; // ourArray等于 [1,2,1]
```

```JavaScript
// 举例
var ourArray = [1,2,3];
ourArray[1] = 3; // ourArray 的值为 [1,3,3].

// 初始化变量
var myArray = [1,2,3];

// 请把你的代码写在这条注释以下
myArray[0] = 3;
```
### 访问带索引的多维数组

可以把` 多维 `数组看作成是一个 数组中的数组。当使用`[]`去访问数组的时候，第一个`[index]`访问的是第N个子数组，第二个`[index]`访问的是第N个子数组的第N个元素。

例如:
```JavaScript
var arr = [
    [1,2,3],
    [4,5,6],
    [7,8,9],
    [[10,11,12], 13, 14]
];
arr[0]; // 等于 [1,2,3]
arr[1][2]; // 等于 6
arr[3][0][1]; // 等于 11
```

```JavaScript
// 初始化变量
var myArray = [[1,2,3], [4,5,6], [7,8,9], [[10,11,12], 13, 14]];

// 请只修改这条注释以下的代码
var myData = myArray[2][1];

```

### 用推动操纵阵列

一个简单的方法将数据追加到一个数组的末尾是通过 `push() `函数。

`.push() `接受把一个或多个参数，并把它“推”入到数组的末尾。
```JavaScript
var arr = [1,2,3];
arr.push(4);
// 现在arr的值为 [1,2,3,4]
```
**任务**
把 `["dog", 3] `“推”入到` myArray `变量的末尾。
```JavaScript
// 举例
var ourArray = ["Stimpson", "J", "cat"];
ourArray.push(["happy", "joy"]); 
// 经过 push 操作后，ourArray 的值为 ["Stimpson", "J", "cat", ["happy", "joy"]]

// 初始化变量
var myArray = [["John", 23], ["cat", 2]];

// 请把你的代码写在这条注释以下
myArray.push(["dog",3]);

```