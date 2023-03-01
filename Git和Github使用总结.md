# Git和Github使用总结

设置用户名邮箱：https://docs.github.com/zh/get-started/getting-started-with-git/setting-your-username-in-git

1. 在github上创建一个 repository 并且copy这个repo http

   比如 ：https://github.com/Michael-Alz/Git_Test.git

2. 在本地创建一个仓库 

   ~~~shell
   git init
   ~~~

3. 使用git pull or clone

   ~~~shell
   git pull https://github.com/Michael-Alz/Git_Test.git
   git clone https://github.com/Michael-Alz/Git_Test.git
   ~~~

​		pull是从github仓库下载到本地仓库，会把本地的文件覆盖掉

​		clone载入远程仓库并且是直接下载整个文件夹

4. 修改下载下来的文件

5. 添加文件到暂存区

   ~~~shell
   git add . #添加当前目录下全部文件
   git add [file1] [files] 	
   git add [dir] #添加指定目录，包括子目录
   git status #查看修改状况
   ~~~

6. commit提交暂存区内容添加到本地仓库

   ~~~shell
   git commit -m 'message' 
   ~~~

7. 显示远程仓库

   ~~~shell
   git remote -v
   origin	https://github.com/Michael-Alz/Git_Test.git (fetch) #origin是远程仓库的别名
   origin	https://github.com/Michael-Alz/Git_Test.git (push)
   ~~~

8. 添加远程仓库

   ~~~shell
   git remote add https://github.com/Michael-Alz/Git_Test.git
   ~~~

9. push到远程仓库

   ~~~shell
   git push <远程主机名> <本地分支名>
   git push -u origin main #注意这里是main不是master
   ~~~

   注意如果使用http网址需要输入github用户名和密码，**密码是Personal Access Token**（https://github.com/settings/tokens）

   ~~~shell
   git config --global credential.helper cache #输入完一遍以后，可以用这个命令记住用户名和密码
   ~~~

   
