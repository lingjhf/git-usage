---
layout: "../layouts/Layout.astro"
---

# 使用 pull requests

## fork 仓库

1. 打开公共仓库。
2. 点击 fork 到个人仓库。

## 创建本地开发分支

1. 下载远程个人仓库，下载远程仓库后 origin 默认是远程个人仓库的链接名称

```sh

    git clone https://github.com/username/xxx.git


```

2. 添加远程公共仓库链接

```sh

    git remote add upstream https://github.com/username/xxx.git


```

3. fetch 远程公共仓库代码

```sh

    git fetch upstream


```

4. 创建开发分支

```sh

    #选择公共仓库其中一个分支作为本地的开发分支
    git checkout -b feat upstream/master


```

## 提交代码发起 pull request

1. 在 feat 分支编写代码后提交

```sh

    git commit -m 'mssage'


```

2. feat 分支上传到远程个人仓库

```sh

    git push origin feat


```

3. 发起 pull requests

   1. 进入 github 的 Pull requests。
   2. 点击 New pull request。
   3. 选择公共仓库 master 分支，选择个人仓库 feat 分支。
   4. 点击确定提交 pull request。

## 后续开发

1. 如果 pr 审核通过后，可以把本地 feat 分支和远程个人仓库的 feat 分支删除。
2. 需要给远程公共编写新功能，执行 fetch 获取最新代码。

```sh

    git fetch upstream


```

3. 新建开发分支

```sh

    git checkout -b feat upstream/master


```

4. 最后根据上面提交代码发起 pull request 步骤完成代码提交。
