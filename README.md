
# <!-- 注释 -->标题1
<div style='display: none'> 注释 </div>

[comment]: <> (注释)
[//]: # (注释)
[^_^]: <> (注释)

&lt;http://example.com/ &gt; &emsp;&emsp;
&lt;http://example.com/ &gt;  
[link](https://note.youdao.com/)

### <span id="title">title</span>

- 任务清单
- [ ] 表示该项目未完成
- [x] 表示该项目已完成

文本内容行末两个空格换行  
下一行

- 空格大小  
  【1】 &emsp;或&#8195; //全角  
  【2】 &ensp;或&#8194; //半角  
  【3】 &nbsp;或&#160;  //半角之半角

<center>行中心对齐</center>
<p Align="left">行左对齐</p>
<p Align="right">行右对齐</p>

*斜体*或_斜体_  
**粗体**  
***加粗斜体***  
~~删除线~~  
<span style="border-bottom:2px dashed yellow;">下划线</span>

- [锚点](#title)

[Google][1]、[Leanote][2]。(结尾空行)

[1]:http://www.google.com
[2]:http://www.leanote.com

[^index.js]  
[^2]  
[^T]

[^index.js]:index.js
[^2]:package-lock.json
[^T]:package.json

1. 有序列表项 一
2. 有序列表项 二
3. 有序列表项 三

* 无序列表项 一
+ 无序列表项 二
- 无序列表项 三

<center>  <!--开始居中对齐-->

![GitHub set up](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa0.att.hudong.com%2F30%2F29%2F01300000201438121627296084016.jpg&refer=http%3A%2F%2Fa0.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1617109249&t=3b5e8d17f6b7ee0aa4db9c151181dbd3 "图片Title")
![图片Alt](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa0.att.hudong.com%2F30%2F29%2F01300000201438121627296084016.jpg&refer=http%3A%2F%2Fa0.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1617109249&t=3b5e8d17f6b7ee0aa4db9c151181dbd3 "图片Title")
</center> <!--结束居中对齐-->

>>> 请问 Markdwon 怎么用？ - 小白  
>> x
>
>> sb
>>> ???
>
>> 自己看教程！ - 愤青
>
> 教程在哪？ - 小白

<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=#0099ff size=12 face="黑体">黑体</font>
<font color=gray size=5>gray</font>
<font color=#00ffff size=3>null</font>

C语言里的函数 `scanf()` 怎么使用？  
四个空格 或 tab 插入代码

    #include &lt;stdio.h&gt;
    int main(void)
    {
        printf(&#34;Hello world\n&#34;);
    }

```js
console.log('hello world');
```

| 左对齐格式 | 右对齐格式 | 居中对齐格式 |
| :-----| ----: | :----: |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |

```mermaid
graph RL
A[流程图-1]-->B{流程图-2}
B-->|推导出|C(流程图-结果1)
B-->|推导出|D(流程图-结果2)
```

```mermaid
graph TB
A(流程图-1)-->B[流程图-2]
A(流程图-1)---E
A(流程图-1)-.->C
B==>|推导出|D(流程图-结果2)
B-->|猜出|E>流程图-3]
B-- 筛子 ---E
E-->|蒙|F((流程图-结果3))
    subgraph one
    A
    F
    end
    subgraph two
    B-.推导出.->C{流程图-结果1}
    end
```

```mermaid
%% 注释: 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant 张三 
    participant 李四
    张三->王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 合理 食物 <br/>看医生...
    李四-->>张三: 很好!
    王五->李四: 你怎么样?
    李四->>王五: 很好!
```

```mermaid
%% 注释: 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant C
    participant ItemService
    participant TaskService
    TaskService->>C: 任务开始 0/10
    loop 任务进度更新
        C->>ItemService: 扣除物品
        ItemService->>TaskService: 物品变化通知
        TaskService->>C: 任务进度更新通知 i++/10
    end
    TaskService->>C: 任务进度更新通知 10/10
    C->>TaskService: 提交任务
    TaskService->>C: 任务完成
```

```mermaid
%% 注释: 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant C
    participant ItemService
    participant TaskService
    TaskService->>C: 任务开始 0/10
    loop 任务进度更新
        ItemService->>TaskService: 物品变化通知
        TaskService->>C: 任务进度更新通知 i++/10
    end
    TaskService->>C: 任务进度更新通知 10/10
    C->>TaskService: 提交任务
    TaskService->>C: 任务完成
    TaskService->>ItemService: 扣除任务物品
```

```mermaid
        gantt
        dateFormat  YYYY-MM-DD
        title 软件开发甘特图
        section 设计
        需求                      :done,    des1, 2014-01-06,2014-01-08
        原型                      :active,  des2, 2014-01-09, 3d
        UI设计                     :         des3, after des2, 5d
        未来任务                     :         des4, after des3, 5d
        section 开发
        学习准备理解需求                      :crit, done, 2014-01-06,24h
        设计框架                             :crit, done, after des2, 2d
        开发                                 :crit, active, 3d
        未来任务                              :crit, 5d
        耍                                   :2d
        section 测试
        功能测试                              :active, a1, after des3, 3d
        压力测试                               :after a1  , 20h
        测试报告                               : 48h
```

* * *
***
*****
- - -
---

