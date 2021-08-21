# 萌新博客
有不懂的标签用谷歌搜索
```
MDN 关键字
```
前端第一戒律
永远不要让图片变形！
## 12.21

学会了上传代码到github
时间线跃迁 git reset --hard 6位标识符

## 12.22

1. WWW的发明与壮大
2. 了解HTML是什么
3. 掌握CRM学习方法
 * Copy
 * Running
 * Modify
 * 先抄后运再修改
4. html的四种标签
  ```html
    <!DOCTYPE html></html>
    <div id="title">???</div>
    <head>!!!</head>
    <div id=不用反斜杠>
  ```
5. 调试
  * vs code
  * webstorm
  * 在线调试 validator.w3.org

## 12.23

1. 学习html各个属性的用法
  * 不到万不得已,千万不要用id,因为id标签不会报错
  * id的作用,js可以直接获取id
  * id不能命名为全局属性名,即window.之后的所有单词
  * tabintex=0 是tab最后访问的地方 -1是tab不访问的地方
  * css可以在F12的style界面直接调试
  * title是鼠标指到之处浮动的小窗
2. 学习css内容标签
  * ol+li //ordered list + list item 有序列表
  * ul+li //unordered list + list item 无序列表
  * dl+dt+dd //description list+term+data 标题与介绍
  * pre // 使得多个空格能显示
  * * html的特点：多个空格/回车会合并成一个空格/回车
  * code // 里面的字符等宽
  * hr //分割线
  * br //break 换行
  * a //anchor 多用于超链接 
    ```html
     <a href="link">text</a>
     <a href="target="_blank</a>表示在新窗口打开
     ```
  * em //emphasis 语气强调
  * strong // 内容本身的重要性
  * q //quote 引用 没效果
  * blockquote // 换行引用

## 12.24
1. yarn global http-server
  * http-server . -c-1 -c代表缓存功能 -1代表不用这样做
2. 永远不要双击打开html 这样调试环境不同
3. yarn global add parcel时 因为node已经到达10.0,需要自行寻找8.0的parcel
  * 然后有bug,选择用http-server
4. a标签的download很多浏览器不支持
5. rel=noopener 为了防止一个bug 目前还没学
6. a的href的取值有9种
  * https协议,http协议,以及无协议的//,无协议优先选https,写链接时优先写//
  * id,用于跳转到指定标签href写#xxx,要跳转的标签id写xxx
```html
        <a href="#999">跳转</a>
        <p id="999">990</p>
```
  * 路径,绝对和相对路径均可.
  * 伪协议
  * javascript:代码
  * * 特殊用法:javascript:;使超链接点击后什么事都不会发生
  * mailto:邮箱
  * tel:手机号  面试时用来给面试官直接拨号给你
7. a的target的取值
  * _blank 新窗口打开
  * _self 当前页面打开
  * _top 使用此值后,在里面可以引用一个iframe页面
  * _parent 在此页面的上一层iframe页面打开链接
  * id,打开一个唯一id的页面,若其它链接id也相同,则会在此页面替换链接,想查该页面的id可以通过Console输入window.name
8. iframe 在当前窗口创建一个嵌入式页面
9. table 只有三个标签
  * thead
  * tbody
  * tfoot
  * 这三个标签里面可以有
```
  th(head组成一行,加粗)
  tr(row能组成一列)
  td(date组成一行，不粗)
```
  * table-layout:样式,auto根据内容调整宽度,fixed尽量平均宽度
  * border-collapse:使得格子之间没有缝隙
  * border-spacing:0也能达到同样效果。此值代表各格间距
10. img
  * src即图片地址
  * alt是当src图片加载失败时显示的内容
  * onload,onerror,监听图片加载
  * * 
     ```
     id.onload = function(){
       console.log("加载成功");
     }
     id.onerror = function(){
       console.log("加载失败")
     };
     即可计数成功失败次数
     ```
  * max-width:100% 响应式,使得图片在任何尺寸屏幕都显示全
