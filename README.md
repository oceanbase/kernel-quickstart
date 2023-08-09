# OceanBase 数据库开发者入门教程

欢迎访问 OceanBase 数据库开发者入门教程，您可以在本仓库中查看开发者入门教程的文档。本文简单为您介绍开发者入门教程各章节包含的内容以及如何贡献文档。

* 文档介绍

* 贡献文档

## 文档介绍

开发者入门教程共分为五个章节，从 MiniOB 概述、环境搭建、存储、索引、SQL 引擎、事务几个方面介绍数据库和 MiniOB，各章节内容如下。

### 第 1 章：数据库系统概述

本章介绍数据库系统概述、MiniOB 概述及 MiniOB 研发环境搭建，主要包含如下内容。

* [1.1 数据库系统的发展历史](zh-CN/1.database-system-overview/2.development-of-database-system.md)：介绍数据库的发展背景，数据库模型以及数据库的发展历史。

* [1.2 数据库系统架构](zh-CN/1.database-system-overview/3.database-system-architecture.md)：从存储、事务和 SQL 三个方面介绍数据库系统架构。

* [1.3 MiniOB 概述](zh-CN/1.database-system-overview/4.miniob-overview.md)：介绍 MiniOB 的背景和框架，并简单介绍如何使用 MiniOB 系统学习 OceanBase 数据库。

* [1.4 MiniOB Gitee 使用说明](zh-CN/1.database-system-overview/5.miniob-github-gitee-instructions.md)：以 Gitee 为例介绍如何在训练营中进行提测以及常用的 Git 操作命令。

* [1.5 MiniOB 开发调试环境搭建](zh-CN/1.database-system-overview/6.miniob-debug-environment-setup.md)：介绍如何通过手动构建或直接使用 Dockerfile 构建两种方法搭建 MiniOB 开发调试环境。

* [1.6 MiniOB 线程模型](zh-CN/1.database-system-overview/7.miniob-thread-model.md)：介绍 MiniOB 的底层数据结构线程池。

* [1.7 课后实践](zh-CN/1.database-system-overview/8.practical-exercises-of-01.md)：根据本章内容给出一个 MiniOB 相关题目供大家练习。

### 第 2 章：数据库的存储结构

本章介绍数据库存储结构基础及 MiniOB 存储实现原理。主要包含如下内容。

* [2.1 存储器的层次结构](zh-CN/2.database-storage-structure/2.memory-hierarchy.md)：介绍存储器的层次和特点，并介绍虚拟存储器。

* [2.2 磁盘存储器](zh-CN/2.database-storage-structure/3.disk-storage.md)：介绍存储器的基础概念，空间计算和存取性能，以及如何优化性能，并介绍磁盘的故障以及如何检测。

* [2.3 块与记录组织](zh-CN/2.database-storage-structure/4.block-record-organization.md)：从概念、记录的类型、记录的存储结构、块的存储结构四个方面介绍块与记录组织。

* [2.4 变长数据和记录](zh-CN/2.database-storage-structure/5.variable-length-data-records.md)：介绍变长数据的定义和类型、具有变长字段/重复字段/可变格式/大值类型的记录，并简单介绍 blob 二进制大对象和列存储。

* [2.5 记录的修改](zh-CN/2.database-storage-structure/6.modification-records.md)：根据插入、更新和删除三种场景介绍如何修改记录。

* [2.6 MiniOB 存储实现原理](zh-CN/2.database-storage-structure/7.miniob-storage-implementation.md)：从存储层面介绍 MiniOB 的实现。

* [2.7 课后实践](zh-CN/2.database-storage-structure/8.practical-exercises-of-02.md)：根据本章内容给出一个 MiniOB 相关题目供大家练习。

### 第 3 章：索引结构

本章主要介绍数据库索引结构基础，以及 MiniOB 中 B+ 树的实现，主要包含如下内容。

* [3.1 B+ 树介绍](zh-CN/3.index-structure/2.btree-introduction.md)：介绍 B+ 树的概念，以及在 B+ 树中如何查找结点、插入结点和删除结点。

