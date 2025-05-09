# proj82-container-os
### 项目名称
容器化Linux操作系统

### 项目描述

容器化Linux操作系统（简称容器化OS）是指用户态的所有进程都是以容器的方式运行，包括1号进程initd。
容器化OS的好处是，用户态的程序不会对OS造成任何修改，即容器化OS本身是不可变的（immutable）。
因为容器对外部的依赖只有内核，所以容器化OS的组件非常少，只需要内核、initd以及rootfs，其主要的工作是：
* 重构initd，以支持调度用户态容器程序，可以参考containd对容器的调度；
* initd要支持为容器程序挂载外部目录、卷等保存容器应用数据的外部存储，可以按照Container Storage Interface的要求来实现。


### 所属赛道

2025全国大学生操作系统比赛的“OS功能设计”赛道



### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求



### 项目导师

王璞

* github https://github.com/datenlord

* email pwang700@qq.com



### 难度

中高级



### 特征

要求用Rust语言来实现



### 文档

* [containerd](https://containerd.io/docs/)
* [Container Storage Interface](https://kubernetes-csi.github.io/docs/)

### License

[MIT license](http://opensource.org/licenses/MIT)



## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

以下项目要求，最基本要求是实现前三条，其他可选：
* 用Rust实现initd，支持调度运行Docker容器程序，并兼容containerd的API；
* 用Rust实现的initd支持为Docker容器程序挂载外部目录或卷；
* 基于QEMU实现容器化OS的测试与验证；
* 支持X86_64，ARM和AARCH64多种架构；
* 支持调度运行Kata容器程序，Kata是基于KVM实现的容器，其对容器的隔离比Docker更加彻底；
* 用Rust实现容器化OS的安装程序；
* 支持容器应用的安全验证，即只允许验证通过的容器应用调度运行。
