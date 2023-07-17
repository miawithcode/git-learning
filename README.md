# [Git Tutorial](https://www.youtube.com/watch?v=Q1kHG842HoI) Note

## Commits

- 查看历史的commits - `git log --all --graph`


## Branch

- 创建分支 - `git branch <branch-name>`
    - 创建一个分支会复制一份现有的所有代码。
    - Branch的命名一般是正在 working on 的featrue，如“social login”

- 切换分支（2种）
    - `git checkout <branch-name>`
    - `git swicth <branch-name>`

## Merge
Merge会把另一个分支合并到当前所在的分支，并把2个分支中所有修改的部分合并在一起

- 合并分支 - `git merge <branch-name> -m "some message"`
    - 通常来说不需要`-m "some message"`，不写的话会跳转到 vim 编辑器去编写 commit 信息

- 合并冲突（Merge Conflict）
    - 合并冲突指2个branch中在同一处分别有各自的修改，此时git不知道合并结果应该是什么，所以git会向我们询问应该合并哪一个分支的修改。
    - 在git展示的编辑框中，可以删除所有其他东西，填入选择的最终代码。
    - 上传并创建新的commit，commit信息可以是“commit conflict resolved”

## Feature Branch Workflow

1. 创建一个 feature branch
2. 上传这个 feature branch 到GitHub
    - 在 GitHub 上创建一个 repo ，并复制 repo 的链接
    - 在本地添加远端 repo 的链接 - `git remote add origin <link>`
    - 上传 main 分支到 GitHub - `git push origin main`
    - 切换到 feature branch ，上传到GitHub - `git push origin feature`
3. 创建一个“Pull Request” （do code reviews）
    - 在 GitHub 找到 Pull request，点击 "**New pull request**"
    - pull request
4. 合并 feature branch 到主分支（merging happens on GitHub）

## Update Local Repository After Merge

- 合并远端 repo 所有更改 - `git fetch`
- 切换到 main 主分支，进行远端和本地的合并 - `git pull origin main`