* [3.2 散列表](zh-CN/3.index-structure/3.hash-table.md)：简单介绍静态散列表和动态散列表，并介绍散列表的插入和删除。

* [3.3 LSM 介绍](zh-CN/3.index-structure/4.lsm-introduction.md)：介绍 LSM-Tree 的基本概念，并以 LevelDB 的 LSM-Tree 为例进行详细介绍。

* [3.4 MiniOB B+Tree 实现](zh-CN/3.index-structure/5.miniob-btree-introduction.md)：介绍 MiniOB 的 B+ 树如何实现，以及如何对 B+ 树进行插入和删除操作。

* [3.5 课后实践](zh-CN/3.index-structure/6.practical-exercises-of-03.md)：根据本章内容给出一个 MiniOB 相关题目供大家练习。

## 第 4 章：SQL 引擎

本章主要介绍数据库 SQL 引擎基础，并对 SQL 的优化和执行进一步拓展，主要包含如下内容。

* [4.1 SQL 层架构](zh-CN/4.sql-engine/2.sql-layer-architecture.md)：介绍 OceanBase 和 MySQL 的 SQL 层架构区别，并简单介绍 SQL 语句结构。

* [4.2 Parser 和 Resolver 模块](zh-CN/4.sql-engine/3.parser-resolver.md)：介绍 SQL 层架构中的 Parser 模块和 Resolver 模块

* [4.3 Transformer 和 optimizer 模块](zh-CN/4.sql-engine/4.transformer-optimizer.md)：简单介绍火山模型，并举例介绍如何从一个火山模型的层次调用结构去看是否有更多的优化空间。

* [4.4 Executor 模块](zh-CN/4.sql-engine/5.executor.md)：结合示例详细介绍 Executor 模块中的火山模型。

* [4.5 Fast-parser 和 Plan cache 模块](zh-CN/4.sql-engine/6.fast-parser-plan-cache.md)：介绍 Fast-parser 和 Plan cache 模块。

* [4.6 基础代数符号与操作介绍](zh-CN/4.sql-engine/7.algebraic-symbols-operate.md)：介绍基础关系代数符号，包括传统的集合运算、专门的关系运算、外连接、聚集、物化计算等。

* [4.7 关系表达式的等价规则转换](zh-CN/4.sql-engine/8.equivalence-rule-conversion.md)：结合示例介绍关系表达式的等价规则转换，并简单说明经过规则改写之后，查询计划会发生什么样的变化。

* [4.8 执行计划的选择](zh-CN/4.sql-engine/9.choice-execution-plan.md)：结合示例帮助理解执行计划选择时的一些影响因素。

* [4.9 代价](zh-CN/4.sql-engine/10.cost.md)：结合示例帮助理解什么是代价，并介绍统计信息的概念，以及统计信息在代价估计中的意义。

* [4.10 课后实践](zh-CN/4.sql-engine/11.practical-exercises-of-04.md)：根据本章内容给出一个 MiniOB 相关题目供大家练习。

## 第 5 章：事务引擎

事务是数据库很重要的概念之一，通过事务保证了很多操作量大，数据量高的业务的稳定性。本章主要介绍事务相关的概念和操作，主要包含如下内容。

* [5.1 事务简介](zh-CN/5.transaction-engine/2.business-profile.md)：介绍事务的基本概念和 ACID 属性。

* [5.2 故障类型和事务模型](zh-CN/5.transaction-engine/3.transaction-model.md)：介绍数据库中故障的产生和处理方法、事务模型，并结合示例介绍事务原语。

* [5.3 undo 日志](zh-CN/5.transaction-engine/4.undo-log.md)：主要介绍回滚日志（undo log）规则、如何使用 undo 日志恢复数据，并结合示例介绍检查点机制和动态检查点。

* [5.4 redo 日志](zh-CN/5.transaction-engine/5.redo-log.md)：主要介绍 redo 日志规则、如何使用 redo 日志恢复数据，并结合示例介绍 redo 日志的检查点。

