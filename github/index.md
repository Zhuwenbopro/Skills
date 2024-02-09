# Github

# 一、 安装 git（Windows）

- 在 [`https://gitforwindows.org/`](https://gitforwindows.org/) 直接下载 .exe 一顿下一步 ，最后安装成功。
- 设置名字和邮箱（姓名和邮箱会随着提交日志一起被公开）

```bash
git config --global user.name "Zeke Pro"
git config --global user.email "zekepro122@gmail.com"
```

- 设置 color.ui 让命令输出有更好的可读性：

```bash
git config --global color.ui auto
```

# 二、使用Github

1. 创建github账号
2. `ssh-keygen -t rsa -C "zekepro122@gmail.com"` 创建本地的rsa，在 `C:/user/11381/.ssh/rsa.pub`  里复制到下图的位置。

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4c7c261-df66-4bc5-8f47-fb5f0c299055/674dbf92-2d95-400b-bb77-3606971f7693/Untitled.png)

1. 输入 `ssh -T git@github.c` 验证是否设置成功：

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4c7c261-df66-4bc5-8f47-fb5f0c299055/40bc7f13-990e-4f8f-9578-e30594200e1c/Untitled.png)

1. 在 github 上创建自己的仓库 skills

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4c7c261-df66-4bc5-8f47-fb5f0c299055/e5c470af-a9c1-418a-a2bf-22f9e36ba0a5/Untitled.png)

1. 在本地使用 `git clone [git@github.com](mailto:git@github.com):Zhuwenbopro/Skills.git` 将仓库下载到本地：

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4c7c261-df66-4bc5-8f47-fb5f0c299055/493b933f-237a-4cff-b7d7-444af9bd9b10/Untitled.png)

1. 第一次进行 git 操作
    - `git add .` 将所有文件提交到暂存区
    - `git commit -m "commit message"` 提交给git
    - `git push` 更新 Github 上的代码

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4c7c261-df66-4bc5-8f47-fb5f0c299055/28f645cb-a2a4-4c6c-8065-82051a9bed1f/Untitled.png)

# 三、使用 Git

- 使用 `git init` 初始化仓库，此时会生成 .git 目录，里面存着管理当前目录所需的仓库数据。
- 使用 `git status` 查看仓库的状态，这个命令经常使用。
- 使用 `git add filename` 向暂存区添加文件，如果想要添加全部文件可以使用 `git add .` 。
- 使用 `git diff`  查看工作树和暂存区状态的差别。
- 使用 `git commit -m "commit message"` 保存仓库的历史纪录，将暂存区中的文件实际保存到仓库的历史纪录中。通过这些记录我们可以在工作树复原文件。如果想记述得更加详细，可以使用 `git commit` 后在编辑器详细原因，保存并关闭编辑器。将提交信息留空并直接关闭编辑器，提交就会被终止。
- 使用 `git log` 查看提交日志。

**分支命令**

- 使用 `git branch` 查看当前现有分支。
- 使用 `git checkout -b branchname` 创建、切换分支。