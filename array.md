###### 数组

```
var arr1 = [3]int{1, 3, 5}
fmt.Println(arr1) //[1 3 5]
```

```
var arr2 = [3]int{0: 8, 2: 9}
fmt.Println(arr2) //[8 0 9]
```

```
var arr3 = [3]string{"aa", "bb"}
fmt.Println(arr3) //[aa bb ]
```

for循环遍历
```
for i := 0; i < len(arr3); i++ {
	fmt.Println(arr3[i], i)
}
```

for...range循环遍历

```
var arr3 = [3]string{"aa", "bb"}
for i, v := range arr3 {
	fmt.Println(i, v)
}

//结果
0 aa
1 bb
2


```

二维数组
```
arr := [2][3]int{{1, 3, 5}, {2, 4, 6}}
fmt.Println(arr)

var s = [2][2]int{{1, 2}, {3, 4}}
fmt.Println(s)
```

###### 切片

1.通过make函数创建 make(类型, 长度, 容量)


```

// 第一个参数: 指定切片数据类型
// 第二个参数: 指定切片的长度
// 第三个参数: 指定切片的容量
var sce = make([]int, 3, 4)

fmt.Println(sce)//[0 0 0]
fmt.Println(len(sce)) // 3
fmt.Println(cap(sce)) // 4

```

2.通过Go提供的语法糖快速创建
<br/>
和创建数组一模一样, 但是不能指定长度
<br/>
通过该方式创建时, 切片的长度和容量相等
<br/>


```
var sce = []string{"aa", "bb", "cc"}
fmt.Println(sce) //[aa bb cc]

//追加
sce = append(sce, "dd")
fmt.Println(sce)	//[aa bb cc dd]

```








