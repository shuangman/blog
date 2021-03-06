如何精简一本书
===========================

`《Redis使用教程》 <http://redisguide.com/>`_ 的写作工作已经接近尾声了，
除了继续撰写最后剩下的几章之外，
我也开始对全书已完成的章节实施修整，
而修整工作最重要的一步，
就是要去芜存菁、删繁就简，
从而达到减少书本篇幅的目的。

跟我之前已经出版的作品相比，
《Redis使用教程》（后简称《教程》）在篇幅方面有了显著的增加：

- 以《Redis设计与实现》（后简称《实现》）为例子，
  我在写《实现》的时候，
  Redis 才刚进入 3.0 版本，
  并且因为《实现》关注的是功能的内部实现，
  只要把内部实现特别是数据结构说清楚就行了，
  具体的功能并不需要一一介绍，
  所以整本书的篇幅限制在了 400 页之内。

- 另一方面，
  对于现在的《教程》来说，
  因为是面向新手和使用者写的一本入门书和参考书，
  所以每个功能都需要巨细无遗地覆盖到，
  而且 Redis 5.0 本身功能就比 3.0 要多得多，
  因此这次《教程》的篇幅应该会在 500 至 600 页左右。

因为《教程》本身篇幅已经不少了，
所以为了保证该书的可读性，
我必须保证书本内容足够紧凑，
没有多余的章节。

为了做到这一点，
我首先把目光聚焦到了书本的《编程练习》部分来。
具体来说，
书本开头的大部分大章都会在章末有名为《编程练习》的一节，
在这一节里面，
我会根据那一章的内容，
设计两三个需要进行编程的题目，
这些题目通常是正文内容的一个延伸，
又或者是正文介绍的程序的一个变种。
举个例子，
书本的《列表》一章在正文里介绍了如何使用列表命令去实现一个先进先出队列，
而该章的其中一个编程练习就是要读者去实现一个后进先出队列（又称栈）。

在刚开始写《教程》的时候，
《编程练习》本来是我觉得不错的构思的其中一个。
但是现在回过头重新审视这个部分，
我却有了相反的想法，
其中的原因大概可以归纳为以下几点：

1. **不是每个人都喜欢做练习。**
   必须承认，
   并不是每个人都喜欢做练习，
   据我所知，
   包括我在内的很多读者都不会真的认真去完成书本中列出的练习，
   最多就是看着题目思考一下，
   然后再去对答案，
   这样的话，
   编程练习中最为重要的“编程”部分就缺失了，
   整个题目在读者脑海中过一下就没了，
   效果不大，
   更别说有些读者还会直接跳过习题。

2. **书本的习题没有做到一视同仁。**
   因为内容的问题，
   书本有些大章是没有《编程练习》部分的，
   这样一来的话，
   读者在阅读的时候可能就会产生这样的疑问“为什么上一章有习题，而这章却没有呢？”。
   但我也不希望为了让每章都有练习而去给某些大章加上一些没有用的练习题，
   这跟我想要为书本“瘦身”的想法是完全相左的。

3. **书本的篇幅有限。**
   正如之前所说，
   介绍 Redis 本身的功能已经占用了相当大的篇幅，
   书本目前的编程练习起码要占用二三十页，
   这并不是一个小数字。

综合来说，
编程练习并不属于书本的核心内容，
这个部分从某种程度上来说对于书本是可有可无的。
因此为了保证书本的简洁性，
我决定从书本中移除各章的《编程练习》部分。

.. figure:: image/remove-exercises.png

   移除各章的《编程练习》部分

当然，
对《编程练习》部分的移除工作并不是简单粗暴地完成的：
我重新审视了每一个练习，
只移除了其中不太重要、没有太多新内容的练习，
至于那些引入了重要知识或者非常有趣的练习，
我接下来会将它们转移到各章的正文里面，
让它们直接以正文的形式出现在书本里面，
这样读者就不会错过任何有趣的内容了。

另一方面，
虽然编程练习没有在这次的《Redis使用教程》里面出现，
但这次构思编程练习题目对于我来说也是一次非常宝贵的经验，
并且计算机知识方面的习题在诸如培训和课堂教学这样的场景里也是不可或缺的。
考虑到这一点，
未来如果有机会的话，
我也许会通过某种方式来给大家出一些 Redis 方面的书面习题和编程题目，
希望大家到时候会感兴趣。

精简一本书并不是一件容易的事情，
但为了提高书本的可读性，
有时候作者必须要有壮士断腕的勇气和决心才行。
当初我在撰写《Redis设计与实现》的时候，
曾经也在书本里面花费了不少篇幅去罗列和介绍 Redis 每种数据结构的底层实现 API ，
但是当我完成书本初稿回头去审视这些内容的时候，
却发现它们不仅作用不大，
而且还很容易引起读者的厌倦，
所以虽然当时花了不少时间去写这个部分，
但是最后却把它们全删了，
被删掉的部分至少有 30 页以上。
虽然这种大刀阔斧的删减还是挺让自己心疼的，
但书本最终出来的效果很好，
大家都很喜欢和欣赏《Redis实现与设计》的简洁精炼，
我很庆幸当初自己做了正确的事情。

好的，
关于书本精简方面的话题就介绍到这里了，
接下来如果有其他这方面的想法或者有其他关于《Redis使用教程》的想法想要跟大家分享的话，
我会再写文章的，
希望大家到时会感兴趣。

最后祝大家国庆节快乐！

| 黄健宏
| 2018.10.1
