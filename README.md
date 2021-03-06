# b-end
业务端逻辑,让用户更专注于业务逻辑,而不是莫名其妙的CURD

# 前言
实际上我们绝大多数的代码都是在处理数据, 用户创建了一个订单,我们需要创建对应的数据, 用户修改了订单,我们还是在对这个数据进行对应的修改, 那么怎么将每天繁杂且重复的工作节省下来呢? 

# 简介
`b-end`可以理解成 `back-end`或者`business-end`,  顾名思义,就是以业务为核心的后端. 让你更注重对业务逻辑的调整, 而不是对sql的编写以及框架参数的无穷无尽的调试.

## 目标
`b-end`的初衷是要让人们从一个`流程图`开始,将`数据(表)`的来龙去脉很直观的表现出来. 这个流程就是你的业务逻辑, 在创建好这个流程之后,你可以基于这个流程创建接口也好,创建定时任务也好,或者是其他的任务. 

## 为什么会想写这样一个框架呢?
1. 正如前面所述,目前研发人员大多数的时间其实都是在调试,以及一些无关紧要的事情上,为什么不能解放这部分的人力呢? 然后去做一些更有难度事情.
2. 有时候总是会吐槽以前的人写的代码难以维护,`屎山`之类的词就是用来吐槽这些的. 除了代码之外,其实很多人会忽略文档的问题,实际上文档也是很大的通点.
3. 技术的更新迭代,如果想要去维护它,总是会遇到各种各样的版本兼容之类的问题。
4. 代码更新时，大多数都不会去维护注释以及测试用例，就会导致注释以及测试用例比较落后。

# 涉及概念
- 工程组 
    >  一系列工程的集合,暂时不会考虑
- 工程 
    >  项目,包含了接口,定时任务等等.
- 流程 
    >  流程和节点的合集,可大可小.
- 节点
    >  流程中的最小的一个点，可以由个块组成
- 块
    >  块，可以认为是一行代码，或者一个函数，通常是用来操作元素
- 元素
    >  数据实体，通常情况下是一个数据表，
