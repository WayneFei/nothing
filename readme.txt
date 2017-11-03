##版本控制系统：
   集中式 SVN -- 拉下来，再更新
   分布式 git -- 将各自修改内容提交

```
 git config --global user.name "Your Name"
 git config --global user.email "email@example.com"
```

##初始化Git仓库
``` 
 git init
```

##添加文件到Git仓库
添加文件到Git仓库，分两步：
: 第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；
: 第二步，使用命令git commit，完成。
```
 git add readme.txt 
 git add one.txt two.txt
 git add **/*.js
 git commit -m 'descript'
```

##查看提交历史
用git log可以查看提交历史，以便确定要回退到哪个版本。
用git reflog查看命令历史，以便确定要回到未来的哪个版本。
```
 git log
 git log --pretty=oneline
```

##版本回退

```
 git reset --hard commitID // commitID是版本号，不必写全，git会自动查找
 git reset --hard HEAD^    // 回退到上一版本
 git reset --hard HEAD^^   // 回退到上上个版本
 git reset --hard HEAD~100 // 回退到前100个版本
```

##远程仓库

先有远程仓库，再克隆到本地

```
// 链接地址可以使http地址，也可以是ssh地址
 git clone git@github.com:...git/https://github.com/Wayne0117/...git
```

先有本地仓库，再添加远程仓库
```
 //关联一个远程库
 git remote add origin git@github.com:WayneFei/gitDemo.git
 //第一次推送master分支的所有内容
 git push -u origin master
 //之后推送最新修改
 git push origin master
 //移除远程仓库
 git remote rm origin  
```

```
 // 提交代码
 git push
 // 更新最新代码
 git pull
```
##创建合并分支

```
 // 创建分支
 git branch <name>
 // 查看分支
 git branch
 // 切换分支
 git checkout <name>
 // 创建并切换到对应分支
 git checkout -b <name>
 // 提交新分支
 git push --set-upstream origin <name>
 // 合并某分支到当前分支
 git merge <name>
 // 删除分支
 git branch -d <name>
```