11. form
  * action属性控制请求哪个页面
  * method属性控制用get还是post请求(以后会讲)
  * autocomplete自动填充
  * target 同a标签
  ```html
  <input type="submit" value="搞起">
  <button type="submit">搞起</button>
  ```
  区别在于,button里面还可以加标签
  * form里面必须有一个含有type="submit"的属性,如果没有,则会给一个没有属性的button添加submit
  * form里的input一定要有name
12. input
  * text
  * color
  * password
  * radio单选按钮,想让两个单选按钮互斥,就使其在同一组
  ```html
  <input name=class type="radio">1
  <input name=class type="radio">2
  ```
  * checkbox多选按钮
  * file选择文件,想多选则在后面加上multiple
  ```html
  <input type="file" multiple>
  ```
  * hidden隐藏
  * textarea多行输入框默认能拖动,不让拖的属性如下
  ```html
  <textarea style="resize: none;">
  ```
  * select就是下拉选单
  ```html
  <select name="请选择日期" id="">
  <option value="1">大年初一</option>
  <option value="2">2</option>
  </select>
  ```
  * onchange 
  * onfocus 把鼠标指在该处
  * onblur 把鼠标从该处挪走
## 12.24
  vscode输入多行的办法
  选中想输入的多行
  ctrl+shift+P
  输入emmet wrap
  在框中输入ul>li*即可获得如下效果
  ul>表示用一个ul框柱选中部分
  *表示每一条选中都被li框柱
  ```html
      <ul>
        <li>司马炎</li>
        <li>杨骏</li>
        <li>司马衷</li>
        <li>贾南风</li>
        <li>司马亮</li>
        <li>司马玮</li>
        <li>司马繇</li>
    </ul>
  ```
## 12.28
  * 重温如何克服拖延症,然后继续做html
  * 学习正则表达式
  * meta:vp的完整内容
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">

```

## 2021.1.4
>工作荒废了几乎一星期，重新起航！
  * css2.1使用最广泛 css3正在使用,每个模块独立升级
  * caniuse.com 输入特性名 就能知道各个浏览器支持什么特性
  * css只有两种语法
```
  选择器 {
  属性名: 属性值;
  /*注释*/
  }
```
```
  @charset "UTF-8"; //指定文件编码
  @import url(2.css); //导入css文件
  @media (min-width: 100px) and (max-width: 200px) {
  语法一
  } //媒体查询，以后会讲
```
  * 如何调试CSS 
  1. webstorm
  2. F12看该标签
  3. 最强方法 Border调试法！
```
  怀疑某个元素有问题
  就给这个元素加 border
  border 没出现？说明选择器错了或者语法错了
  border 出现了？看看边界是否符合预期
  bug 解决了才可以把  border 删掉
