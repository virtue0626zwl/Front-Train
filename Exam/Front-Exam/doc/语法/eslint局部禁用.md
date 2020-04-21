## eslint局部禁用

###  禁用单行语句

- 第一种，直接在后面追加注释
```
// 直接在本行中禁用eslint
var test =  'test' + 4; // eslint-disable-line  
```
- 第二种，在单行语句上面追加注释
```
// 在下一行禁用eslint，类似上一种方法，只是写的位置不同罢了
// eslint-disable-next-line
var test =  'test' + 4;
```


###  禁用文件

- 在代码顶部添加注释
```
/* eslint-disable */
```

- 还可以在注释后加入详细规则，这样就能避开指定的校验规则了

```
// 如: 禁止在使用new构造一个实例后不赋值
/* eslint-disable no-new */
```

###  禁用和启动eslint

```

/* eslint-disable */
var a = 100;
console.log(a);  
/* eslint-enable */

```

###  禁用一条规则：

```
/*eslint-disable no-console */
var a = 100;
console.log(a);
/*eslint-enable no-console */
```

###  调整规则：

```
/* eslint no-console:0 */
var a = 100;
console.log(a);

```