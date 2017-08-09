### 练习2.1

>  类型int, long, long long和short的区别是什么？ 无符号类型和带符号类型的区别是什么？float 和 double的区别是什么?

答：都属于整型， 区别是C++标准规定的尺寸的最小值不同， short为短整型，16位；int位整型，16位；long和long long为长整型，32位和64位。

无符号类型仅能表示大于等于0的数；带符号类型最高位用于表示符号，其余位表示数字，可表示负数，0，正数

float和double分别位单精度浮点数和双精度浮点数，区别在于内存中所占的比特数不同，以及默认规定的有效位数不同。

### 练习2.2

> 计算按揭贷款时，对于利率、本金、付款分别应选择何种数据类型？说明你的理由

答： 实际运用中，利率、本金、付款都既可能是整型也可能是浮点型，所以应该选择浮点类型来表示；而一共有三种浮点类型float ,double, long double。float 和double的计算代价比较接近，而double能表示的范围更广，long double计算代价相对过大，所以建议选择double 类型。

### 练习2.3

> 读程序结果:

```c++
unsigned u = 10, u2 = 42;
std::cout << u2 - u << std::endl;
std::cout << u - u2 << std::endl;
int i = 10, i2 = 42;
std::cout << i2 - i << std::endl;
std::cout << i - i2 << std::endl;
std::cout << i - u << std::endl; //这里有符号数会转为无符号数后再计算
std::cout << u - i << std::endl; //同上
```

答：

```json
32
4294967264
32
-32
0
0

```



