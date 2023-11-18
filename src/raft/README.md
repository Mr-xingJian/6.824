# Raft实现总结

## Background

在去年其实已经实现过一次Raft基本流程了，完成了2A、2B、2C三个Lab，整个实现的过程还是十分挣扎的，记得应该熬了好多夜才最终实现出来，实现的Code没有做到简洁优雅。

这次原本的构想是对去年的实现做一次重构，梳理一下流程，也能让自己对Raft的认知更加深刻。重构之前又去YouTube上把Raft作者讲解Raft实现的视频看了一遍，时间确实是非常奇妙的东西，去年没法做到理解视频中的每一张图、每一句话，今年再看好多地方一下子就能串起来了，然而这一年中我也并没有去继续学习Raft。

与上次直接开始写代码不同，这次我去看了课程的一些Guide文章，特别是如何在流程中加日志来帮助我们高效分析问题，磨刀不误砍柴工。从结果上看，这一次的重构还是比较有效的，实现代码简洁了不少，整个测试结果也更加稳定，每一个Lab都是连续测试100次，均没有出错，也让我更加有信心去完成后面的Lab。

去年实现Raft花了好久，这次只花了不到一周的时间，仍然是抽出下班后的一点时间来完成，所以理解分布式算法比实现更重要，只有全面且完备的理解了工作原理，才能轻松地实现Code。