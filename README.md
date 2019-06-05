# Git-Test
## Java 基本数据类型 ###

### 1. 内置数据类型 ###

Java语言提供了八种基本类型。六种数字类型（四个整数型，两个浮点型），一种字符类型，还有一种布尔型。
- 获取某一类型占用的字节数`Byte.SIZE` (包装类.SIZE)

1.`byte`：
- 包装类：`java.lang.Bype`
- byte 数据类型是8位、有符号的，以二进制补码表示的整数；
- 最小值是 `Bype.MIN_VALUE = -128(-2^7)`
- 最大值是 `Bype.MAX_VALUE = 127(2^7-1)`
- 默认值是 `0`；
- byte 类型用在大型数组中节约空间，主要代替整数，因为 byte 变量占用的空间只有 int 类型的四分之一；
- 例子：`byte a = 100，byte b = -50`。

2.`short`：
- 包装类：`java.lang.Short`
- short 数据类型是 16 位、有符号的以二进制补码表示的整数
- 最小值是 `Short.MIN_VALUE = -32768(-2^15)`
- 最大值是 `Short.MAX_VALUE = 32767(2^15-1)`
- Short 数据类型也可以像 byte 那样节省空间。一个short变量是int型变量所占空间的二分之一；
- 默认值是 `0`；
- 例子：`short s = 1000，short r = -20000`。

3.`int`：
- 包装类：`java.lang.Integer`
- int 数据类型是32位、有符号的以二进制补码表示的整数；
- 最小值是 `Integer.MIN_VALUE = -2,147,483,648(-2^31)`
- 最大值是 `Integer.MAX_VALUE = 2,147,483,647(2^31-1)`
- 一般地整型变量默认为 int 类型；
- 默认值是 `0` ；
- 例子：`int a = 100000, int b = -200000`。

4.`long`：
- 包装类：`java.lang.Long`
- long 数据类型是 64 位、有符号的以二进制补码表示的整数；
- 最小值是 -9,223,372,036,854,775,808（-2^63）；
- 最大值是 9,223,372,036,854,775,807（2^63 -1）；
- 这种类型主要使用在需要比较大整数的系统上；
- 默认值是 `0L`；
- 例子： `long a = 100000L，Long b = -200000L`。
- "L"理论上不分大小写，但是若写成"l"容易与数字"1"混淆，不容易分辩。所以最好大写。

5.`float`：
- 包装类：`java.lang.Float`
- float 数据类型是单精度、32位、符合IEEE 754标准的浮点数；
- float 在储存大型浮点数组的时候可节省内存空间；
- 默认值是 `0.0f`；
- 浮点数不能用来表示精确的值，如货币；
- 例子：`float f1 = 234.5f`。

6.`double`：
- 包装类：`java.lang.Double`
- double 数据类型是双精度、64 位、符合IEEE 754标准的浮点数；
- 浮点数的默认类型为double类型；
- double类型同样不能表示精确的值，如货币；
- 默认值是 `0.0d`；
- 例子：`double d1 = 123.4`。

7.`boolean`：
- 包装类：`java.lang.Boolean`
- boolean数据类型表示一位的信息；
- 只有两个取值：`true` 和 `false`；
- 这种类型只作为一种标志来记录 true/false 情况；
- 默认值是 `false`；
- 例子：`boolean one = true`。

8.`char`：
- 包装类：`java.lang.Character`
- char类型是一个单一的 16 位 Unicode 字符；
- 最小值是 `\u0000`（即为`0`），也是默认值；
- 最大值是 `\uffff`（即为`65535`）；
- char 数据类型可以储存任何字符；
- 例子：`char letter = 'A'`。

### 2. 引用类型 ###
> 在Java中，引用类型的变量非常类似于C/C++的指针。引用类型指向一个对象，指向对象的变量是引用变量。这些变量在声明时被指定为一个特定的类型，比如 Employee、Puppy 等。变量一旦声明后，类型就不能被改变了。
- 对象、数组都是引用数据类型。
- 所有引用类型的默认值都是null。
- 一个引用变量可以用来引用任何与之兼容的类型。
- 例子：`Site site = new Site("site")`

## 常量修饰符 ##
> 常量在程序运行时是不能被修改的，强制修改报错。
- 在 Java 中使用 final 关键字来修饰常量，声明方式和变量类似：
 ``` final int _CONST = 12; ```
### 字符串常量 ###
> 字符串常量和字符常量都可以包含任何Unicode字符。例如：
- `char a = '\u0001';`
- `String a = "\u0001";`
## 变量的其他进制表示 ##
类型| 8进制 |  16进制 | 例子|
-|-|-|-
byte| 0开头 | 0x开头 |014, 0x10|
int| 0开头 |  0x开头|0144, 0x65|
long| 0开头 | 0x开头 |0144, 0x65|
short| 0开头 | 0x开头 |0144, 0x65|

## 转义字符 ##
符号| 含义 
-|-|-|-
\\n	|换行 (0x0a)
\\r	|回车 (0x0d)
\\f	|换页符(0x0c)
\\b	|退格 (0x08)
\\0	|空字符 (0x20)
\\s	|字符串
\\t	|制表符
\\"	|双引号
\\'	|单引号
\\\	|反斜杠
\\ddd	|八进制字符 (ddd)
\\uxxxx	|16进制Unicode字符 (xxxx)

## Java修饰符 ##
> 像其他语言一样，Java可以使用修饰符来修饰类中方法和属性。主要有两类修饰符：

- 访问控制修饰符 : default, public , protected, private
- 非访问控制修饰符 : final, abstract, static, synchronized
