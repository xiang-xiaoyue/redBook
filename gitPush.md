# 提交规范 commit convention

> 原文链接：[https://github.com/Tencent/cherry-markdown/wiki/%E6%8F%90%E4%BA%A4%E8%A7%84%E8%8C%83-commit-convention](https://github.com/Tencent/cherry-markdown/wiki/%E6%8F%90%E4%BA%A4%E8%A7%84%E8%8C%83-commit-convention)

---

## ⚠️ 注意

不要在 `main` 分支提交任何修改性质代码，`main` 分支只作为发版分支。

---

## 一、规范意义

作为开源项目，我们的提交规范也要和业界使用 Conventional Commits 的规范一致，因此要定制一套符合我们的提交规范。同时，我们还规范开发工作流，以便版本管理和多人协作。

---

## 二、提交公式

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

- **标题行**：必填，描述主要修改类型和内容，scope 增强描述提交作用范围，例如我们 cherry 的 core 层、Editor、Previewer 等。
- **主题内容**：描述为什么修改，做了什么样的修改，以及开发的思路；这里直接引用 tapd 源码关键字，若没有则不填。
- **页脚注释**：放 Breaking Changes 或 Closed Issues。

---

## 示例

```
fix: [空格] 别为代码块

其他补充信息，解释 fix 标题

Fixed #10 
Close #10
```

---

## type 类型如下

1. feat：新功能（feature）
2. fix：修补 bug
3. docs：文档（documentation）
4. style：格式（不影响代码运行的变动）
5. refactor：重构（即不是新增功能，也不是修改 bug 的代码变动）
6. test：增加测试
7. chore：构建过程或辅助工具的变动

---

## 提交

> 当前提交需要使用 `changeset-cli` 进行提交 release 信息。

执行 `yarn changeset`，如果当前有包含提交的依赖就使用空格选中。

然后点击回车，分别有 `major bump`、`minor bump`、`patch bump` 进行选择，这里会影响到后面依赖升级的版本。然后在 `Summary »` 后提交此次 commit 信息。

---
