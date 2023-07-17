---
title: 文件系统
---

文件系统是操作系统的核心功能之一，上层应用程序与文件系统打交道，而不是直接与底层存储打交道，可以做到通用(无需对各种不同的存储特别编写不同的程序)、方便、可移植。

文件系统大致可以分为如下几类：

1. 本地文件系统：例如windows用的NTFS、Linux常用的ext、macOS的APFS、通用的vFAT等等
1. 只读文件系统：如光盘用的ISO9660、系统引导用的SquashFS等
1. 加密文件系统：gocryptfs等
1. 网络文件系统：smb、NFS

上述文件系统在Linux和基于FreeBSD的macOS中都可以mount到一棵目录树上，然后象本地文件系统一样去操作。

HDFS是Hadoop Filesystem的缩写，也是文件系统，但与上述文件系统不同，HDFS是Hadoop架构的分布式文件系统，一般不会象上面的文件系统那样mount到本地目录数中，因为HDFS的优势在于分布式、海量数据的存取，而不是小量数据的随机存取。HDFS由其上层程序如Map-Reduce、Spark等存取，这样才能发挥出HDFS的优势。

