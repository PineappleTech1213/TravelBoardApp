# 黑马程序员-PINK-JavaScript笔记

## JS基础

## Day3 - 数组

### 数组

```javascript
let arr = ['pink', 'hotpink'];
// 新增元素 - push()
// 追加到arr末尾，返回数组长度
arr.push('deep', 'red'); 		//可以增加1个或者多个
console.log(arr); 			// ['pink', 'hotpink', 'deep', 'red']

// 新增元素 - unshift()
// 追加到arr开头，返回数组长度
arr.unshift('blue');
console.log(arr); 			// ['blue', 'pink', 'hotpink', 'deep', 'red']

// 删除元素 - pop()
// 删除最后一个元素，返回该元素值
arr.pop();					// ['blue', 'pink', 'hotpink', 'deep']


// 删除元素 - shift()
// 删除第一个元素，返回该元素值
arr.shift();				// [pink', 'hotpink', 'deep']

// 删除元素 - splice(start, deleteCount)
// 删除指定元素, 从start开始删，删deleteCount个
arr.splice(1, 1)			// ['pink', 'deep']
```

### 数组排序

冒泡排序

```javascript
let arr = [2, 4, 3, 5, 1];
for (let i = 0; i < arr.length - 1; i++) {
    for (let j = 0; j < arr.length - i - 1; j++) {
        // 开始交换，前提是第一个数字大于第二个数字
        if (arr[j] > arr[j+1]) {
            let temp = arr[j];
            arr[j] = arr[j+1];
            arr[j+1] = temp;
        }
    }
}
console.log(arr);			// [1, 2, 3, 4, 5]

```

sort()

```javascript
// 1. 升序排列写法
arr.sort(function (a, b){
    return a - b;
})
console.log(arr);			// [1, 2, 3, 4, 5]

// 2. 降序排列写法
arr.sort(function (a, b){
    return b - a;
})
console.log(arr);			// [5, 4, 3, 2, 1]
```

## Day5 - 对象

### 对象的增删查改

```javascript
let obj = {
    name: '小米10青春版',
    num: '12025254215',
    weight: '0.55kg',
    address: 'China'
}
// 查
console.log(obj.name);
// 改
obj.name = 'iPhone';
// 增
obj.length = '110cm';
// 删
delete obj.length;

// 另一种 查
console.log(obj['name']);

```

### 对象的方法

```javascript
let obj = {
    name: '刘德华',
    // 方法
    singASong: function() {
        console.log('大家好我是zz辉')
    }
}

// 方法调用
obj.singASong();
```

### 遍历对象

```javascript
let obj = {
    uname: 'Jack',
    age: 18,
    gender: 'male'
}

// 遍历对象
for (let key in obj) {
    console.log(key);
    console.log(obj[key]);
}


```

内置对象Math - JS自带

```javascript
// ceil 向上取整
console.log(Math.ceil(1.1)) // 2
console.log(Math.ceil(1.5)) // 2
console.log(Math.ceil(1.9)) // 2

// floor 向下取整
console.log(Math.ceil(1.1)) // 1
console.log(Math.ceil(1.5)) // 1
console.log(Math.ceil(1.9)) // 1

// round 四舍五入
console.log(Math.ceil(1.1)) // 1
console.log(Math.ceil(1.49)) // 1
console.log(Math.ceil(1.5)) // 2
console.log(Math.ceil(-1.1)) // -1
console.log(Math.ceil(-1.5)) // -1
console.log(Math.ceil(-1.51)) // -2

// max() 和 min()
console.log(Math.max(1, 2, 3, 4, 5)) // 5
console.log(Math.min(1, 2, 3, 4, 5)) // 1

// abs() 绝对值
console.log(Math.abs(-1))	// 1

```

### random()

```javascript
// 生成 0 ~ 10 之间的随机数
Math.floor(Math.random() * (10 + 1) )

// 生成 5 ~ 10 之间的随机数
Math.floor(Math.random() * (5 + 1) ) + 5

// 生成 N ~ M 之间的随机数
Math.floor(Math.random() * (M - N + 1) ) + N
```

