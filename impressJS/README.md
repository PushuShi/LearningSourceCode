# Learning ImpressJS
___
### 使用
可去[原github](https://github.com/impress/impress.js) 下载最新版本
这里的impress-sps.js是个人对impress.js加了自己的一些详细的注释，以便学习理解；

当前注释尚不完整，会不断添加补充，如果有错误之处，欢迎指正。

### 数据属性
data-* 是html5新增的自定义属性，js通过dataset来获取这里数据；  

data-x = 幻灯片的x坐标

data-y = 幻灯片的y坐标

data-scale = 通过指定一个值来进行缩放，data-scale为5则将会在你幻灯片原始尺寸基础放大5倍

data-rotate = 通过一个数字度数来确定旋转你的幻灯片

data-rotate-x = 为3D用，这个数字度数是它应该相对x轴旋转多少度。（前倾/后仰）

data-rotate-y = 为3D用，这个数字度数是它应该相对y轴旋转多少度。 （左摆/右摆）

data-rotate-z = 为3D用，这个数字度数是它应该相对z轴旋转多少度。

### 全局预览
```html
<div id="overview" class="step" data-x="-200" data-y="-500" data-scale="3"></div>
```
### 主函数
var impress = window.impress = function ( rootId ) {......}

### 通用函数
| 函数 | 作用 |
|---|---|
| pfx（）|它通过检测浏览器给css3属性加上当前浏览器可用的前缀，这样就不用人工手写'Webkit" ,"Moz" 'O' ,'ms' .'Khtml'等浏览器前缀 |
| arrayify | 将Array-Like对象转换成Array对象  |
| css（）| 将指定属性应用到指定元素上 |  
| toNumber（）| 将参数转换成数字，如果无法转换返回默认值 |  
| byId（）| 通过id获取元素 |
| $（）| 返回满足选择器的第一个元素 |
| $$（）| 返回满足选择器的所有元素 |
| triggerEvent（）| 在指定元素上触发指定事件 |
| translate（）|将translate对象转换成css使用的字符串  
| rotate（）| 将rotate对象转换成css使用的字符串|
| scale（）| 将scale对象转换成css使用的字符串  |
| perspective（）| 将perspective对象转换成css使用的字符串 |
| getElementFromHash（）| 根据hash来获取元素，hash就是URL中形如#step1的东西|  
| computeWindowScale（）| 根据当前窗口尺寸计算scale。用于放大和缩小 |

### API

```
goto()  
init()
next()
prev()
initStep()  
```
