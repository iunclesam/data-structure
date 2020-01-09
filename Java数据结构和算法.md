# 数据结构和算法

## 数据结构和算法内容介绍

### 先看几个经典的算法面试题

#### 字符串匹配问题

1）有一个字符串 str1 = "硅硅谷 尚硅谷你尚硅 尚硅谷你尚硅谷你尚硅你好"，和一个子串 str2 = "尚硅谷你尚硅你"

2）现在要判断 str1 是否含有 str2，如果存在，就返回第一次出现的位置，如果没有，则返回 -1

3）要求用最快的速度来完成匹配

4）你的思路是什么？

暴力匹配：简单，但是效率低

KMP算法（部分匹配表）

#### 汉诺塔游戏

请完成汉诺塔游戏的代码，要求：

1）将A塔的所有圆盘移动到C塔，2）并规定在小圆盘上不能放大圆盘，3）在三根柱子之间一次只能移动一个圆盘

![](https://i.postimg.cc/yxVmgcLn/th-id-OIP.jpg)

使用到分治算法

http://brainmetrix.com/tower-of-hanoi/

#### 八皇后问题

是一个古老而著名的问题，是回溯算法的典型案例。该问题是国际西洋棋棋手马克斯·贝瑟尔于1848年提出：在8✖8格的国际象棋上摆放八个皇后，使其不能相互攻击，即任意两个皇后都不能处于同一行、同一列或同一斜线上，问有多少种摆法。

![](http://support.sas.com/documentation/cdl/en/orcpug/59630/HTML/default/images/queens.png)

使用到回溯法算法

高斯认为有76种方案。1854年在柏林的象棋杂志上不同的作者发表了40种不同的解，后来有人用图论的方法解出92种结果。计算机发明后，有多种计算机语言可以解决此问题

http://brainmetrix.com/8-queens

### 数据结构和算法的重要性

1）算法是程序的灵魂，优秀的程序可以在海里数据计算时，依然保持高速计算

2）一般来讲程序会使用内存计算框架（比如Spark）和缓存技术（比如Redis等）来优化程序，再深入的思考一下，这些计算框架和缓存技术，它的核心功能是哪个部分呢？

3）拿实际工作经历来说，在Unix下开发服务器程序，功能是要支持上千万人同时在线，在上线前，做内侧，一切OK，可上线后，服务器就支撑不住了，公司的CTO对代码进行优化，再次上线，坚如磐石。你能感受到程序是有灵魂的，就是算法。

4）目前程序员面试的门槛越来越高，很多一线IT公司（大厂），都会有数据结构和算法面试题（负责的告诉你，肯定有的）

5）如果你不想永远都是代码工人，那就花时间来研究下数据结构和算法

### 本套数据结构和算法内容介绍

...

### 课程亮点和授课方式

1）课程深入，非蜻蜓点水

2）课程成体系，非星星点灯

3）高效而愉快的学习，数据结构和算法很有用、很好玩

4）数据结构和算法很重要，但是相对困难，我们努力做到通俗易懂

5）采用 应用场景->数据结构或算法->剖析原理->分析实现步骤（图解）->代码实现 的步骤讲解 [比如：八皇后问题和动态规划算法]

6）课程目标：让大家掌握本质，到达能在工作中灵活运用解决实际问题和优化程序的目的.

## 数据结构和算法概述

### 数据结构和算法的关系

1）数据（data）结构（structure）是一门研究组织数据方式的学科，有了编程语言也就有了数据结构。学号数据结构可以编写出更加漂亮，更加有效率的代码。

2）要学习好数据结构就要多多考虑如何将生活中遇到的问题，用程序去实现解决。

3）程序 =  数据结构 + 算法

4）数据结构是算法的基础，换言之，想要学好算法，需要把数据结构学到位。

### 看几个实际编程中遇到的问题

#### String.replaceAll()方法

```java
public static void main(String[] args) {
    String str = "Java,Java, hello,world";
    String newStr = str.replaceAll("Java", "尚硅谷~"); //算法
    System.out.println("newStr=" + newStr)
}
```

问：试写出用**单链表**表示的字符串类及字符串节点类的定义，并依次实现它的构造函数、以及计算串长度，串赋值、判断两串相等、求子串、两串连接、求子串在串中位置等7个成员函数。

#### 一个五子棋程序

![](https://i.postimg.cc/Dw84S6dx/2019-12-22-4-50-57.png)

如何判读游戏的输赢？并可以完成存盘退出和继续上局的功能

1）棋盘->**二维数组**->**稀疏数组-**>写入文件【存档功能】

2）读取文件->稀疏数组->二维数组->棋盘【接上局】

#### 约瑟夫问题（丢手帕问题 ）

1）Josephu问题为：设编号为1，2，… n的n个人围坐一圈，约定编号为k（1 <= k <= n）的人从1开始报数，数到m的那个人出列，它的下一位又从1开始报数，数到m的那个人又出列，以此类推，直到所有人出列为止，由此产生一个出队编号的序列。

2）提示：用一个不带头结点的循环链表来处理Josephu问题：先构成一个有n个结点的单循环链表（**单向环形链表**），然后由k结点起从1开始计数，计到m时，对应结点从链表中删除，然后再从被删除结点的下一个结点又从1开始计数，直到最后一个结点从链表中删除算法结束。

![](https://i.postimg.cc/TPxNFsRh/2019-12-22-8-26-44.png)

3）小结：完成约瑟夫问题，需要使用到单向环形链表这个数据结构

#### 其他常见算法问题

- 磁盘问题

- 公交车

- 画图

- 矩阵中查找单词路径数

- 球和篮子

- 仍石头

- PlayCards

- 扑克牌组三张以上

  修路问题 -> 最小生成树（数据结构）+ 普里姆算法

  最短路径问题 -> 图 + 费洛伊德算法

  汉诺塔 -> 分治算法

  八皇后问题 ->回溯算法

### 线性结构和非线性结构

数据结构包括：线性结构和非线性结构

#### 线性结构

1）线性结构作为最常用的数据结构，其特点是数据元素之间存在一对一的线性关系

2）线性结构有两种不同的存储结构，即**顺序存储结构**（**数组**）和**链式存储结构**（**链表**）。顺序存储的线性表称为顺序表，顺序表中的**存储元素是连续**的

3）链式存储的线性表称为链表，链表中的**存储元素不一定是连续的**，元素节点中存放数据元素以及相邻元素的地址信息

4）线性结构常见的有：**数组**、**队列**、**链表和栈**，后面我们会详细讲解

#### 非线性结构

非线性结构包括：二维数组，多维数组，广义表、**树结构**、**图结构**

## 稀疏数组和队列

### 稀疏数组（sparse array）

#### 先看一个实际的需求

- 编写一个五子棋程序中，有存盘退出和续上盘的功能。

![](https://i.postimg.cc/zXqDW6x7/2019-12-22-10-57-33.png)

- 分析问题

  因为该二维数组的很多值是默认值0，因此记录了**很多没有意义的数据**->**稀疏数组**

#### 基本介绍

当一个数组中大部分元素为0，或者为同一个值的数组时，可以使用稀疏数组来保存该数组。

稀疏数组的处理方法是：

1）记录数组一共**有几行几列，有多少个不同**的值

2）把具有不同值得元素的行列及值记录在一个小规模的数组中，从而缩小程序的规模

- 稀疏数组举例说明

![](https://i.postimg.cc/ncJVkcJb/2019-12-23-12-22-55.png)

#### 应用实例

1）使用稀疏数组，来保留类似前面的二维数组（棋盘、地图等）

2）把稀疏数组存盘，并且可以从新恢复原来的二维数组

3）整体思路分析

![](https://i.postimg.cc/0NDZsfbB/2019-12-23-12-38-10.png)

- 二维数组 转 稀疏数组的思路
  1. 遍历原始的二维数组，得到有效数据的个数sum
  2. 根据sum就可以创建稀疏数组 sparseArr int\[sum + 1][3]
  3. 将二维数组的有效数据存入到稀疏数组
- 稀疏数组 转 原始二维数组的思路
  1. 先读取稀疏数组的第一行，根据第一行的数据，创建原始的二维数组，比如上面的 chessArr2  int\[11][11]
  2. 在读取稀疏数组后几行的数据，并赋值给原始的二维数组即可

4）代码实现

```java
package com.atguigu.sparsearray;

public class SparseArray {
    public static void main(String[] args) {
        // 创建一个原始的二维数组 11 * 11
        // 0：没有棋子，1：黑子 2：篮子
        int[][] chessArr1 = new int[11][11];

        chessArr1[1][2] = 1;
        chessArr1[2][3] = 2;
        chessArr1[4][5] = 2;

        System.out.println("原始的二维数组");
        for (int[] row : chessArr1) {
            for (int data : row) {
                System.out.printf("%d\t", data);
            }
            System.out.println();
        }

        // 二维数组 转 稀疏数组的思路
        // 1. 遍历原始的二维数组，得到有效数据的个数sum
        int sum = 0;
        for (int i = 0; i < 11; i++) {
            for (int j = 0; j < 11; j++) {
                if (chessArr1[i][j] != 0) {
                    sum++;
                }
            }
        }
        // 2. 根据sum就可以创建稀疏数组 sparseArr int[sum + 1][3]
        int[][] sparseArr = new int[sum + 1][3];
        sparseArr[0][0] = 11;
        sparseArr[0][1] = 11;
        sparseArr[0][2] = sum;
        // 3. 将二维数组的有效数据存入到稀疏数组
        int count = 0; // 用于记录是第几个非0数据
        for (int i = 0; i < 11; i++) {
            for (int j = 0; j < 11; j++) {
                if (chessArr1[i][j] != 0) {
                    count++;
                    sparseArr[count][0] = i;
                    sparseArr[count][1] = j;
                    sparseArr[count][2] = chessArr1[i][j];
                }
            }
        }

        System.out.println("得到稀疏数组为");
        for (int i = 0; i < sparseArr.length; i++) {
            System.out.printf("%d\t%d\t%d\t\n", sparseArr[i][0],sparseArr[i][1],sparseArr[i][2]);
        }

        // 稀疏数组 转 原始二维数组的思路
        // 1. 先读取稀疏数组的第一行，根据第一行的数据，创建原始的二维数组，比如上面的 chessArr2  int[11][11]
        int[][] chessArr2 = new int[sparseArr[0][0]][sparseArr[0][1]];
        // 2. 在读取稀疏数组后几行的数据，并赋值给原始的二维数组即可
        for (int i = 1; i < sparseArr.length; i++) {
            chessArr2[sparseArr[i][0]][sparseArr[i][1]] = sparseArr[i][2];
        }

        System.out.println("恢复后的二维数组");
        for (int[] row : chessArr2) {
            for (int data : row) {
                System.out.printf("%d\t", data);
            }
            System.out.println();
        }
    }
}

```

#### 课后练习

要求：

1）在前面的基础上，将稀疏数组保存到磁盘上，比如map.data

2）恢复原来的数组时，读取map.data进行恢复

### 队列

#### 队列的一个使用场景

银行排队的案例

![](https://i.postimg.cc/Y0MDk21h/2019-12-24-11-38-37.png)

#### 队列的介绍

1）队列是一个**有序列表**，可以用**数组**或是**链表**来实现。

2）遵循**先入先出**的原则。即：**先存入队列的数据，要先取出**。**后存入的要后取**出

3）示意图：（使用数组模拟队列示意图）

![](https://i.postimg.cc/3R50kdfJ/2019-12-24-11-44-42.png)



#### 数组模拟队列思路

- 队列本身是有序列表，若使用数组的结构来存储队列的数据，则队列数组的声明如下图，其中maxSize是该队列的最大容量。
- 因为队列的输出、输入是分别从前后端来处理，因此需要两个变量front及rear分别记录队列前后端的下标，front会随着数据输出而改变，而rear则是随着数据输入而改变，如图所示：

![](https://i.postimg.cc/c42G1b7M/2019-12-26-11-24-18.png)

- 当我们将数据存入队列时称为“addQueue”，addQueue的处理需要有两个步骤：思路分析

  1）将尾指针往后移：rear+1，当front==rear【空】

  2）若尾指针rear小于队列的最大下标maxSize-1，则将数据存入rear所指的数据元素中，否则无法存入数据。rear == maxSize - 1【队列满】

- 代码实现

  ```java
  package com.atguigu.queue;
  
  import java.util.Scanner;
  
  public class ArrayQueueDemo {
      public static void main(String[] args) {
          // 创建一个队列
          ArrayQueue queue = new ArrayQueue(3);
          char key = ' '; // 接收用户输入
          Scanner scanner = new Scanner(System.in);
          boolean loop = true;
          // 输出一个菜单
          while (loop) {
              System.out.println("s(show)：显示队列");
              System.out.println("e(exit)：退出程序");
              System.out.println("a(add)：添加数据到队列");
              System.out.println("g(get)：从队列取出数据");
              System.out.println("h(head)：查看队列头的数据");
              key = scanner.next().charAt(0); // 接收一个字符
              switch (key) {
                  case 's':
                      queue.showQueue();
                      break;
                  case 'a':
                      System.out.println("输出一个数");
                      int value = scanner.nextInt();
                      queue.addQueue(value);
                      break;
                  case 'g': // 取出数据
                      try {
                          int res = queue.getQueue();
                          System.out.printf("取出的数据是%d\n", res);
                      } catch (Exception e) {
                          e.printStackTrace();
                      }
                      break;
                  case 'h': // 查看队列头的数据
                      try {
                          int res = queue.headQueue();
                          System.out.printf("队列头的数据是%d\n", res);
                      } catch (Exception e) {
                          e.printStackTrace();
                      }
                      break;
                  case 'e': // 退出
                      scanner.close();
                      loop = false;
                      break;
                  default:
                          break;
              }
          }
          System.out.println("程序退出~");
      }
  }
  // 使用数组模拟队列-编写一个ArrayQueue类
  class ArrayQueue {
      private int maxSize; // 表示数组的最大容量
      private int front; // 队列头
      private int rear; // 队列尾
      private int[] arr; // 该数据用于存放数据，模拟队列
  
      // 创建
      public ArrayQueue(int maxSize) {
          this.maxSize = maxSize;
          arr = new int[maxSize];
          front = -1; // 指向队列头部，分析出front是指向队列头的前一个位置
          rear = -1; // 指向队列尾，指向队列尾的数据（即就是队列最后一个数据）
      }
  
      // 判断队列是否满
      public boolean isFull() {
          return rear == maxSize - 1;
      }
  
      // 判断队列是否为空
      public boolean isEmpty() {
          return rear == front;
      }
  
      // 添加数据到队列
      public void addQueue(int n) {
          // 判断队列是否满
          if (isFull()) {
              System.out.println("队列满，不能加入数据~");
              return;
          }
          rear++; // 让rear后移
          arr[rear] = n;
      }
  
      // 获取队列的数据，出队列
      public int getQueue() {
          // 判断队列是否空
          if (isEmpty()) {
              // 通过抛出异常
              throw new RuntimeException("队列空，不能取数据");
          }
          front++; // front后移
          return arr[front];
      }
  
      // 显示队列的所有数据
      public void showQueue() {
          // 遍历
          if (isEmpty()) {
              System.out.println("队列空的，没有数据~");
              return;
          }
  
          for (int i = 0; i < arr.length; i++) {
              System.out.printf("arr[%d]=%d\n", i, arr[i]);
          }
      }
  
      // 显示队列的头数据，注意不是取出数据
      public int headQueue() {
          // 判断
          if (isEmpty()) {
              throw new RuntimeException("队列空的，没有数据~");
          }
          return arr[front +1];
      }
  }
  ```

- 问题分析并优化

  1）目前数组使用一次就不能用，没有达到复用的效果

  2）将这个数组使用算法，改进成为一个环形的队列 取模(%)

#### 数组模拟环形队列

对前面的数组模拟队列的优化，充分利用数组，因此将数组看做一个环形的。（通过**取模的方式来实现**即可）

- 分析说明

  1）尾索引的下一个为头索引时表示队列满，即将队列容量空出一个作为约定，这个在做判断队列满的时候需要注意（rear + 1）% maxSize == front 【满】

  2）rear == front 【空】

  3）分析示意图

  ![](https://i.postimg.cc/j22PMvY1/2019-12-30-10-14-12.png)

  思路如下：

  1. front变量的含义做一个调整：front就指向队列的第一个元素，也就是说arr[front]就是队列的第一个元素front的初始值=0
  2. rear变量的含义做一个调整：rear指向队列的最后一个元素的后一个位置。因为希望空出一个空间作为约定，rear的初始值=0
  3. 当队列满时，条件是（rear + 1）% maxSize=front【满】
  4. 当队列为空的条件，rear==front【空】
  5. 当我们这样分析，队列中有效的数据的个数（rear + maxSize - front）% maxSize // rear=1 front=0
  6. 我们就可以在原来的队列上修改得到，一个环形队列

## 链表

### 链表介绍(Linked List)

链表是有序的列表，但是它在内存中是存储如下

![](https://i.postimg.cc/jqZzkKbG/2019-12-31-8-28-48.png)

小结上图：

1）链表是以结点的方式来存储，是**链式存储**

2）每个结点包含data域，next域（指向下一个结点）

3）如图，发现**链表的各个结点不一定是连续存储**

4）链表分**带头结点的链表**和**没有头结点的链表**，根据实际的需求来确定



- 单链表（带头结点）逻辑结构示意图如下

![](https://i.postimg.cc/mr34yBnn/2019-12-31-8-42-35.png)



### 单链表的应用实例

使用带head头的单向链表实现-水浒传英雄排行榜管理完成对英雄人物的增删改查操作，注：删除和修改、查找

可以考虑学员独立完成，也可带学员完成

1）第一种方法在添加英雄时，直接添加到链表的尾部

思路分析示意图：

单链表的创建示意图（**添加**），显示单向链表的分析

![](https://i.postimg.cc/8cpngVtj/2019-12-31-8-51-13.png)

```java
class HeroNode {
  int no;
  String name;
  String nickName;
  HeroNode next;
}
```

添加（创建）

1. 先创建一个head头结点，作用就是表示单链表的头
2. 后面我们每添加一个节点，就直接加入到链表的最后

遍历

1. 通过一个辅助变量遍历，帮助遍历整个链表

2）第二种方式在添加英雄，根据排名将英雄插入到指定位置（如果有这个排名，则添加失败，并给出提示）

思路分析示意图

![](https://i.postimg.cc/TPwdfp3X/2019-12-31-9-54-06.png)

需要按照编号的顺序添加

1. 首先找到新添加的节点位置，是通过辅助变量（指针），通过遍历来搞定
2. 新的节点.next=temp.next
3. 将temp.next=新的节点

3）修改节点

思路（1）先找到该节点，通过遍历（2）temp.name=newHeroNode.name; temp.nickname=newHeroNode.nickname

4）删除节点

思路分析的示意图

![](https://i.postimg.cc/Zn4BwS6R/2019-12-31-10-23-26.png)

从单链表中删除一个节点的思路

1. 我们先找到需要删除的这个节点的前一个节点temp
2. temp.next=temp.next.next
3. 被删除的节点，将不会用其他引用指向，会被垃圾回收机制回收

### 单链表面试题(新浪、百度、腾讯)

单链表的常见面试题有如下：

1）求单链表中有效节点的个数

代码如下：

```java
		/**
     * 获取到单链表的节点个数(如果是带头结点的链表，需求不统计头节点)
     * @param head 链表的头节点
     * @return 返回的就是有效节点的个数
     */
    public static int getLength(HeroNode head) {
        if (head.next == null) { // 空链表
            return 0;
        }
        int length = 0;
        // 定义一个辅助的变量，这里我们没有统计头节点
        HeroNode cur = head.next;
        while (cur != null) {
            length++;
            cur = cur.next; // 遍历
        }
        return length;
    }
```

2）查找单链表中的倒数第k个节点【新浪面试题】

代码演示：

```java
/**
     * 查找单链表中的倒数第k个结点【新浪面试题】
     * 思路
     * 1. 编写一个方法，接受head节点，同时接收一个index
     * 2. index表示是倒数第index个节点
     * 3. 先把链表从头到尾遍历，得到链表的总的长度getLength
     * 4. 得到size后，我们从链表的第一个开始遍历（size-index）个，就可以得到
     * 5. 如果找到了，则返回该节点，否则返回null
     */
    public static HeroNode findLastIndexNode(HeroNode head, int index) {
        // 判断如果链表为空，返回null
        if (head.next == null) {
            return null; // 没有找到
        }
        // 第一次遍历得到链表的长度(节点个数)
        int size = getLength(head);
        // 第二次遍历 size-index 位置，就是我们倒数的第k个节点
        // 先做一个 index 的校验
        if (index <= 0 || index > size) {
            return null;
        }
        // 定义给辅助变量，for循环定位到倒数的 index
        HeroNode cur = head.next; // 3 - 1 = 2
        for (int i = 0; i < size - index; i++) {
            cur = cur.next;
        }
        return cur;
    }
```

3）单链表的反转【腾讯面试题，有点难度】

- 思路分析图解

  ![](https://i.postimg.cc/3xtM1Zd4/2020-01-07-7-53-01.png)

思路：

1. 先定义一个节点reverseHead = new HeroNode();
2. 从头到尾遍历原来的链表，每遍历一个节点，就将其取出，并放在新的链表reverseHead的最前端
3. 原来的链表的head.next = reverseHead.next

![](https://i.postimg.cc/P5PKGbS8/2020-01-07-7-56-03.png)

- 代码实现

  ```java
  // 将单链表反转
      public static void reverseList(HeroNode head) {
          // 如果当前链表为空，或者只有一个节点，无需反转，直接返回
          if (head.next == null || head.next.next == null) {
              return;
          }
  
          // 定义一个辅助的指针(变量)，帮助我们遍历原来的链表
          HeroNode cur = head.next;
          HeroNode next = null; // 指向当前节点[cur]的下一个节点
          HeroNode reverseHead = new HeroNode(0, "", "");
  
          // 遍历原来的链表，每遍历一个节点，就将其取出，并放在新的链表reverseHead的最前端
          // 动脑筋
          while (cur != null) {
              next = cur.next; // 先暂时保存当前节点的下一个节点，因为后面需要使用
              cur.next = reverseHead.next; // 将cur的下一个节点指向新的链表的最前端
              reverseHead.next = cur; // 将cur连接到新的链表上
              cur = next; // 让cur后移
          }
          // 将head.next指向reverseHead.next，实现单链表的反转
          head.next = reverseHead.next;
      }
  ```

4）从尾到头打印单链表【百度，要求方式1：反向遍历 方式2：Stack栈】

- 思路分析图解

  ![](https://i.postimg.cc/PJHpyHRM/2020-01-07-8-03-55.png)

思路：

1. 上面的题的要求就是逆序打印单链表

2. 方式1：先将单链表进行反转操作，然后再遍历即可，这样做的问题是会破坏原来单链表的结构，不建议

3. 方式2：可以利用栈这个数据结构，将各个节点压入到栈中，然后利用栈的先进后出的特点，就实现了逆序打印的效果

   举例演示栈的使用 Stack

- 代码实现

  写了一个小程序，测试Stack的使用

  ```java
  package com.atguigu.linkedlist;
  
  import java.util.Stack;
  
  // 演示栈Stack的基本使用
  public class TestStack {
      public static void main(String[] args) {
          Stack<String> stack = new Stack<>();
          // 入栈
          stack.add("jack");
          stack.add("tom");
          stack.add("smith");
  
          // 出栈
          // smith，tom，jack
          while (stack.size() > 0) {
              System.out.println(stack.pop()); // pop就是将栈顶的数据取出
          }
      }
  }
  
  ```



  单链表的逆序打印代码：

  ```java
  // 可以利用栈这个数据结构，将各个节点压入到栈中，然后利用栈的先进后出的特点，就实现了逆序打印的效果
    public static void reversePrint(HeroNode head) {
        if (head.next == null) { // 空链表，不能打印
            return;
        }
        // 创建要给一个栈，将各个节点压入栈
        Stack<HeroNode> stack = new Stack<>();
        HeroNode cur = head.next;
        // 将链表的所有节点压入栈
        while (cur != null) {
            stack.push(cur);
            cur = cur.next; // cur后移，这样就可以压入下一个节点
        }
        // 将栈中的节点进行打印，pop出栈
        while (stack.size() > 0) {
            System.out.println(stack.pop()); // stack的特点是先进后出
        }
    }
  ```

5）合并两个有序的单链表，合并之后的链表依然有序【课后练习】

### 双向链表应用实例

#### 双向链表的操作分析和实现

使用带head头的双向链表实现--水浒英雄排行榜

- 管理单向链表的缺点分析

  1）单向链表，查找的方向只能是一个方向，而双向链表可以向前或者向后查找

  2）单向链表不能自我删除，需要辅助节点，而双向链表，则可以自我删除，所以前面我们单链表删除节点时，总是找到temp，temp是待删除节点的前一个节点（认真体会）

  3）分析了双向链表如何完成遍历，添加，修改和删除的思路

  ![](https://i.postimg.cc/50jJ091K/2020-01-08-7-51-34.png)

​	对上图的说明

​	分析双向链表的遍历，添加，修改和删除的操作思路 ==》代码实现

​	1）**遍历**和单链表一样，只是可以向前，也可以向后查找

​	2）**添加**（默认添加到双向链表的最后）

​	    （1）先找到双向链表的最后这个节点

​		（2）temp.next = newHeroNode

​		（3）newHeroNode.pre = temp

​	3）**修改**思路和原来的单向链表一样

​	4）**删除**

​		（1）因为是双向链表，因此，我们可以实现自我删除某个节点

​		（2）直接找到要删除的这个节点，比如temp

​		（3）temp.pre.next = temp.next

​		（4）temp.next.pre = temp.pre

- 双向链表的代码实现

  ```java
  package com.atguigu.linkedlist;
  
  public class DoubleLinkedListDemo {
      public static void main(String[] args) {
          // 测试
          System.out.println("双向链表的测试");
          // 先创建节点
          HeroNode2 hero1 = new HeroNode2(1, "宋江", "及时雨");
          HeroNode2 hero2 = new HeroNode2(2, "卢俊义", "玉麒麟");
          HeroNode2 hero3 = new HeroNode2(3, "吴用", "智多星");
          HeroNode2 hero4 = new HeroNode2(4, "林冲", "豹子头");
  
          // 创建一个双向链表
          DoubleLinkedList doubleLinkedList = new DoubleLinkedList();
          doubleLinkedList.add(hero1);
          doubleLinkedList.add(hero2);
          doubleLinkedList.add(hero3);
          doubleLinkedList.add(hero4);
  
          doubleLinkedList.list();
  
          // 修改
          HeroNode2 newHeroNode = new HeroNode2(4, "公孙胜", "入云龙");
          doubleLinkedList.update(newHeroNode);
          System.out.println("修改后的链表情况");
          doubleLinkedList.list();
  
          // 删除
          doubleLinkedList.del(3);
          System.out.println("删除后的链表情况");
          doubleLinkedList.list();
      }
  }
  
  class DoubleLinkedList {
      // 先初始化一个头结点，头结点不要动，不存放具体的数据
      private HeroNode2 head = new HeroNode2(0, "", "");
  
      // 返回头结点
      public HeroNode2 getHead() {
          return head;
      }
  
      // 遍历双向链表的方法
      // 显示链表[遍历]
      public void list() {
          // 判断链表是否为空
          if (head.next == null) {
              System.out.println("链表为空");
              return;
          }
  
          // 因为头节点，不能动，因此我们需要一个辅助变量来遍历
          HeroNode2 temp = head.next;
          while (true) {
              // 判断是否到链表最后
              if (temp == null) {
                  break;
              }
              // 输出节点信息
              System.out.println(temp);
              // 将temp后移，一定小心
              temp = temp.next;
          }
      }
  
      // 添加一个节点到双向链表的最后
      public void add(HeroNode2 heroNode) {
          // 因为head节点不能动，因此我们需要一个辅助遍历temp
          HeroNode2 temp = head;
          // 遍历链表，找到最后
          while (true) {
              // 找到链表的最后
              if (temp.next == null) {
                  break;
              }
              // 如果没有找到最后，将temp后移
              temp = temp.next;
          }
          // 当退出while循环时，temp就指向了链表的最后
          // 形成一个双向链表
          temp.next = heroNode;
          heroNode.pre = temp;
      }
  
      // 修改一个节点的内容，可以看到双向链表的节点内容修改和单向链表一样
      // 只是节点类型改成HeroNode2
      public void update(HeroNode2 newHeroNode) {
          // 判断是否空
          if (head.next == null) {
              System.out.println("链表为空~");
              return;
          }
          // 找到需要修改的节点，根据no编号
          // 定义一个辅助变量
          HeroNode2 temp = head.next;
          boolean flag = false; // 表示是否找到该节点
          while (true) {
              if (temp == null) {
                  break; // 已经遍历完链表
              }
              if (temp.no == newHeroNode.no) {
                  // 找到
                  flag = true;
                  break;
              }
              temp = temp.next;
          }
          // 根据flag判断是否找到要修改的节点
          if (flag) {
              temp.name = newHeroNode.name;
              temp.nickname = newHeroNode.nickname;
          } else { // 没有找到
              System.out.printf("没有找到编号%d的节点，不能修改\n", newHeroNode.no);
          }
      }
  
      // 从双向链表中删除一个节点
      // 说明
      // 1. 对于双向链表，我们可以直接找到要删除的这个节点
      // 2. 找到后，自我删除即可
      public void del(int no) {
          // 判断当前链表是否空
          if (head.next == null) { // 空链表
              System.out.println("链表为空，无法删除");
              return;
          }
  
          HeroNode2 temp = head.next; // 辅助变量（指针）
          boolean flag = false; // 标志是否找到待删除节点的
          while (true) {
              if (temp == null) { // 已经到链表的最后
                  break;
              }
              if (temp.no == no) {
                  // 找到的待删除节点的前一个节点temp
                  flag = true;
                  break;
              }
              temp = temp.next; // temp后移，遍历
          }
          // 判断flag
          if (flag) { // 找到
              // 可以删除
              // temp.next = temp.next.next;【单向链表】
              temp.pre.next = temp.next;
              // 这里我们的代码有问题？
              // 如果是最后一个节点，就不需要执行下面这条语句，否则出现空指针
              if (temp.next != null) {
                  temp.next.pre = temp.pre;
              }
          } else {
              System.out.printf("要删除的%d节点不存在\n", no);
          }
      }
  }
  
  // 定义HeroNode2，每个HeroNode2对象就是一个节点
  class HeroNode2 {
      public int no;
      public String name;
      public String nickname;
      public HeroNode2 next; // 指向下一个节点，默认为null
      public HeroNode2 pre; // 指向前一个节点，默认为null
  
      // 构造器
      public HeroNode2(int no, String name, String nickname) {
          this.no = no;
          this.name = name;
          this.nickname = nickname;
      }
  
      // 为了显示方法，我们重写toString
      @Override
      public String toString() {
          return "HeroNode{" +
                  "no=" + no +
                  ", name='" + name + '\'' +
                  ", nickname='" + nickname + '\'' +
                  '}';
      }
  }
  ```

#### 课堂作业和思路提示

双向链表的第二种添加方式，按照编号顺序[示意图]，按照**单链表的顺序添加**，稍作修改即可





## 马踏棋盘算法介绍和游戏演示

1）马踏棋盘算法也被称为骑士周游问题

2）将马随机放在国际象棋的8✖8棋盘Board\[0~7][0~7]的某个方格中，马按走棋规则（马走日字）进行移动。要求每个方格只进入一次，走遍棋盘上全部64个方格

3）游戏演示：http://brainmetrix.com/chess-knight/

4）会使用到图的深度优先遍历算法（DFS）+ 贪心算法优化

### 马踏棋盘算法

![](https://i.postimg.cc/5tYnbBrC/th-id-OIP.jpg)

马踏棋盘游戏代码实现

1）马踏棋盘问题（骑士周游问题）实际上是图的深度优先搜索（DFS）的应用。

2）如果是用回溯（就是深度优先搜索）来解决，加入马儿塔了53个点，如图：走到了第53个，坐标（1,0），发现已经走到尽头，没办法，那就只能回退了，查看其它的路径，就在棋盘上不停的回溯...，效率很低

3）因此需要使用贪心算法（greedy algorithm）进行优化，我们直接使用贪心算法优化思路来解决马踏棋盘问题。

4）马踏棋盘问题思路分析+代码实现

5）使用前面游戏来验证算法是否正确

![](https://cn.bing.com/th?id=OIP.kG_x7QDsXXr0DW5C6mK3_gAAAA&pid=Api&rs=1)

