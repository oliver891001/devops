# sed

文本查找与替换

### 参数
```
-n 安静模式，只有经过sed才会显示出来
-e 在命令列模式上进行 sed 的动作编辑
-f 直接将 sed 的动作写在一个文件内， -f filename 则可以运行 filename 内的 sed 动作
-i 直接修改读取的文件内容，而不是输出到终端

动作说明： [n1[,n2]]function
n1, n2 ：从n1到n2

function：
a ：新增
c ：取代
d ：删除
i ：插入
p ：打印
s ：替换
```

###使用案例

打印输出删除log中的3-5行

```
cat -n log1 ｜sed  '3,5d'
```

删除指定的行数(删除第三行)

```
cat -n log1 ｜sed  '3d'
```

从第三行之后删除所有的行数(删除第三行之后的所有)

```
cat -n log1 ｜sed  '3,$d'
```

打印文本

```
cat -n log1 ｜sed  '3,$p'
```


### History

v1:基础操作

v2:结合脚本使用

### License

[MIT License](https://opensource.org/licenses/mit-license.html). © Running Lee