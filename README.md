# A-little-guessing-game
猜数小游戏-对random,sys，datetime模块的使用，以及对于函数及封装练习
任务描述
一、语言和环境

1、实现语言：Python语言

2、版本：Python3.6或Python3.6以上版本

3、环境要求及开发工具：Pycharm

二、程序整体要求

1、 划分功能模块，日志文件用以进行游戏过程中信息记录，主程序用以进行代码编写

2、 函数的定义要清楚易懂，代码结构要层次分明，代码中可添加必要的注释

3、 程序中的函数名、变量名、参数名称要符合命名规范

4、 程序运行效果与提供的页面效果图、结构保持一致，提示中的分隔符（“*”）数量不做统一要求，文字大小、背景色也不做统一要求

5、 将作业项目形成压缩文件并提交

三、思路分析：

由题目要求和运行效果，可分析出项目划分为两大模块：mooc_test.py和record.txt

前者主要完成游戏后台逻辑的控制，并进行如效果图所示的功能点的补充（要求编码时注意函数抽取思想的应用）：

1、自定义游戏进入提示函数guide_page(guide_word)：

     功能描述： 提示玩家进入游戏，并输出如效果图标题的所示信息， 要求：

        （1）设置参数guide_word，记录要输出的标题文字信息

        （2）运用字符串的格式化函数（format），拼接“*”号和标题文字信息

        （3）符合程序运行效果图中标题的样式进行输出（注：“*”号的数量不作统一限制）

2、自定义数字类型判断函数all_num(n)：

     功能描述：判断指定的值是否为数字，要求：

        （1）设置参数n接收用于进行判定的变量的值

        （2）运用isdigit( )方法进行判定并返回其判定结果 

3、自定义数值合法性判定函数num_legal(ls)：

     功能描述：判定指定序列中的数值是否相等以及记录数字区间起始位置的值是否大于记录数字区间终止位置的值，要求：

        （1）设置列表类型的参数用于接收指定的序列

        （2）取出序列中的值并进行比较：

                     若两者相等，则退出程序，并提示玩家重新启动程序；

                     若表示数字区间起始位置的值大于数字区间终止位置的值，则退出程序，并提示玩家重新启动程序；

                     反之，则返回值为1

          注意：导入sys模块，sys.exit()即退出程序

4、自定义产生指定区间随机数函数set_final_num(num1,num2)：

     功能描述：根据参数值，产生一个位于参数值区间以内的随机数， 要求：

       （1）设置两个参数用于接收用户所输入区间的起始值和终止值，并将其保存至列表中

       （2）利用内置函数filter()及思路分析2中的all_num(n)过滤以确保输入值全部为数字

       （3）依据（2）中过滤后的返回值进行判断，若全部为数字，则调用自定义的等值判断函数，判断输入值是否相等，并根据判断之后的返回值，输出用户产生随机数的区间，并运用random模块，返回产生区间内的随机数；反之则提示玩家所输入的为非数字字符，请重新启动

5、自定义核查数值是否属于指定区间函数check_num_legal(num)：

     功能描述：判定所输入的数值是否在指定的区间

     要求：依据输入的数字区间起始值和终止值，利用条件语句判断输入数值是否在指定区间，若不在该区间内，则提示玩家所输入的数字未在指定区间

6、自定义日志写入函数write_record(times,value)：

     功能描述：将玩家每一次猜测数字和本次猜测次数两项信息写入日志文件，要求：

     （1）设置参数接收玩家猜测的次数（times）和本次猜测的具体数字(value)

     （2）根据datetime模块获取玩家进行每一次猜测数字输入的时间

     （3）使用with语法操作日志文件，将获取到的参数和时间信息以追加方式写入日志文件

8、自定义main(rand1)函数：

     功能描述：依据所产生的随机数字(rand1)，提示玩家输入猜测数字并进行比对直到猜测到正确数字， 要求：

     （1）设置变量temp接收已产生的随机数字，记录猜测数字的次数（默认为0） 

     （2）设置无限循环：                             

                                 1.提示用户输入所猜测数字，并转换为int类型 

                                 2.if判断核查数值函数，如果为真，则输出对不起您输入的数字未在指定区间！！！，跳过本次循环

                                 3.实现用户输入一次猜测数字，次数+1

                                 4.调用日志写入函数，传入猜测的次数和用户猜测的数字

                                 5.使用if语句判断用户猜测的数字，相等，大于，小于的情况，并输出如效果图所示的提示信息

9、控制程序逻辑执行流程（if __name__ == '__main__':）：

     功能描述：依据效果图，调用自定义函数实现对应的功能

     要求：

              （1）调用guide_page(  )输出如效果图所示的标题信息

              （2）设置两个变量（i，j）分别接收用户输入数字区间的起始值和终止值

              （3）调用set_final_num( )函数得到随机数

              （4）调用main( )执行程序流程

项目教程地址：https://blog.csdn.net/qq_38570633/article/details/106195873


