
一，git配置

git config --global core.editor "vim"
git config --global user.name 
git config --global user.email 

二，git回退
```
    根据–soft –mixed –hard，会对working tree和index和HEAD进行重置:  
    
    git reset –mixed <commit_id>：
       此为默认方式，不带任何参数的git reset，即时这种方式，它回退到某个版本，只保留源码，回退commit和index信息
    git reset –soft <commit_id> ：
       回退到某个版本，只回退了commit的信息，不会恢复到index file一级。如果还要提交，直接commit即可
    git reset –hard <commit_id> ：
       彻底回退到某个版本，本地的源码也会变为上一个版本的内容
```
三，git操作  
```
git checkout -b 4.2/2561.bak remotes/origin/4.2/2561    创建远程分支remotes/origin/4.2/2561到本地分支 4.2/2561.bak，

git push origin :remotes/origin/4.2/2561            删除远程分支

git push orign  localbranch：/4.2/2561            推本地库localbranch 到远程分支 origin/4.2/2561

git branch --set-upstream-to=origin/4.2/daily-build      设定本地分支跟踪的远程分支

git pull 同步当前跟踪的远程分支 到本地

git branch -vv 查看本地分支对应的远程分支

git branch -d  删除本地分支

git branch -m a b 将本地分支a 改名为b

git remote add origin git@github.com:Tnkld/Note.git 关联本地库与远程库

git commit --amend 修改上一个commit

git push origin HEAD --force
```

