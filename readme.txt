1. git init(成了master)
2. git add ---.---
3. git commit -m "我是注释"
//2、3步骤——No newa is good news!
4. git status //查看是否有还未提交的文件
5. git diff 我是文件名 //查看修改的具体内容
6. git add, git commit -m "我又是注释" //修改之后，再次提交
7. git log 查看历史记录； git log --pretty=oneline 精简显示
8. git reset --hard HEAD^ 回退到上一个版本； ... HEAD^^ 回退到上面两个版本； ... HEAD~100 回退到往前数前第100个版本。
//这时候，log、cat（查看文本）都完成了回退。
9. git reflog //查看以往所有git版本号（包括回退的）
10.git reset --hard 我是版本号 恢复到版本
//补充：工作区和版本库的区别：被git init的文件夹都在工作区；隐藏目录.git就是版本库，里面有暂存区（stage），和一个分支master以及指向master的一个指针HEAD。一个add的，都在stage里，每一个commit的，就把暂存区的内容提交到当前分支上。总结顺序：工作区——>暂存区——>分支
11.check out -- <file> //放弃工作区的修改，此时有两种情况：如果尚未add到暂存区，则回到和上一个版本库一个状态；如果已经add到暂存区了，则回到暂存区后的状态撤销修改及删除文件