```
  * 在哪查css资料呢
  1. mdn 样式
  2. css trick
  3. 张鑫旭的博客
***
  * 在哪练习（抄）呢
  1. PSD
  * Freepik 搜索 PSD web
  * 365PSD 里的 UI 套件还行
  2. 效果图（不提供下载）
  * dribbble.com 顶级设计师社区
  3. 商业网站
  * 直接模仿你常去的网站
***
  >外包公司的缺点，你做的都是重复工作。不能呆超过一年半，否则无法提升。
  * margin默认能多宽有多宽
  * 学精JS好过学精CSS
## 1.5
  >盒模型分两种，content-box和border-box
  * 内容盒的宽度和设定的一样
  * 边框盒的宽度=borer+padding+内容
***
  * 孩子之间的margin会合并
  * 外边距合并只在上下存在
  * border-radius:50% 就是圆形
***
## 1.7
  1. float布局，IE用的了解一下就行，以后大概用不上了。
  * 如果图片下面有颜色溢出，加一行vertiacl-align:top;
  * border调试可能会干扰位置，可以换成outline。
  * 居中方法margin-left:auto; margin-right:auto;
  * 如果需要平均布局，会需要用到负margin。负margin不会换行。
***
## 1.9
  1. flex容器由两种写法
```css
.container{
  display: flex; /*快捷输入 d:f + tab*/
}/*这个会另起一行*/
```
```css
.container{
   display: inline-flex;
}/*这个不会另起一行*/
```
  * flex-direction:row; 流向横/反横/纵/反纵
  * flex-wrap: wrap; 是否换行wrap是/nowrap否
  * justify-content: 主轴（默认为横）对齐方式
  * align-items: 副轴（默认为纵）对齐方式
***
## 1.10
  1. grid布局,快淘汰了
## 1.11
  1. 学习css层级
  * float属性的div在普通div的上方
  2. position: static;默认属性 什么都不改，所以也不用写出来
  3. position: relative;属性
  * z-index:1 表示比0高一层
  4. position: absolute;属性<br>
 <span style="color:red;">会找第一个不是static的祖先标签进行匹配，不是只找relative</span>
> white-space:nowrap; 文字内容不准换行，通常用于button按钮

```css
button span{
  display: none; /* 内容不显示 */
}
button:hover span{
  display: inline-block; /* 鼠标挪过去才显示 */
}
```

  * F12-style-hov-hov打钩 就可以看鼠标悬停内容
  5. position:fix;相对于视口定位，具体来说对于iframe标签，常用语回到顶部按钮。
  * fix不要和transform混用，会出现问题。
  * fix别用在移动端，全是问题。
  6. position: sticky;窗口下滑时总有一行悬浮在最上方，意为粘滞。
  7. z-index: 层级从上到下为
```
99
...
1
0
-1
...
但是不能跑到html后面
```
***
## 1.17
  * 打开控制台按ESC，点击console旁边的三点，选择rendering，给paint flashing打钩。就可以看渲染过程。闪烁一次代表渲染一次。
  * ctrl+shift+L 饥人谷js代码格式化
  * csstriggers.com 写了不同浏览器的渲染方式
***
渲染原理
1. HTML构建HTML树
2. CSS构建CSS树
3. 合并成一颗渲染树
4. Layout-Paint-Compose依次进行
***
transition
```css
#heart{
  margin:100px;
  position:relative;
  display: inline-block;
  transition: all .5s;
}
#heart:hover{
  transform:scale(1.5);
}
```
***
animation
```css
#heart{
  margin:100px;
  position:relative;
  display: inline-block;
  animation: heart 1s alternate infinite;
}
#heart:hover{
  from{
    transform:scale(1.0);
  }
  to{
    transform:scale(2.0);
  }
}
```
***
个人感觉animation更灵活一些
***
### HTTP部分
127.0.0.1 表示自己<br>
localhost 表示通过host指向自己<br>
0.0.0.0 不指向任何设备<br>
node.js
* ``这种引号里面可以用回车
* ''这种引号必须写\n才能回车

vscode ctrl+/ 一键注释<br>
node server.js 8888 运行js服务器
***
## 1.19
如何成为专家->踩坑足够多 <br>
如何踩坑->个人做项目，意思是所有代码都是你一个人写的，这样能全方位踩坑<br>

JavaScript的诞生
```
必须蹭Java流量
名字mocha->LiveScript->JavaScript
布莱登用十天就做成了
浏览器刚开始同时支持java和javascript
经过时间的洗礼java转去后端了
```
浏览器大战
```
微软发布IE3并支持JScript
网景t联合其它浏览器在ECMA弄了个浏览器标准ECMAScript
但是98年微软把IE捆绑在windows里打败了网景
同年网景开源自家的浏览器，成为了Firefox
99年网景被AOL收购
IE6进入全盛期
2001-2010，IE6都是全球份额最高。Firefox紧随其后。
谷歌2008年发布chrome。
2011年份额超过Firefox。
2016年拿下全球62%的份额。
同年淘宝天猫宣布不再支持IE6、IE7
年底宣布不再支持IE8
从此国内前端极速发展
```
回头说说ECMAScript标准
```
1997.06，第一版发布
1999.12，第三版发布，IE6也支持该版。所以使用广泛
第四版流产
2009.12，第五版发布
注：99-09年IE6一手遮天
2015.06，第六版发布，新浏览器都支持这一版
以后每年都发布一版，版本号以年份命名
```
JS与ECMAScript(简称ES)的关系
```
ES是纸上的标准，JS是实现。先实现，再讨论出标准。
是总结型标准，不是指点型标准。
```
JavaScript的兴起
```
2004年谷歌发布Gmail在线网页
2005年前端技术正式出现
2006年jQuery发布，目前最长寿的JS库
jQuery强在哪？能同时兼容IE和Firefox。
所以IE不行了jQuery热度也有所下降
```
中国的前端发展
* 来源
1. 后端转前端
2. 设计师转前端
* 缺人
1. 大学不教前端
2. 早期前端工资比不上后端，所以科班多半做后端
~~哦我也是科班啊，个人项目都没写过的屑科班~~<br>

JavaScript的爆发
```
Chrome的JS引擎叫V8（V8的作者还写过V1-V7，分别对应8种不同的语言的虚拟机，神仙）
2009年Ryan基于V8创建了Node.js
2010年Isaac基于Node.js写出了npm
同年TJ受Sinatra启发，发不了Express.js
至此，Node.js终于能部分取代java、php、C++等后端语言独自运行服务器，但并不能完全代替，以后再谈。
从此前端工程师可以写后端应用了
```
JavaScript的走位
1. JS有一个标准，相当于谁都能实现、讨论JS，开创了互联网先河。
2. Gmail也开创了互联网先河，浏览器竟然可以收邮件，以前收邮件都是下载软件的，Gmail正是JS写的。也是JS的正名之作。
3. 移动端上使用JS很省电，至少比Flash省……
4. Node.js的出现，使得JS前后端通吃。

***
## 1.20
把HTML和CSS下载并合并起来的过程，叫做渲染<br>
浏览器的功能模块：用户界面、渲染引擎、JS引擎、存储。
线程是一种比进程更小的东西
JS有些什么引擎呢
* Chrome用的V8，C++写
* Firefox用的SpiderMonkey，C++写
* Safari用的JavaScriptCore，不用记
* IE用的Chakra(JScript9)
* Edge用的V8
* Node.js用的V8
>我们主要讲V8
>JS引擎的作用是编译、优化、执行和垃圾回收
***
## 7.11
懒狗回归

***
## 7.14
=的意思是把右边的东西复制给左边，A=B就是把B的内容给A<br>
===是对比 就是我们数学上的用法
了解JS的内存使用<br>
预览markdown ctrl+shift+v<br>
做一个canvas画板<br>
预览html 在终端输入hs . -c-1<br>
先随便试试事件，错了再改
学习canvas

***
## 8.17
canvas画线<br>
***
## 8.18
学习JS<br>
js的优点：门槛低，用途广<br>
js的特点：<br>
什么是表达式
>表达式就是有值的东西
只有函数有返回值
1+2的值是3 不是返回值

什么是语句
>var a=1 是一个语句，语句一般会改变环境，可能没有值。

大小写敏感<br>
回车和空格大多数情况无所谓<br>
但是return后面不能加回车<br>
比如
```js
function a(){return 3}
```
输入a()回车 返回3
```js
function b(){
  return
  3
}
```
输入b()回车 返回undefined<br>
因为return后面没东西的话js会自动帮你补充undefined 很蛋疼<br>
老师强调：写代码要多些注释===放屁<br>
坏的注释
* 把代码翻译成中文
* 过时的注释 没删掉
* 发泄不满的注释

好的注释
* 踩坑注解
* 为什么代码写得这么奇怪，遇到什么bug

>webstorm除了打开慢，没有缺点！

>vscode开得快，免费，但是代码报错功能很烂

if语句<br>
if(表达式){语句1}else{语句2}<br>
逗号表示这句话没完<br>
分号表示这句话结束<br>
```
程序员第一戒律
不要相信人类，包括你自己
程序员第二戒律
不要用有歧义的语法
所以推荐语法为
if (表达式) {
  语句1
} else if (表达式2) {
  语句2
} else {
  语句3
}
```
switch语句<br>
不推荐用，别问，谁用谁知道。<br>

问好冒号表达式<br>
if else都是单条件单结果的话，可以省略成这样<br>
```js
function max(a,b){
  return a>b ? a:b 
  //如果a>b返回a 否则返回b
}
```

&&短路逻辑<br>
a&&b&&c&&d 取第一个假值或d<br>
不会取true/false<br>
```js
if(f1){
  console.log('exist f1')
}//如果定义了f1，就打印存在f1
```
等价于
```js
f1 && console.log('exist f1')
```

||短路逻辑<br>
a||b||c||d 取第一个真值或d<br>
不会取true/false<br>
```js
if(b){
  b=b
  }else{
    b=100
    }/*如果b存在，就不变。如果不存在则赋值100。用于检验b是否存在，100是个保底值。*/
