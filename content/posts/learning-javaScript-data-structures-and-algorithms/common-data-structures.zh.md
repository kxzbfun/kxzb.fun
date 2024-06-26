---
title: "常用的数据结构和技巧"
date: 2024-05-21T20:22:41+08:00
draft: false
showSummary: false
description: "本文介绍常用的数据结构和对应的算法技巧方案，关联Leetcode算法题目"
tags: ["技术", "数据结构和算法", "Leetcode"]
categories: ["Study"]
keywords:
  - "数据结构和算法"
  - "Leetcode"
---

本文介绍常用的数据结构和对应的算法技巧方案，关联Leetcode算法题目

TODO

- 添加图片
- [x] 添加 Leetcode URL
- 添加讲解

## 常用数据结构和技巧/Common Data Structure

- 数组、字符串/Array & String
- 链表/Linked-list
- 栈/Stack
- 队列/Queue
- 双端队列/Deque
- 树/Tree

## 数组、字符串/Array & String

### 优点

构建一个数组非常简单
能让我们在 O（1）的时间里根据数组的下标（index）查询读取某个元素

### 缺点

- 构建时必须分配一段连续的空间
- 查询某个元素是否存在时需要遍历整个数组，耗费 O（n）的时间（其中，n是元素的个数）
- 删除和添加某个元素时，同样需要耗费 O（n）的时间

### 关联题目

[题目242. 有效的字母异位词](https://leetcode.cn/problems/valid-anagram/description/)

解题思路：

  1. 如果s和t的长度不同，直接返回false。
  2. 哈希表，英文字母一共26个，s 中字母 在26个英文字母中出现一次，则加一。
  3. t 中字母在26个英文字母中出现一次，  则减一。
  4. 若26个字母每个都为0则互为异位词返回true，若不为0否则返回false

## 链表 /Linked List

单链表：链表中的每个元素实际上是一个单独的对象，而所有对象都通过每个元素中的引用字段链
接在一起。

双链表：与单链表不同的是，双链表的每个结点中都含有 `两个引用字段`。

### 链表优点

灵活地分配内存空间

能在 O（1）时间内删除或者添加元素

### 链表缺点

查询元素需要 O（n）时间 （只能根据list.next.next一个一个的顺序查找）

### 解题技巧

- 利用快慢指针（有时候需要用到三个指针）
  1. 链表的翻转
  2. 寻找倒数第K个元素
  3. 寻找链表中间链表的元素
  4. 判断链表是否有环

- 构建一个虛假的链表头
  - 两个排序链表，进行整合排序
  - 将链表的奇偶数按原定顺序分离，生成前半部分为奇数，后半部分为偶数的链表

[题目25.K个一组翻转链表](https://leetcode.cn/problems/reverse-nodes-in-k-group/description/)

考察的点

- 对翻转链表的熟悉程度
- 递归算法的理解程度

### 如何训练该技巧

- 在纸上或者白板上画出节点之间的相互关系
- 画出修改的方法

## 栈/Stack

### 特点

- 后进先出 LIFO

### 算法基本思想

- 可以用一个单链表来实现
- 只关心上一次的操作 (要对这些特点敏感，熟能生巧)
- 处理完上一次的操作后，能在O（1）时间内查找到更前一次的操作

### 栈相关题目

[题目20.有效的括号](https://leetcode.cn/problems/valid-parentheses/description/)

[题目739.每日温度](https://leetcode.cn/problems/daily-temperatures/description/)

## 队列/Queue

### 队列特点

- 先进先出（FIFO）

### 常用的场景

- 广度优先搜索

## 双端队列/Deque

### 基本实现

- 可以利用一个双链表
- 队列的头尾两端能在 O（1）的时间内进行数据的查看、添加和删除

### 双端队列常用的场景

- 实现一个长度动态变化的窗口或者连续区间

### 队列相关题目

[题目239. 滑动窗口最大值](https://leetcode.cn/problems/sliding-window-maximum/description/)

## 树/Tree

### 树的共性

- 结构直观
- 通过树问题来考察 `递归算法` 掌握的熟练程度

### 面试中常考的树的形状有普通二叉树

- 平衡二叉树
- 完全二叉树
- 二叉搜索树
- 四叉树
- 多叉树
- 特殊的树：红黑树、自平衡二叉搜索树

### 遍历

- 前序遍历（Preorder Traversal）
- 中序遍历 （Inorder Traversal）
- 后序遍历 （Postorder Traversal）

### 树相关题目

[题目230.二又捜索中第K小的元素](https://leetcode.cn/problems/kth-smallest-element-in-a-bst/description/)
