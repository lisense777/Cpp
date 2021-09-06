​	s![1621961447032](C:\Users\老大哥\AppData\Roaming\Typora\typora-user-images\1621961447032.png)

![1621962258012](C:\Users\老大哥\AppData\Roaming\Typora\typora-user-images\1621962258012.png)

![1622002783224](C:\Users\老大哥\AppData\Roaming\Typora\typora-user-images\1622002783224.png)

![1622003345236](C:\Users\老大哥\AppData\Roaming\Typora\typora-user-images\1622003345236.png)

## github中的冲突问题及解决

1.由于每次的更新都是基于本地仓库进行更新的，若有多个人同时提交，提交慢的人是基于原来本地仓库的内容进行更新的，但是此时的本地仓库已经被更新，提交慢的人就无法完成提交（基于修改的本地仓库已被修改）此时就需要git pull更新本地仓库再进行修改。

2.如果修改的是同一个地方  则需要手动解决冲突    git pull 拉取更新后的代码   git如果可以merge就不需要其他操作  否则就自己手动解决冲突。

## git分支管理

当想对于原来分支进行修改时，可以创建一个新分支（但是新创建的分支需要追踪一个远程仓库的分支）



创建的新分支只是本地仓库的一个新分支，并没有追踪到远程仓库的分支



创建分支的命令：git branch  【name 】 

切换分支：git branch 【name】

删除分支：git branch -d/D（硬性） 

合并分支： git merge 【name】将【name】分支合并到本地分支

git push origin sortdev:main      **指定推送到远端的的分支**

## 本地分支合并解决方案

多人同时拉取了远程仓库的代码的情况下，一个人对其进行创建分支并合并，再将其推送到远程仓库；而此时其他人（git pull）之后也进行了修改------------同时更新出了多个版本的  main ，第一个人再将其进行合并到main分支上，就出现了合并冲突（合并冲突都是合并到远程仓库（即本地分支追踪的远程分支））



需要手动合并 再推送到远端仓库