```
等价于
```js
b=b || 100
```

while循环
```js
var i = 0.1
while(i !== 1){
  console.log(i)
  i = i+0.1
  }
```
会死循环，因为浮点数不精确，0.2+0.1=0.30000000000000004<br>
do while感兴趣的自己了解<br>

for循环<br>
其实是while循环的简便写法
```js
for(语句1;表达式2;语句3){
  循环体
}
```
先执行语句1，然后判断表达式2。<br>
真，执行循环体，再执行语句3。<br>
假，退出循环，执行下面的语句。<br>
```js
for(var i=0;i<5;i++){
  console.log(i)
}//会打印01234
```
此时输出i，值为5。<br>
因为先判断i<5，打印4。<br>
然后4+1，判断i<5。不打印了。但i已经等于5<br>

```js
for(var i=0;i<5;i++){
  setTimeout(()=>{ 
    console.log(i)
    },0) //setTimeout(()=>{},0)意为延迟0ms后执行
}//会打印55555
```
>下面这个循环不打印01234的原因是
代码停止这个循环后，才会延迟0ms执行打印。
由于i已经加完了，所以打印5。
由于代码执行了五次，所以攒下五次延迟打印。
解决方法很简单，把var改成let。
实际上这个let是写JS标准的人做的特殊处理，正常输出就应该是5个5。

break和continue<br>
break跳出该循环，只会退出最近的循环<br>
continue跳过单个循环，有些语言把这个指令写作next<br>
```js
for(var i=0;i<10;i++){
  if(i%2===1){
      console.log(i)
      break
  }
}
//打印1 跳出循环
```
```js
for(var i=0;i<10;i++){
  if(i%2===1){
      console.log(i)
      continue
  }
}
//打印13579 跳出循环
```

label语句<br>
```js
{
  foo:1
}//这是个foo标签，里面的语句是1

