# 前言
欢迎来到编程的世界，本教程致力于将课堂中繁杂晦涩的知识点，用通俗易懂的语言表述出来，鉴于我能力有限，难免会有错误和遗漏，一切以教学内容为主(除了谭浩强的书)。还有一点，本教程更新将会跟目前教学进度同步，也就是会比上课的内容慢一点，要是预习请访问[这个网站](https://www.runoob.com/cprogramming/c-tutorial.html)。想深入更多？欢迎了解[信息学竞赛内容](https://oi-wiki.org/)。


------------
# 环境配置

想让代码在电脑上运行起来？这对于新手来说是个挺复杂的问题。在Android上有相关的软件，直接下载就行了。
### Windows
本部分只针对 Windows 10 编写，其他系统请参照官方文档，或者[点这里给我发邮件](mailto:anine09@pm.me)。由于你还没有买电脑，我们暂时跳过这一部分。


------------
# 第一行代码
在配置好环境之后，我们就可以写下我们的第一行代码了。在这里我介绍个程序员的传统，一般在新电脑配置好之后，我们的第一行代码都是 _Hello，World！_ 用来检查环境是否配置成功，代码是否可以正常运行。下面我们就以 _Hello，World！_ 的代码为例，进行讲解。 
```c
#include<stdio.h>

int main(){
    
    printf("Hello，World！");

    return 0;
}
```
你以后会很清楚的看见，我写的代码会跟书上的空格换行符号啥的不太一样，这是我的编码风格，只是为了简洁好看，不影响程序运行。   
### 头文件

首先我们来看第一行代码
```c
#include<stdio.h>
```
这行代码表示，我要借用一个工具箱，工具箱的名字叫  _**stdio.h**_ ，它是个**头文件**（ .h 代表 head ） ， _**stdio**_ 其实就是 **Standard Input Output （标准输入输出）** 的简写，我们不需要死盯概念，这是我认为初学者不好学 C 语言的问题所在，一开头就乱七八糟的专有名词，搞得大家都没兴趣继续学下去了。  

我们这样理解，写程序会用到一些别人早就帮我们写好的代码，这个概念你以后会经常用到，就是：我们会经常用别人早就写好的代码。在业内有句话：**“不要重复发明轮子。”** 所以，引用别人的代码是件习以为常的事情。回到这个地方,  _**#include<XXX.h>**_ 就相当于告诉计算机，我需要借用一个叫做 **XXX.h** 的工具箱，现在在这个程序中，工具箱的名字就是 _**stdio.h**_，这个工具箱里面包含了你以后会经常用到的两个工具（当然它里面不止两个工具，我们以后可能会深入讨论它） ， _**printf()**_ 和 _**scanf()**_，放心，我后面肯定会详细介绍它们的，再给你预告一下，你以后可能会经常用到另一个工具箱，叫做 _**math.h**_，“箱”如其名，它里面有很多跟数学有关的工具。那么我们怎么使用它呢，当然是依葫芦画瓢啦。把**下面的代码**写在**开头**，第一行啊第二行这种位置，只要保证它在 _**int main()**_ 的前面就行了。
```c
#include<math.h>
```
### 程序入口
第二行代码是
```c
int main(){


}
```
在英语中，**main** 有 **主要的** 的意思，所以我们习惯把 _**main()**_ 称为主函数。这里的概念有些复杂，我打算留到后面讲，目前你需要了解：C语言的代码都是从 _**main()**_ 的花括号 **{ }** 中的内容开始的，也就是说， _**int main(){XXX}**_ 中的 **XXX** 将是第一行被运行的代码，OK，我们甚至也不需要了解这个概念，在后面编译的 part 我们会更深入的讨论这个问题。**注意！！！ 不要把 main() 写成 mian() 不要写成 面函数，人家叫主函数，** 实在是见过太多人这样写了，一弄反，程序就会报一大堆乱七八糟的你暂时还看不懂的英文出来，多注意一下，我相信你是个很细心的人。
### 主函数返回值
还有个代码，它是长这样的：
```c
return 0;
```
每一个函数都有返回值，就像数学的函数代值进去能算出 **y** 一样。这句话代表着使用 _**main()**_ 函数后，计算机会回馈个 0 给你，来表示你的程序是正常的结束了，当然，你不用特殊手段是**看不到这个 0 的**，目前我们不必深究这个，后面我会详细讲解。**不要忘了结尾有个分号 ";"。**
### 模板
这个是一个好习惯，我希望你每次写 C 语言的时候，能想都不想的先打出下面的代码。
```c
#include<stdio.h>

int main(){


    return 0;
}
```
相信我，多练习几次，多打几次，手就记下来了，很有用。**不要忘了分号。**
### 输出函数
看看这行代码
```c
printf("Hello,World!");
```

输出有多种形式和方法，叫 _**printf()**_ 输出函数其实不严谨，不然我们叫它**打印函数**吧哈哈哈哈，它的功能就是把你写在 **引号里 "XXX"** 的一些**XXX**，显示在那个黑不溜秋的框框里面，一般我们会写 **Hello,World!** 这是我们的传统。讲个笑话，我们 C 语言的老师把 **World** 写成了 **Word** 。

![Hello Word](https://z3.ax1x.com/2021/10/28/5byBM4.png)
你可能在书上看到的更多的是这个代码：

```c
prinf("Hello,World!\n");
```
这里的 _**\n**_，是一种**转义符**，代表将光标另起一行，就跟你打完字按个回车的效果一样。本着不必要就不多讲的原则，我们先不用了解**转义符**的概念，后面有的是时间讲。  
我们回到 _**printf()**_ 的上面去。你说这个 **print** 我认识，不就是**打印**嘛。但是它为什么要写成 **printf** 啊，看着特别别扭。其实这个 **f** 代表的是格式化的意思 **format。** 我们可以类比下之前稍微提过一次的  _**scanf()**_  函数，它也是英语单词 **扫描** 加了个格式化（**scan + f**）。什么叫**格式化输入输出**我们以后会很详细的讨论。**不要忘了结尾要写分号！**
### 小结
我们好不容易能够读懂了第一个程序，