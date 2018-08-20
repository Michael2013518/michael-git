## Git Demo Library.
> 1. Bootstrap
> 2. jQuery
> 3. HTML5 + CSS3
> 4.font library

### Git Command list
git help -a  /git的所有帮助命令/
git help -g  /git的使用手册/

> Git配置文件

git config --global user.name 'michael' /设置配置文件/

git config --global unset user.name 'Michael' /重新设置/

git config --list  /查看所有配置文件/

cat ~/.gitconfig  /获取别名配置文件/

>基础

git init /初始化/

git commit /提交/

git diff /对比文件区别/
git diff master..mobile-feature /对比分支区别或分支上文件的区别/

git rm style.css /删除文件/

git mv style.css theme.css /重命名文件或移动文件/

git checkout HEAD -- index.html /HEAD:最近一次提交，HEAD^上上一次提交，--：当前分支；恢复刚刚删除或修改的文件/

git revert bb95e87 (id) /恢复文件的历史版本/

git reset --soft bb95e87 / --mixed| --hard，重置提交，控制头部指针/

git stash save files /保存工作进度/
git stash list    /显示暂存工作进度/
git stash show -p stash@{0} /对比工作进度跟现在工作目录区别/
git stash apply stash{0} /恢复工作进度/
git stash drop stash{0} /删除工作进度/

git branch -m bugfix hotfix /重命名分支/
git branch -d bugfix  /删除分支/

git checkout -b dev  /创建并切换分支/

git clone  /克隆远程git/

git fetch /提取远程分支/


>Create a new repository

git clone http://192.168.232.10/michael/web-protype.git
cd web-protype
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master

>Existing folder or Git repository

cd existing_folder
git init
git remote add origin http://192.168.232.10/michael/web-protype.git
git add .
git commit
git push -u origin master