var a ={
  foo:1
}//这是个对象
```

## 8.19
电话号码一定要用字符串，数字不行<br>
JS有7+1种数据类型<br>
number<br>
string<br>
symbol<br>
undefined<br>
null<br>
object = {array,function,date}<br>
数组函数日期，都是object<br>
四基两空一对象<br>
最新的数据类型bigint，用不到先不急<br>

1.23e4=1.23*10^4 科学计数法<br>
***
number的特殊值
>正零+0 负零-0 和 零0

>正无穷+Infinity 负无穷-Infinity

>NaN=Not a Number 不是一个数字，或者说不确定是哪个数字。比如0/0=NaN
***
bool的falsy值
>falsy意为与相当于false又不是false的值<br>
有5个，分别是 undefined null 0 NaN ''

只有这5个+false是假值<br>
还记得&&吗，取第一个假值或最末尾的真值<br>
```js
1 && 2
1 && 0
```
输出2和0，因为0是falsy<br>

## 8.20
var a = 1 <br>
现在基本弃用var<br>
let a = 1 <br>
作用于一个{}大括号里，可以不赋值，for配合let就不会有一些怪问题<br>
const a = 1<br>
const和let几乎相同，唯一区别，声明时要赋值，且不可更改。<br>

数字变字符串<br>
```js
let a = 1
a+''
```
字符串变数字
```js
let a = '123'
a-0
```
用String(a)也行，但有点小bug
```js
String(1000000000000000000000000000000000000000)
```
后面很多零会转换成"1e+39"<br>
任意数据转布尔<br>
```js
Boolean(1)
!!1
```
一个！代表取该数据的反布尔，两个！就是原布尔了。<br>

任意数据转字符串<br>
true.toString()<br>
得到"true"<br>
1.toString()，提示bug。<br>
因为js默认1.之后你是要写一个小数，看到你写个t就觉得你写错了。<br>
得改成(1).toString()<br>
或者1..toString()<br>
因为js认为1.是个正常数……<br>
js的更多bug详见https://bonsaiden.github.io/JavaScript-Garden/zh/

***

对象<br>
键名是字符串<br>
声明对象的两种语法<br>
```js
let obj = {key:'value',属性名:'属性值'}
let obj = new Object ({key:'value'})//标准写法
```
键名引号有时可以省略<br>
比如<br>
```js
let obj = {1e2:true,}
```
键名会自动转换为'100'<br>
[]方括号，能取该变量的值作为键值<br>
```js
let a = 'xxx'
let obj = {
  [a] : 1234
}
```
obj输出为xxx:1234<br>
除了字符串，symbol也能做属性名。<br>
```js
let a = symbol()
let obj = {[a]:'hello'}
```

## 8.21
属性的增删改查
***

删
```js
let obj = {name:'frank',age:18}
obj.name = undefined //仅删除属性值
delete obj.name //整个属性都删除
```
检查整个属性是否删除成功了
```js
'name' in obj //true=删了，false=没删
//一定要记得加引号啊！
```
检查是否删除属性值但没删属性名
```js
'name' in obj &&obj.name === undefined
```
不能单obj.name === undefined，如果删了整个属性，这样也返回true<br>

读
```js
let obj = {name:'frank',age:18}
Object.keys(obj) //读取属性名
Object.values(obj)//读取值
Object.entries(obj)//读取属性名+值

