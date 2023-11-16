# 系统圣经
- caching：专攻最重要的部分以降低整体开销
	- 加速所有数据访问太贵，则仅加速重要信息的访问(CPU cache, database buffer)
	- 比较数据太贵，则仅比较描述数据本身的关键信息(MD5, fingerprint)
	- 搜索所有的数据太贵，则仅搜索描述数据组织的关键信息(index structure, bloom filter)
	- 某一个功能在很多应用里都需要而每次都单独实现太麻烦，则仅抽象成基础功能由底层架构实现（kernel feature，middleware，base class）
- batching：一次性做更多事以平摊每件事情的开销
	- 仅访问一个任务太贵，则聚集更多相同的任务一起执行(network/SSD queue，write buffer)
	- 系统中仅一个资源忙碌工作成为瓶颈而其他资源空闲，则聚集不同的任务一起执行(DMA，pipeline，async，any form of trade-off)

欢迎各种讨论和补充(≧∇≦)ﾉ
