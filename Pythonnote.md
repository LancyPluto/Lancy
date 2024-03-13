#  -Python

## 一：Python程序格式-缩进-行注释-段注释

### 程序格式-缩进

1.python用**缩进**而不是**{}**表示程序块的层次关系，因此要用适当的空格来缩进。

2.**语句每次都要从新行的第一列开始**（容易报错）。

3.python区分大小写。

### 行注释-段注释

1.单行注释：每行注释前加 **#** 号，#后的内容即为此行的注释。

2.段注释（多行注释）：使用三个单引号 **‘’‘** 或三个双引号 **“”“** 。当解释器看到 **’‘’** 则会扫描到下一个**‘’‘**，然后忽略他们之间的内容。

![image-20240121215536767](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240121215536767.png)



3.快捷键： *ctrl+/*

​                   按下后，鼠标点击的行就变成了注释

## 二：Python程序的构成 

1.行连接符：**\ ** ，放在这一行结束的地方

![image-20240121221821522](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240121221821522.png)



## 三：对象的基本组成和内存示意图

1.对象的基本组成

a.标识：唯一标识对象，通常对应于对象在计算机内存中的地址。

b.类型：表示对象存储的”数据“的类型。

c.值：表示对象所存储的数据的信息。

2.对象的本质：一个内存块，拥有特定的值，支持特定类型的相关操作。

## 四：引用的本质-栈内存和堆内存-内存示意图

1.变量位于**栈内存**（连续的空间），对象位于**堆内存**（不连续的空间）。

2.Python是动态类型语言：变量不需要显式声明类型，根据变量引用的对象，Python解释器自动确定数据类型

## 五：标识符-帮助系统简单使用-命名规则

标识符四大规则：

1.区分大小写

2.第一个字符必须是字母，下划线。其后的字符是：字母，数字，下划线。

3.不能使用关键字（可以使用help（）

​                                                  help>keywords 来查看关键字）。比如‘if'，’or‘。

4.以双下划线开头和结尾的名称通常含有特殊含义（例如：__ _init_ _ _(),是一个函数），尽量避免这种写法。



## 六：变量的申明-初始化-垃圾回收机制

1.删除变量机制：**del** 删除不再使用的变量。如果对象没有变量引用，就会被垃圾回收器回收清空内存空间。

![image-20240123143529512](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123143529512.png)

此时程序会报错

## 七：常量-链式赋值-系列解包赋值

1.常量：python不支持常量，即没有语法规则限制改变一个常量的值。

2.链式赋值：用于同一个对象赋值给多个变量‘x=y=120'.

3.系列解包赋值：系列数据赋值给对应相同个数的变量（个数必须保持一致），例如：a,b,c=4,5,6   **a,b=b,a(变量值的互换)** 

## 八：内置数据类型-基本算数运算符

1.python内置的四种类型：整型 int  浮点型 float  布尔型 bool  字符串型 str

![image-20240123145012776](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123145012776.png)



2.基本运算符： 

![image-20240123150047631](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123150047631.png)

使用divmod0（）函数同时得到商和余数

![image-20240123155344132](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123155344132.png)



## 九：整数-不同进制-其他类型转成整数

1.0B或0b表示二进制

2.0O或0o表示八进制

3.0X或0x表示十六进制

4.使用int（）实现类型转换（括号内是数字不需要加双引号，如果是字符类型就要加双引号）

![image-20240123160546230](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123160546230.png)

5.自动转型：整数和浮点数混合运算时，表达式结果自动转型成浮点数。比如： 2+8.0 的结果是 10.0

6.round（）函数可以返回四舍五入的值。但不会该改变原有值，而是产生新的值。

![image-20240129143507302](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240129143507302.png)

7.增强型赋值运算符：运算符‘+’，'-'，‘*’，‘/’，‘//’，‘**’和 ‘ %’ 与 = 结合可以构成‘增强型运算符（和C语言一致）。

## 十：时间的表示

1.python中可以通过time.time（）获得当前时刻（使用前要先import，不然使用不了），返回的值是以秒为单位，带微秒精度的浮点值（从1970年10月10日至现在）。

![image-20240123203527989](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123203527989.png)

## 十一：布尔值本质-逻辑运算符-位运算符-比较运算符-短路问题

1.在python语言底层，会将布尔值Ture看作1，将布尔值False看作0，尽管从表面上看，Ture和1，False和0是完全不同的两个值，但实际上，他们是相同的。

2.在python语言中有一些特殊的布尔类型值为False，例如False，0，0.0，空值None，空序列对象（空列表，空集合等），空range对象，空迭代对象。其他情况均为True。

![image-20240123204942790](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123204942790.png)



3.逻辑运算符：和c语言一致

![image-20240123210045778](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123210045778.png)

4.比较运算符：所有比较运算符返回1表示真，返回0表示假。分别和True和False等价（**在python中可以使用连续判断，例如 3<a<10**）。

5.位运算符：

![image-20240123211132129](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123211132129.png)

 6.![image-20240123212242248](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123212242248.png)

7.**python不支持自增  ++ 和自减 --**

## 十一：同一运算符-身份运算符-优先级问题

1.同一运算符**is**和**is not**：is比较id，比较地址，而’==‘比较值。

![image-20240123213032313](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240123213032313.png)

2.整数缓存问题：命令行模式下，python仅仅对**比较小的整数**对象进行缓存（范围为[-5,256]）缓存起来，因此上面的a和b都是同一个已被提前缓存的对象。*文件模式*（即写代码的界面）下，**所有数字**都会被缓存 

![image-20240124130736638](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124130736638.png)

## 十二：字符串-Unicode字符集-三种创建字符串的方式

1.python的字符串是不可变的，我们无法对原字符串做任何修改

2.可以用ord（）把字符转换成对应的Unicode码

3.使用内置函数chr（）可以把十进制数字转换成对应的字符

![image-20240124132454503](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124132454503.png)

4.可以通过单引号或双引号创建字符串，例如：a=‘abc’，b=“sxf”。

5.连续三个单引号或三个双引号，可以帮助我们创建多行字符串。并且在长字符串中会保留原始的格式

![image-20240124132957459](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124132957459.png)

![image-20240124133008428](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124133008428.png)

## 十三：字符串-转义字符-字符串拼接-字符串复制-input获取键盘输入

1.转义字符：

![image-20240124133421299](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124133421299.png)

2.字符串拼接： 如果‘+’两边都是字符串，则拼接。也可以将多个字符串放在一起实现拼接，例如：

![image-20240124133936858](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124133936858.png)

3.字符串复制：使用‘*’可以实现字符串复制

4.不换行打印：python调用print会自动印一个换行符，如果不想自动换行。我们可以自己通过参数**end=“任意字符串”**，来实现末尾添加任何内容

![image-20240124134354736](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124134354736.png)

5.从控制台读取字符串：使用input（）从控制台读取键盘输入的内容（**注意：获取到的内容是字符串，即使输入的是数字，也会是字符串的形式**）

![image-20240124134609976](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124134609976.png)

## 十四：字符串-str（）-字符提取-replace（）替换-内存分析

1.replace()实现字符串替换

![image-20240124204358268](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124204358268.png)

2.str（）可以帮助我们将其他数据类型转换为字符串。

![ ](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240124204446493.png)

3.索引：正向索引和c语言一致。逆向索引从==-1==开始算

## 十五：字符串切片slice操作-逆序

1.典型操作：

![image-20240125160923825](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240125160923825.png)



![image-20240125170734561](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240125170734561.png)



## 十六：字符串-split（）分割-join（）合并-代码效率测试

1.分割：split（）可以基于指定分隔符将字符串分隔成多个子字符串。如果不指定分隔符，则默认使用空白字符 

![image-20240125172020859](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240125172020859.png)

2.合并：join（）将一系列字符串连接起来。*join函数只新建一次对象，所以效率高于+*。

![image-20240125173919039](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240125173919039.png)

## 十七：字符串-驻留机制-同一判断-值相等判断

1.字符串驻留：常量字符串只保留一份。

![image-20240126154301622](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240126154301622.png)

2.判断：和c语言一致。

3.成员操作符判断子字符串：==in ，not in==判断某个字符（子字符串）是否存在于字符串中。

## 十八：字符串-常用查找方法-去除首位信息-大小写转换-排版-特征判断

1.字符串常用函数：

![image-20240126154953502](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240126154953502.png)

2.去除首尾信息：可以通过strip（）去除字符串首尾指定信息。用lstrip去除字符串左边指定信息，rstrip（）去除字符串右边指定信息。

![image-20240126155250214](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240126155250214.png)

3.大小写转换：

 ![image-20240126155719323](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240126155719323.png)

4.格式排版：center（），ljust（），rjust（）这三个函数用于对字符串实现排版：

![image-20240126163024743](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240126163024743.png)

5.特征判断方法：

![image-20240126165330191](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240126165330191.png)

## 十九：字符串-format格式化-数字格式化操作

1.format（）的基本用法：通过{}和：来代替以前的%。format（）函数可以接受不限个数的参数，位置可以不按顺序。

![image-20240128223531653](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128223531653.png)

![image-20240128224031886](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128224031886.png)



![image-20240128224157285](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128224157285.png)

2.填充常跟对其一起使用：^, <, > 分别是居中，左对齐，哟对其，后面带宽度==：==号，==：==后带填充的字符，只能是一个字符，不指定的话默认是用空格填

![image-20240128224944885](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128224944885.png)

3.数字格式化：浮点数通过==f==，整数通过==d==进行需要的格式化。案例如下：

![image-20240128225150963](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128225150963.png)

## 二十：可变字符串-io.StringIO

1.可变字符串：在python中，字符串是不支持原地修改的，但如果确实需要原地修改字符串，可以使用io.stringIO对象或array模块（使用前需要先导入io模块（import io））

![image-20240128225941524](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128225941524.png)

## 二十一：类型转换总结

![image-20240128230253693](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240128230253693.png)

## 二十二：列表-特点-内存分析

1.列表：

a.用于存储任意数目，任意类型的数据集合

b.列表是内置可变序列，是包含多个元素的有序连续的内存空间。其标准语法格式：

​                          ==a = [10,12,30]==

c.列表中的元素可以各不相同，可以是任意类型，比如：

​                    ==a = [10,20,'abc',True]==

d.python中列表的大小可变，根据需要随时增加或减小

2.列表对象的常用方法：

![image-20240202213658744](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240202213658744.png)

## 二十三：创建列表的4钟方式-推导式创建列表

1.列表的创建：

a.基本语法**[]**创建

![image-20240202214131062](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240202214131062.png)

b.list()创建

![image-20240202214223669](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240202214223669.png)

2.range()创建整数列表：其语法格式为  ==range（[start],end,[step]）==

![image-20240202214832775](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240202214832775.png)

典型示例：

![image-20240202215431729](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240202215431729.png)

3.推导式创建列表

![image-20240203161233727](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203161233727.png)

## 二十四：列表-元素的5种添加方式-效率问题

1.列表元素添加的五种方式：

a.**apend()方法**：原地修改列表对象，是真正的**列表尾部添加新的元素**，==速度最快==。

![](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203162251178.png)

b.**+ 运算符操作**：并不是真正的尾部添加元素，而是创建新的列表对象；**将原列表元素和新列表元素依次复制到新的列表中**。这样会涉及大量的复制操作，**对于操作大量元素不建议使用**。

![image-20240203162716128](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203162716128.png)

c.**extend()方法**：将目标列表的*所有*元素添加到本列表的尾部，属于原地操作，**不创建新的列表对象**

![image-20240203162951539](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203162951539.png)

d.**insert()插入元素**：使用insert()方法可以将指定的元素插入到列表对象的任意指定位置。*插入位置后面的元素都会移动*

![image-20240203163455702](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203163455702.png)

e.**乘法扩展**：和字符串乘法相同，生成一个新列表。

![image-20240203163732251](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203163732251.png)

## 二十五：列表删除的三种方式-删除的本质时元素是拷贝

1.**del()删除**：删除指定位置的元素

![image-20240203164124135](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203164124135.png)

2.**pop()方法**：删除并返回指定位置元素，如果未指定位置则默认操作列表最后一个元素

![image-20240203164308786](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203164308786.png)

3.**remove()**:删除**首次**出现的指定元素，若不存在则该元素抛出异常。

![image-20240203165710868](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203165710868.png)

## 二十六：列表-元素的访问-出现次数统计-成员资格判断

1. 通过索引直接访问元素

![image-20240203220358726](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203220358726.png)

2.index()获得指定元素在列表中首次出现的索引：index()可以获取指定元素首次出现的索引位置

![image-20240203222145202](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203222145202.png)

3.count()：获得指定元素在列表中出现的次数

![image-20240203222632783](C:\Users\彦祖\AppData\Roaming\Typora\typora-user-images\image-20240203222632783.png)

4.len()：返回列表长度

![image-20240203225839667](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203225839667.png)、

5.使用in和not in来判断列表中是否存在指定元素

![image-20240203225940365](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203225940365.png)

## 二十六：列表切片slice操作

*和字符串切片一致*

## 二十七：列表-遍历-排序-max-min-sum

1.复制列表所有元素到新列表对象 ：

```python
```list1 = [30,40,50]
list2 = list1
```

**上面这个代码只是将list2也指向了列表对象，也就是说list1和list2持有的地址值是相同的，列表对象本身的元素并没有复制**。

```python
list1 = [30,40,50]
list2 = [] + list1
```

**可以通过这种方式来实现列表元素内容的复制**

2.排序：

a.建新列表的排序：使用内置函数sorted()进行排序，这个方法返回新列表，不对原列表做修改

（**下面应为c = sorted(a**==,==**reverse=True，图片打错了**)

![image-20240203232925634](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203232925634.png)

b.不创建新的列表排序：使用内置函数sort()

![image-20240203234019778](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203234019778.png)

3.reversed()返回迭代器：内置函数reversed()也支持进行逆序排序，但reversed()不对原列表做任何修改，只是返回一个逆序排列的迭代器对象

![image-20240203234738407](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203234738407.png)

![image-20240203234452922](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203234452922.png)

![image-20240203234505292](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240203234505292.png)

4.max和min：用于返回列表中最大和最小值

![image-20240205155057454](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205155057454.png)

5.sum：对数值型列表的所有元素进行求和操作，对非数值型列表运算则会报错

![image-20240205155253149](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205155253149.png)

## 二十八：列表-二维列表-表格数据存储和读取

1.二维列表：和c语言基本一致。

![image-20240205160142638](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205160142638.png)

## 二十九：元组-特点-创建的两种方式-tuple()要点

1.元组：元组和列表用法几乎一模一样，**但是元组属于不可变序列，不能修改元组中的元素**。因此，元素没有增加元素，修改元素，删除元素的方法。

![image-20240205162042714](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205162042714.png)

2.元组的创建：通过()创建元组。小括号可以省略。如：a = (10,20,30)或者 a = 10,20,30。

 **如果元组只有一个元素，则必须后面加逗号。这是因为解释器会把(1)，解释为整数1，(1,)才会被解释为元组**

![image-20240205162436046](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205162436046.png)

3.通过tuple()创建元组（和list()一样）

![image-20240205162910889](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205162910889.png)

## 三十：元组-元素访问-计数方法-切片操作-成员资格判断

1.元组的元素访问和计数：和列表基本上一致，但元组不能修改

![image-20240205164715389](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205164715389.png)

![image-20240205164723471](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205164723471.png)

2.元组排序：只能使用内置函数sorted(tupleObj),并生成新的**列表**对象

![image-20240205174455465](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205174455465.png)

3.zip:zip(列表1，列表2，……)将多个列表对应位置的元素组合成为元组，并返回这个zip对象

**如果各个迭代器的元素个数不一致，则返沪列表长度与最短的对象相同**

![image-20240205223115399](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240205223115399.png)

## 三十一：元组-生成器推导式创建元组-总结

1.从形式上看，生成器推导式与列表推导式类似，只是生成器推导式使用小括号。

2.但是，列表推导式直接生成列表对象，生成器推导式生成的既不是列表也不是元组，**而是一个生成器对象**。

![image-20240207200803435](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207200803435.png)

![](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207200803435.png)



用tuple()可以生成元组（只能使用一次，再使用一次会生成空元组）

![image-20240207200915211](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207200915211.png)

![image-20240207200929006](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207200929006.png)

使用_ next _()遍历元组

![image-20240207201425668](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207201425668.png)

![image-20240207201432601](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207201432601.png)

## 三十二：字典-特点-四种创建方式

1.字典：

![image-20240207201645850](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207201645850.png)

一个典型的字典的定义方式：

```python
a = {'name':'gaoqi','age':18,'job':'programmer'}
```

2.字典的查找：字典中通过“键对象”找到对应的“值对象”。

![image-20240207202023296](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207202023296.png)

如果键重复，后面的键会把前面的键覆盖



3.字典的创建：

通过{}，dict()来创建字典对象：

![image-20240207202232201](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207202232201.png)

通过zip()：

![image-20240207202329126](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207202329126.png)

通过fromkeys()创建值为空的字典：

![image-20240207202406475](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207202406475.png)

## 三十三：字典-元素的访问-键的访问-值的访问-键值对的访问

1.元素的访问： 

a.通过{键}获得值

![image-20240207204123768](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207204123768.png)





b.通过get()方法获得值。优点：指定键不存在，返回None；也可以设定指定键不存在时默认返回的对象。推荐使用get()获取值对象

![image-20240207204842755](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207204842755.png)

 

![image-20240207204853787](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207204853787.png)

2.列出所有的键值对：

![image-20240207205109438](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207205109438.png)

3.列出所有的键，所有的值

![image-20240207205135992](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207205135992.png)

4.len()计算键值对的个数



![image-20240207205308040](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207205308040.png)

5.检测一个”键“是否在字典中

![image-20240207205336623](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207205336623.png)



## 三十四：字典-元素的添加-修改-删除

1.使用update()将新字典中所有键值对全部添加到旧字典对象上。如果key有重复，则直接覆盖

![image-20240207210248505](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240207210248505.png)

2.字典元素的删除：可以使用del()；或者clear()删除所有键值对；pop()删除指定键值对，并返回对用的值对象

del()和pop()函数

![image-20240208224434851](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240208224434851.png)

3.popitem()：随机删除和返回该键值对（返回值是元组）。

![image-20240208225024153](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240208225024153.png)

## 三十五：字典-序列解包用于列表元组字典

1.序列解包可以用于元组，列表，字典

 ![image-20240208225652915](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240208225652915.png)

2.序列解包用于字典时，默认是对“键”进行操作；如果需要对键值对操作，则需要使用items()；

如果需要对值进行操作，则需要使用values()；

![image-20240210213853833](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210213853833.png)

## 三十六：字典-复杂表格数据存储-列表和字典综合嵌套

![image-20240210233631449](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210233631449.png)



![image-20240210233639021](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210233639021.png)

## 三十七：集合-特点-创建和删除-交集并集差集运算

集合是无序可变，元素不能重复。实际上，集合底层是字典实现，集合的所有元素都是字典中的“键对象”，因此是不能重复的且唯一的。

1.使用{}创建集合对象，并使用add()方法添加元素

![image-20240210235155946](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210235155946.png)

2.使用set()，将列表，元组等可迭代对象转成集合。如果原来数据存在重复数据，则只保留一个。

![image-20240210235319098](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210235319098.png)

3.remove()删除指定元素；clear()清空整个集合

![image-20240210235354964](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210235354964.png)

4.集合相关操作

![image-20240210235743852](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240210235743852.png)

## 三十八：控制语句和现实逻辑表达

1.控制语句和逻辑思维：和c语言一致

## 三十九：单分支选择结构-条件表达式详解

1.if语句单分支结构的语法形式如下：

![image-20240211000843951](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240211000843951.png)

![image-20240213203134442](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213203134442.png)

![](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213203134442.png)

2.在选择和循环结构中，条件表达式的值为False的情况如下：

![image-20240213203507597](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213203507597.png)

其他情况，均为True。

3.**这么看来，Python所有的合法表达式都可以看做条件表达式，甚至包括函数调用的表达式。**

![image-20240213203646563](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213203646563.png)



## 四十：双分支结构-三元运算符的使用详解

1.语法结构：

![image-20240213204646361](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213204646361.png)

*其余与单分支一致*

2.三元条件运算符：

![image-20240213205200506](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213205200506.png)



![image-20240213205206477](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213205206477.png)



## 四十一：多分支选择结构

1.多分支选择结构的语法格式如下：

![image-20240213205604005](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213205604005.png)

*注：计算机行业，描述语法格式时，使用中括号[]通常表示可选，非必选。*

## 四十二：while循环结构-死循环处理

1.while循环的语法结构：

![image-20240213211102740](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213211102740.png)



## 四十三：for循环结构-遍历各种可迭代对象-range对象

1.语法格式：

![image-20240213211637444](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213211637444.png)

2.可迭代对象：序列（字符串，列表，元组），字典，迭代器对象，生成器函数，文件对象

![image-20240213211844354](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213211844354.png)

![image-20240213211851502](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213211851502.png)

3.range对象：range对象是一个迭代器对象，用来产生指定范围的数字序列，格式为：

![image-20240213212348558](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213212348558.png)

![image-20240213212438804](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240213212438804.png)

## 四十四：break语句

1.用于结束循环，当有嵌套循环时，break语句只能跳出最近一层的循环。

## 四十五：continue语句

结束本次循环，继续下一次。多个循环嵌套式，continue也是应用于最近的一层循环。

## 四十六：循环中的else子句

while，for循环可以附带一个else语句（可选）。如果for，while语句没有被break语句结束，则会执行else子句，否则不执行。

![image-20240220202754931](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240220202754931.png)



![image-20240220211348551](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240220211348551.png)



未录入四名员工：

![image-20240221145716302](C:\Users\彦祖\AppData\Roaming\Typora\typora-user-images\image-20240221145716302.png)

录入四名员工：

![image-20240221145735666](C:\Users\彦祖\AppData\Roaming\Typora\typora-user-images\image-20240221145735666.png)

## 四十七：zip()并行迭代多个序列

1.我们可以通过zip()函数对多个序列进行迭代，zip()函数在最短序列“用完”时就会停止。

![image-20240221150450770](C:\Users\彦祖\AppData\Roaming\Typora\typora-user-images\image-20240221150450770.png)

执行结果：

![image-20240221150507325](C:\Users\彦祖\AppData\Roaming\Typora\typora-user-images\image-20240221150507325.png)

## 四十八：推导式创建序列-列表推导式-字典推导式-集合推导式-生成器推导式

1.列表推导式：

![image-20240221214024788](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221214024788.png)

![image-20240221214031569](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221214031569.png)

2.字典推导式：

![image-20240221214617050](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221214617050.png)

![image-20240221214623992](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221214623992.png)

![image-20240221214629838](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221214629838.png)

3.集合推导式：

![image-20240221215556557](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221215556557.png)

![image-20240221215602262](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221215602262.png)

 4.生成器推导式发（不直接生成元组）：

1.![image-20240221223938338](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221223938338.png)

*提示是“一个生成器对象”。显然，元组是没有推导式的。*

*一个生成器只能运行一次。第一次迭代可以得到数据，第二次迭代发现数据已经没有了*

![image-20240221224109721](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221224109721.png)

第二次不会输出任何东西

## 四十九：函数的基本概念-内存分析-函数分类-定义和调用

1.在python中，定义函数的语法如下：

```python
def 函数名([参数列表]) :
    "文档字符串" #函数的注释
    函数体/若干语句
```

![image-20240221230526528](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240221230526528.png)

## 五十：返回值详解

1.如果函数体中包含return语句，则结束函数执行并返回值。

2.如果函数体中不包含return语句，则返回None值。

3.要返回多个值，使用列表，元组，字典，集合将多个值’存起来‘即可。

## 五十一：变量作用域-全局变量-局部变量-栈帧内存分析详解

1.全局变量：在函数和类定义之外的声明的变量。

​                        在函数内要改变全局变量的值，使用**global**声明一下。

2.局部变量：如果局部变量和全局变量同名，则在函数内隐藏全局变量，只使用同名的局部变量。

![image-20240222221703169](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222221703169.png)

![image-20240222221707612](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222221707612.png)

## 五十二：参数的传递-传递不可变对象

1.不可变对象：int,float,字符串，元组，布尔值

![image-20240222222621602](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222222621602.png)

*若函数内没有进行任何赋值操作，则a的地址不变*

## 五十三：浅拷贝和深拷贝

1.浅拷贝：拷贝对象，但不拷贝子对象的内容，只是拷贝子对象的引用。

2.深拷贝：拷贝对象，并且会连子对象的内存也全部（递归）拷贝一份，对子对象的修改不会影响源对象。

**浅拷贝：**

![image-20240222224004493](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222224004493.png)



![image-20240222224012374](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222224012374.png)

**深拷贝：**

![image-20240222225540049](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222225540049.png)



![image-20240222225548454](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222225548454.png)

## 五十三：参数的传递-不可变对象含可变子对象

1.元组中包含列表：

![image-20240302172728402](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302172728402.png)

![image-20240222230454337](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240222230454337.png)

**对象地址没变**

## 五十四：参数的类型-默认值参数-命名参数

1.默认值参数：如果没有传递数值，则默认为默认值，传递了数值则为传递值。

![image-20240302204342272](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302204342272.png)

2.命名参数：

![image-20240302204735111](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302204735111.png)

## 五十五：参数的类型-可变参数-强制命名参数

1. **‘*’号只能放在最后面，除非使用强制命名参数，不然会报错。**
2. ![image-20240302211042799](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302211042799.png)
3. ![image-20240302211051857](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302211051857.png)

a.一个 * 号：将多个参数收集到一个“元组”对象中。

b.两个 * 号：建 多个参数收集到一个“字典”对象中。

![image-20240302210309419](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302210309419.png)



![image-20240302210322335](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240302210322335.png)

## 五十六：lambda表达式和匿名函数

1.lambda表达式：lambda表达式只允许包含一个表达式，不能包含复杂语，该表达式的计算结果就是函数的返回值。

![image-20240303005904592](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303005904592.png)



![image-20240303005911422](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303005911422.png)

列表形式：

![image-20240303154854705](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303154854705.png)



## 五十七：eval()函数的用法和注入安全隐患问题

1.功能：将字符串str当成有效的表达式来求值并且返回计算结果，因此会被注入安全隐患。比如：字符串中含有删除文件的语句。 

![image-20240303160139329](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303160139329.png)

![image-20240303160150287](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303160150287.png)

## 五十八：递归函数-内存分析-栈帧的创建

1.和c语言思想基本一致。

![image-20240303161042948](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303161042948.png)

![image-20240303161052078](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240303161052078.png)

*5的阶乘*：

![image-20240304210524837](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304210524837.png)

![](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304210524837.png)

## 五十九：嵌套函数-内部函数-数据隐藏

1.嵌套函数：在函数内部嵌套的函数（**在函数内部定义的函数只能在此函数内部使用，函数外部调用不了**）。

## 六十：nonlocal和global关键字

1：nonlocal用来在内部函数中，声明外层的局部变量。global用于函数内声明全局变量，然后才使用全局变量。

![image-20240304212630519](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304212630519.png)



![image-20240304212642874](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304212642874.png)

## 六十一：LEGB规则

python在查找“名称”时，是按照LEGB规则查找的：

![image-20240304213007440](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304213007440.png)

**local**指的是函数或者类的方法内部

**Enclosed**指的是嵌套函数

**Global**指的是模块中的全局变量

**Built in**指的是python为自己保留的特殊名称

![image-20240304213154114](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304213154114.png)

*如果在inner函数内有变量 s ，则打印inner中的 s ，inner中没有，则搜索outer中的变量 s ，一层一层往外找。

## 六十二：类的定义-类和对象的关系-对象的内存模型

1.类可以看作时一个模板，或者图纸，系统根据类的定义来造出对象。

某个类的对象，某个类的实例，是一样的意思



2.*属性和方法*：我们通过类定义数据类型的属性（数据）和方法（行为），也就是说，“类将行为和状态打包在一起”。对象是类的具体实体。

![image-20240304215018948](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240304215018948.png)



*从一个类创建对象时，每个对象会共享这个类的行为，但会有自己的属性值。*（**方法代码是共享的，属性数据不共享**）

3.定义类的语法格式如下：

```python
class 类名:
    类体
```

要点如下：

a.类名必须符合“标识符”规则。

b.类体中我们可以定义属性和方法。

c.属性用来描述数据，方法（函数）用来描述这些数据相关的操作。

```py
class Student:
    def __init__(self,name,score): #__init__初始化属性，使得后面的函数可以调用主函数传递过来的参数。
		self.name=name 
        self.score=score
    def say_score(self):
        pass
s1=Student("Lancy",18)
```

输出结果：

```py
Lancy 18
```

## 六十三：构造函数-init和new的方法

1.初始化对象，我们需要定义构造函数__ init__()方法。构造方法用于执行“=实例对象的初始化工作”，即对象创建后，初始化当前对象的相关属性，无返回值。

2.__ init __()要点：

**名称固定，必须为__ init __()**

**第一个参数固定，必须为：self。self值得就是刚刚创建好的实例对象**

**构造函数通常用来舒适化实例对象的实例属性，如下代码就是初始化实例属性：name和score**

```python
def __init__(self,name,score):
    self.name=name
    self.score=score
```

**通过类名（参数列表）来调用构造函数。调用后，将创建好的对象，返回给相应的变量**



**__ init __()：初始化创建好的对象，即给实例属性赋值。**

**__ new __(): 用于创建对象，但一般无需重定义该方法**

**如果不定义__ init __方法，系统会提供一个默认的 _ _ init _ _方法**



## 六十四：实例属性

1.实例属  性一般  在_ _ init _ _()方法中通过如下代码进行定义：

```python
self 实例属性名 = 初始值
```

2.创建实例对象后，通过实例对象访问：

**obj01 = 类名()   #创建和初始化对象，调用_ _init _ _()初始化属性**

**obj01.实例属性名 = 值  #可以给已有属性赋值，也可以新加属性**

3.

![image-20240305200632512](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240305200632512.png)



运行结果：

![image-20240305200722974](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240305200722974.png)

**在类外部新加属性：**

![image-20240305200823216](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240305200823216.png)



## 六十五：实例方法-内存分析方法调用过程

1.实例方法是从属于实例对象的方法。实例方法的定义格式如下：

```py
def 方法名(self,[,形参列表]):
    函数体
```

**定义实例方法时，第一个参数必须为self。和前面一样，self指当前的实例对象。**

**调用实例方法时，不需要也不能给self传参。self由解释器自动传参**。

2.实例对象的方法调用本质：

![image-20240305202315415](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240305202315415.png)

3.其他操作：

**dir(obj)可以获得对象的所有属性，方法**

**obj._ _dict _ _对象的属性字典**

**pass空语句**

**isinstanace(对象，类型）判断"对象"是不是“指定类型.返回值时True或False”**

## 六十六：类对象

1.当解释器执行**class**语句时，就会创建一个类对象。

![image-20240305203555256](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240305203555256.png)

![image-20240305203603566](https://lytypora.oss-cn-guangzhou.aliyuncs.com/image-20240305203603566.png)