Object.dir(obj)//读取属性名+公共属性名+值+公共值

'toString' in obj//判断obj是否包含toString属性，存在true
obj.hasOwnProperty('toString')
//判断toString属性是否是obj的私有属性
//true为私有，false不是私有
```
所有对象都有原型，对象的原型也是对象<br>

查<br>
```js
obj['key']//查单个属性的值
obj.key //这里的key是字符串，不是变量
console.dir(obj)//查obj的所有属性
```

改或增<br>
直接赋值
```js
let obj = {name:'frank'} //直接覆盖之前的，无论是否存在
obj.name = 'frank' //给obj的'name'属性修改值为'frank'

let key ='name';obj[key]='frank'//一般没必要用这个
//新建一个属性name，赋值frank再扔到obj里
```
批量赋值
```js
Object.assign(obj,{age:18,gender:'man'})
```
改增共有属性<br>
改原型都是高手做的，新手了解一下即可
```js
obj.__proto__.toString='xxx'//不推荐改带下划线的东西
Object.prototype.toString='xxx'
```
增加公共属性
```js
let common = {nation:'CN',hair:'black'}
//构造一个common对象
let obj1 = Object.create(common)
//让common的所有属性成为obj1对象的公共属性
obj1.name='sam'
let obj2 = Object.create(common)
obj2.name='amy'
//此时两个obj的name属性不同，nation和hair属性相同
```
公共属性重新关联会抹掉私有属性
```js
let obj1 = Object.create(common)
obj1.name='sam'
let obj1 = Object.create(common)
//此时obj1没name属性了
```
所以一旦关联就不要轻易修改关联