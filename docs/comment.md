>【强制】类、类属性、类方法的注释必须使用 Javadoc 规范，使用/\*\*内容\*/格式，不得使用 // xxx 方式。

?> 在 IDE 编辑窗口中，Javadoc 方式会 示相关注释，生成 Javadoc 可以正确输出相应注 释;在 IDE 中，工程调用方法时，不进入方法即可悬浮 示方法、参数、返回值的意义， 高 阅读效率。

>【强制】所有的抽象方法(包括接口中的方法)必须要用 Javadoc 注释、除了返回值、参数、 异常说明外，还必须指出该方法做什么事情，实现什么功能。

?> 对子类的实现要求，或者调用注意事项，请一并说明。

>【强制】所有的类都必须添加创建者和创建日期。

---
>【强制】方法内部单行注释，在被注释语句上方另起一行，使用//注释。方法内部多行注释使用/* */注释，注意与代码对齐。

---

>【强制】所有的枚举类型字段必须要有注释，说明每个数据项的用途。

---

>【推荐】与其“半吊子”英文来注释，不如用中文注释把问题说清楚。专有名词与关键字保持 英文原文即可。

反例:   

?> “TCP 连接超时”解释成“传输控制协议连接超时”，理解反而费脑筋。

>【推荐】代码修改的同时，注释也要进行相应的修改，尤其是参数、返回值、异常、核心逻辑 等的修改。

?> 代码与注释更新不同步，就像路网与导航软件更新不同步一样，如果导航软件严重滞后， 就失去了导航的意义。

>【参考】谨慎注释掉代码。在上方详细说明，而不是简单地注释掉。如果无用，则删除。 ?> 代码被注释掉有两种可能性:1)后续会恢复此段代码逻辑。2)永久不用。前者如果没 有备注信息，难以知晓注释动机。后者建议直接删掉(代码仓库保存了历史代码)。

---

>【参考】对于注释的要求:第一、能够准确反应设计思想和代码逻辑;第二、能够 述业务含 义，使别的程序员能够迅速了解到代码背后的信息。完全没有注释的大段代码对于阅读者形同 天书，注释是给自己看的，即使隔很长时间，也能清晰理解当时的思路;注释也是给继任者看 的，使其能够快速接替自己的工作。

---

>【参考】好的命名、代码结构是自解释的，注释力求精简准确、表达到位。避免出现注释的一个极端:过多过滥的注释，代码的逻辑一旦修改，修改注释是相当大的负担。

反例:
```
// put elephant into fridge
put(elephant, fridge);
//方法名 put，加上两个有意义的变量名 elephant 和 fridge，已经说明了这是在干什么，语义清晰的代码不需要额外的注释。
```

>【参考】特殊注释标记，请注明标记人与标记时间。注意及时处理这些标记，通过标记扫 ， 经常清理此类标记。线上故障有时候就是来源于这些标记处的代码。

- 待办事宜(TODO):( 标记人，标记时间，[预计处理时间])  
表示需要实现，但目前还未实现的功能。这实际上是一个 Javadoc 的标签，目前的 Javadoc还没有实现，但已经被广泛使用。只能应用于类，接口和方法(因为它是一个 Javadoc 标签)。
- 错误，不能工作(FIXME):(标记人，标记时间，[预计处理时间])  
在注释中用 FIXME 标记某代码是错误的，而且不能工作，需要及时纠正的情况。