* [5.5 undo/redo 日志](zh-CN/5.transaction-engine/6.undo-redo-log.md)：主要介绍 undo/redo 日志规则、如何使用 undo/redo 日志恢复数据，并结合示例介绍 undo/redo 日志的检查点及 undo/redo 日志的应用。

* [5.6 隔离级别](zh-CN/5.transaction-engine/7.isolation-level.md)：介绍数据库的隔离级别，包括读未提交、读提交、可重复读、可有序化等。

* [5.7 锁](zh-CN/5.transaction-engine/8.lock.md)：通过示例介绍数据库中锁的概念，包括细粒度的锁和两阶段加锁。

* [5.8 时间戳](zh-CN/5.transaction-engine/9.timestamp.md)：介绍数据库中时间戳的概念。

* [5.9 多版本并发控制](zh-CN/5.transaction-engine/10.mvcc.md)：介绍版本控制协议和快照隔离的概念。

* [5.10 课后实践](zh-CN/5.transaction-engine/11.practical-exercises-of-05.md)：根据本章内容给出一个 MiniOB 相关题目供大家练习。

## 贡献文档

### 开始之前

感谢您对 OceanBase 数据库文档的贡献兴趣。为厘清就个人或实体贡献内容而授予的知识产权许可，我们必须对每位贡献者签署的贡献者许可协议（Contributor Licence Agreement，简称 CLA）（“CLA”）进行归档，以证明就 CLA 达成的一致。点击 [OceaBase CLA](https://cla-assistant.io/oceanbase/oceanbase?pullRequest=108)，点击 **Sign in with GitHub to agree** 按钮签署协议。

### 贡献指南

您可以按照以下步骤提交 Pull Request（简称 PR）：

#### 步骤 1：Fork 项目仓库

1. 访问 OceanBase 数据库开发者入门教程文档的 [GitHub 地址](https://github.com/oceanbase/kernel-quickstart)。

2. 点击 Fork 按钮创建远程分支。

#### 步骤 2：克隆分支到本地

1. 定义工作目录。

   ```shell
   # 定义工作目录
   working_dir=$HOME/Workspace
   ```

2. 配置 GitHub 用户名。

   ```shell
   user={GitHub账户名}
   ```

3. 克隆代码。

   ```shell
   # 克隆代码
   mkdir -p $working_dir
   cd $working_dir
   git clone git@github.com:$user/kernel-quickstart.git
   # 或: git clone https://github.com/$user/kernel-quickstart.git

   # 添加上游分支
   cd $working_dir/kernel-quickstart
   git remote add upstream git@github.com:oceanbase/kernel-quickstart.git
   # 或: git remote add upstream https://github.com/oceanbase/kernel-quickstart.git

   # 为上游分支设置 no_push
   git remote set-url --push upstream no_push

   # 确认远程分支有效
   git remote -v
   ```

#### 步骤 3：创建新分支

1. 更新本地分支。

   ```shell
   cd $working_dir/kernel-quickstart
   git fetch upstream
   git checkout $branch
   git rebase upstream/$branch
   ```

2. 基于本地 $branch 分支创建新分支。

   ```shell
   git checkout -b new-branch-name
   ```

#### 步骤 4：修改/添加/删除文档

在 `new-branch-name` 上修改文档并保存更改。

#### 步骤 5：提交更改

```shell
# 检查本地文件状态
git status

# 添加您希望提交的文件
# 如果您希望提交所有更改，直接使用 `git add .`
git add <file> ...
git commit -m "commit-message: update the xx"
```

#### 步骤 6：保持开发分支与上游分支同步

```shell
# 在开发分支执行以下操作
git fetch upstream
git rebase upstream/branch
```

#### 步骤 7：推送更改至远程分支

```shell
# 在开发分支执行以下操作
git push -u origin new-branch-name
```

#### 步骤 8：创建 PR

1. 访问您 Fork 的仓库。

2. 单击 `new-branch-name` 分支旁的 `Compare & pull request` 按钮。

以上就是参与 OceanBase 数据库文档共建的步骤，如果在此过程中遇到任何问题，可以加入我们唯一官网钉钉群：41203246，与社区热心的技术大神、热情的贡献者、经验丰富的技术专家一起交流、探讨问题。
