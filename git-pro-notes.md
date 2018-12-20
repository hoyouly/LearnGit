## git diff
* git diff 比较的是工作目录中当前文件和暂存区之间的差异
* git diff --cached   查看已经暂存起来的文件和上次提交时候的差异，其实就是查看git add 后文件和已经提交上去的差异
* git diff --staged   在git 1.6.1版本以及更高版本使用，和git diff --cached 效果一样


## git commit
git commit -v 修改差异的每一行都包含到注释中来
git commit -a 自动吧所有已经跟着过的文件暂存起来一并提交，从而跳过git add 步骤

git commit --amend 重新编写提交说明，修正第一个提交的内容

## git log
参数列表
* -p   : 按照补丁格式显示每个更新之间的差异
* --stat  ：显示每次更新的文件修改统计信息
* --shortstat : 只显示 --stat 中最后的行数修改添加移除统计记录
* --name--only : 仅在提交信息后显示已修改的文件清单
* --name-status : 显示新增，修改，删除的文件清单
* --abbrev-commit : 仅显示SHA-1 的前几个字符，而非所有的40个字符
* --relative-date 使用较短的相对显示时间
* --graph 显示ASCII图形表示的分支合并历史
* pretty 使用其他格式显示历史提交信息，可用的选项包括
  * oneline     git log --pretty=oneline 将每个提交放在一行显示
  * short
  * full
  * fuller
  * format  格式化输出
  eg git log --pretty=format : "%h - %an ,%ar : %s"
    * %H 提交对象 commit的完整哈希子串
    * %h 提交对象的尖端哈希串
    * %T 树对象的完整哈希串
    * %t 树对象的简短哈希串
    * %P 父对象的完整哈希串
    * %p 父对象的简短哈希串
    * %an 作者的名字
    * %ad 作者修订的日期，可以用 -date=选项定制格式
    * %ar 作者修改日期，按多久以前的方式显示
    * %cn 提交者的名字
    * %ce 提交者的电子邮件
    * %cd 提交日期
    * %cr 提交日期，安多久以前的方式显示
    * %s 提交说明

* --since , --after : 仅显示指定时间之后的提交  
  eg: git log --since=2.weaks  列出最近两周内的提交
* --until  ,--before   : 仅显示指定时间之前的提交  
* --author  :  仅显示指定作者相关的提交
* --committer  :  仅显示指定提交者相关的提交

## git reset
取消暂存
git reset HEAD <file>  撤销add   <file> 文件的操作
git reset HEAD ^ 撤销所有add 的操作


## git 别名
git config --global alias.co  checkout   git co  相当于 git checkout
git config --global alias.br  branch     git br  相当于 git branch
git config --global alias.ci  commit     git ci  相当于 git commit
git config --global alias.st  status     git st  相当于 git status



















===
end