## APIs

## Day2 - 事件监听

```html
<button>按钮</button>
<script>
    // 	先获取元素源
    const btn = document.querySelector('.btn')
    //	修改元素样式
    // 	元素.addEventListener('事件类型'， 要执行的函数)
    btn.addEventListener('click', function() {
        alert('点击了~')
    })
</script>
```

### 事件类型

```javascript
/*
鼠标事件
鼠标点击	click
鼠标经过	mouseenter
鼠标离开	mouseleave

焦点事件
获得焦点	focus
失去焦点	blur

键盘事件
按下键盘	keydown
抬起键盘	keyup

文本时间
输入事件	input

*/


```

## Day5 - BOM

### 浏览器BOM对象

![image-20230712173547598](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712173547598.png)

### 定时器setTimeout()

![image-20230712174253159](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712174253159.png)

### location

![image-20230712201301362](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712201301362.png)

![image-20230712201352300](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712201352300.png)

![image-20230712201646842](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712201646842.png)

![image-20230712201710897](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712201710897.png)

### navigator

![image-20230712200519434](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712200519434.png)

![image-20230712200630930](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712200630930.png)

### history

![image-20230712200450222](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712200450222.png)

![image-20230712200400381](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230712200400381.png)

## Day6 - 正则表达式

### 正则表达式

![image-20230714202405062](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714202405062.png)

![image-20230714202532438](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714202532438.png)

![image-20230714202639869](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714202639869.png)

### 元字符

例如：[a-z] ： 代表匹配26个字母

- 边界符（表示位置， 开头和结尾，必须以什么为开头，or以什么为结尾）
- 量词 （出现次数，多少次）
- 字符类 （\d 表示0-9的数字）

![image-20230714203329316](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714203329316.png)

```javascript
// For example
console.log(/哈/.test('哈'))		// true
console.log(/^哈/.test('哈二'))	// true
console.log(/^哈/.test('二哈'))	// false

console.log(/哈$/.test('哈'))		// true
console.log(/哈$/.test('哈二'))	// false 因为不是以 ‘哈’ 结尾

// 当^ $一起，代表精确匹配，匹配字符必须要跟^$之间的一模一样
console.log(/^哈$/.test('哈'))		// true
console.log(/^哈$/.test('哈哈'))		// false 
console.log(/^哈二$/.test('哈二哈二'))	// false  也错，因为多了，就得只有2个字符且为‘二哈’
```

![image-20230714204208886](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714204208886.png)

```javascript
// For example
console.log(/^哈$/.test('哈'))		// true
console.log(/^哈*$/.test(''))		// true
console.log(/^哈*$/.test('哈哈'))		// true

// 量词 {n}
console.log(/哈{4}/.test('哈哈哈哈'))	// true
console.log(/哈{4}/.test('哈哈'))		// false

// 量词 {n,}	>= n
console.log(/哈{4,}/.test('哈哈哈哈'))		// true
console.log(/哈{4,}/.test('哈哈哈哈哈'))		// true

// 量词 {n,m}	>= n && <= m
console.log(/哈{4,6}/.test('哈哈哈哈'))		// true
console.log(/哈{4,6}/.test('哈哈哈哈哈哈哈'))		// false
```

![image-20230714231322967](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714231322967.png)

![image-20230714231624973](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714231624973.png)

![image-20230714231832733](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230714231832733.png)

![image-20230715015137418](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230715015137418.png)

![image-20230715015300668](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230715015300668.png)

![image-20230715015459339](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230715015459339.png)

![image-20230715015434697](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230715015434697.png)

## JS进阶

### Day1 - 作用域&解构&箭头函数

### 作用域 Scope

- var 是旧时代产物，可全局
- let const 推荐使用

### 垃圾回收机制

![image-20230717171002267](C:\Users\86159\AppData\Roaming\Typora\typora-user-images\image-20230717171002267.png)
