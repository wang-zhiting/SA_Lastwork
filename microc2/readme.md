# Microcc
---
- 课程名称：编程语言原理与编译
- 实验项目：期末大作业
- 专业班级：计算机1801
- 学生学号：31801071，31801069
- 学生姓名：周宇超，林凯达
- 实验指导教师: 郭鸣
---

## 简介
这是一个编译原理大作业，主要基于microC完成的。

本次大作业，我们在解释器中做了大量的尝试，实现了for循环，i++，i--，注释功能，我们按照自己的思路设计词法分析器，语法分析器，以及解释器。


## 结构
- 前端：由`F#`语言编写而成  
  - `Clex.fsl`生成的`Clex.fs`词法分析器。
  - `CPar.fsy`生成的`Cpar.fs`语法分析器。
  - `Absyn.fs` 定义了抽象语法树
  - `interp.fs`解释器
  - `Contcomp.fs`编译器


- 测试集：测试程序为ex1.c——ex4.c


## 用法
- ` dotnet restore  interpc.fsproj `
- ` dotnet clean  interpc.fsproj  `
- ` dotnet build -v n interpc.fsproj  `
构建解释器 
- ` dotnet run -p interpc.fsproj ex1.c 0`
测试i++,i--
- ` dotnet run -p interpc.fsproj ex2.c 0`
测试for循环
- ` dotnet run -p interpc.fsproj ex3.c 0`
测试注释
- ` dotnet run -p interpc.fsproj ex4.c 0`
测试三目运算符


## 功能实现

### 改进列表：

1. 修改注释表示方式，将注释  /*   */改为(* * *)
2. 修改标识符定义，类型名称以大写开头，包括Int，Char
3. 增加关键字for
4. 增加标识符 ++  -- ：
5. 增加for循环
7. 增加i++和i--
8. 增加三目运算符  表达式：


### 用例说明：

1.ex1.c用到i++和i--

2.ex2.c用到for循环

3.ex3.c用到注释

4.ex4.c用到三目运算符


	- ex1.c代码  


  - ex1.c代码 
    
  - void main(Int n) {
    
     n++;
     
     print n;
     
    }
    
  - 语法树及运行结果 
    
    ![image-20210630145510103](C:\Users\billy\AppData\Roaming\Typora\typora-user-images\image-20210630145510103.png)


  - ex2.c代码  
    
  - void main(Int n){
    
    Int i;
  
    for(i=0;i<n;i++){
  
     print i;
  
    }

  }

  - 语法树及运行结果 

  - ![image-20210630145827739](C:\Users\billy\AppData\Roaming\Typora\typora-user-images\image-20210630145827739.png)


  - ex3.c代码  

  - void main(Int n){

      n=0;

      (*nnnnnnnnn*)

    }

  - 语法树及运行结果 

  - ![image-20210630150002966](C:\Users\billy\AppData\Roaming\Typora\typora-user-images\image-20210630150002966.png)


  - ex4.c代码  

  - void main(Int n) {

     n>10:n=1:n=2;

     print n;

    }

  - 语法树及运行结果 
    
  - ![image-20210630150121975](C:\Users\billy\AppData\Roaming\Typora\typora-user-images\image-20210630150121975.png)



 



## 心得体会
- 周宇超：  
    编译原理这门课很深奥，F#是一个完全没接触过的全新类型的语言，所以一切都得自己慢慢摸索和探索，通过本次编译原理大作业，加深了我对于计算本质的理解与运用。老师上课讲的很好，但是比较难理解，课后需要及时消化，遇到问题，老师也会耐心地解答。这次大作业让我受益匪浅，不仅锻炼了我独立思考的能力，还锻炼了小组内的团结互助，我也对编译原理有了初步的了解，编译原理的世界还是相当有趣的，希望今后我能更加深入地了解编译原理，以及加深对整个计算机上系统的深刻理解，让自己的知识和能力都更上一层楼！


- 林凯达：  
    在初学编译原理一个学期后，我们进行了对一种编译语言的学习和改进，尝试实现更多不同的功能。通过编译语言，了解到了程序设计语言编译程序构造的基本原理和设计方法。只有深入地了解了编译原理，才能让我更加了解计算机语言的形成，使我受益匪浅。

    
## 技术评价

| 功能 | 对应文件 | 优  | 良  | 中  |
| ---- | -------- | --- | --- | --- |
|i++、i--||√|||
|三目运算符||√|||
|for循环||√|||
|注释|||√||
## 小组分工

- 周宇超
  - 学号：31801069
  - 班级：计算机1801
    - 工作内容
      - 语法分析
      - 词法分析
      - 、for循环、注释、三目运算符
- 林凯达
  - 学号：31801071
  - 班级：计算机1801
    - 工作内容
      - 文档编写
      - 测试程序
      - i++，i--
  
- 权重分配表：  

| 周宇超 | 林凯达 |
| ------ | ------ |
| 0.95  | 0.95   |

![image-20210630160156351](C:\Users\billy\AppData\Roaming\Typora\typora-user-images\image-20210630160156351.png)