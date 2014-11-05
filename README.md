Git_Guide
=========
git 常用命令

设置用户信息：git config --global user.name "John Doe"
git config --global user.email johndoe@example.com

批量删除使用：git add -A

查看改动使用：git status

批量添加文件：git add .

关联远程仓库：git remote add origin git@github.com:zhbbupt/learngit.git

建立本地分支：git branch

建立远程分支：gir branch origin

快速复制：按住左键选中内容，再单击右键完成复制

快速粘贴：单击右键完成粘贴

回退到上一版本：git reset --hard HEAD^

查看历史日志：git log

查看详细日志：git log -p

回退到某一版本：git reset --hard <版本号>

回退后查看以前更新的日志：git reflog

忽略某些文件：cat .gitignore

重命名某一文件：git mv

查看分支间的不同：git diff

当前的索引和上次提交间的差异：git diff --cached

显示工作目录与上次提交时之间的所有差别：git diff HEAD

当前目录下的某个文件和上次提交的差别：git diff HEAD -- ./

统计一下有哪些文件被改动，有多少行被改动:git diff --stat

合并分支：git merge

切换到某分支：git checkout

新建并切换到某一分支：git checkout -b

提交改动：git commit -m "******"

推送到某一远程分支：git push -u origin

查看远程分支:git branch -a

删除远程分支:git push origin --delete

删除tag:git push origin --delete tag

同步本地仓库：git pull origin

创建并更新所有远程分支的本地远程分支.：git fetch

重命名本地分支:git branch -m

把本地tag推送到远程：git push --tags

获取远程tag: git fetch origin tag

列显已有的标签:git tag

新建含附注的标签:git tag -a -m '********'

查看相应标签:git show

签署标签:git tag -s -m '********'

轻量级标签:git tag -a 对象校验号（9fceb02）

git bash 操作流程

上传： cd 路径 git add . git commit -m "这次操作的备注(最好用英文)" git push origin <分支名>

同步： cd 路径 git pull origin <远程仓库分支名>

克隆仓库：

cd 路径 git clone 网址

创建本地分支 git branch <分支名>

合并分支 git merge <分支名>

添加pull请求 git pull requst

windows 专业版右键有git Bash选项，可以在进入目标文件后，右键选择该项，这样就可以不用每次都打cd命令，而且还有历史命令可以直接使用，直接点击桌面的git.bash是没有这种功能的

git commit 规范

添加文件：Add name

删除：Delete name

更新：Update name

回滚到某一版：Revert 哈希码前四位

跟源分支：1. git remote add upstream 地址 如(git remote add upstream https://github.com/octocat/Spoon-Knife.git)
          2. git fetch upstream
          3. git merge upstream/master
