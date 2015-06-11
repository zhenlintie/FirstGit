#本地git仓库，并连接到github远程仓库(Mac)
______
## 创建SSH Key
  1. 打开终端，输入以下命令:<br>
	```
	$ ssh-keygen -t rsa -C "your@example.com" // 双引号内是github邮箱账户
	```
	<br>回车，直到完成。
  2. 切到用户名目录下，找到`.ssh`目录中的`id_rsa.pub`，这是公钥。**复制里面的内容**
  3. 登录[github](https://github.com),点击`Settings`图标,并切换到`SSH Keys`下。
     点击`Add SSH Key`，填写`title`，并将之前复制的`id_rsa.pub`内容复制到`key`，点击`Add Key`完成。

## 远程仓库
  1. 登录github网站后，切到个人主页。
  2. 切到`Repositories`,并点击`New`，新建仓库。
  3. 起名字为`FirstGit`，其他选项暂时默认。完成创建。
    
 界面会许多提示，_**可以将仓库clone到本地，则无需再进行连接**_
 <br>这里为了测试建立本地仓库与远程仓库的连接，直接做了下面的操作。

## 建立本地仓库，并连接到远程
  1. 建立本地文件夹`FirstGit`，切到`FirstGit`目录下
  2. 创建`README.md`文件
  3. git命令
``` shell
$ git init  // 创建版本库
$ git add README.md // 为版本库添加README.md 文件
$ git commit -m "first commit" // 提交更新
$ git remote add origin git@github.com:XXXX/FirstGit.git // 连接github远程仓库 XXXX为github用户名
$ git push -u origin master // 推送更新，origin：远程库的名，master：分支名，这是主分支
```

#### 最后在github网站刷新一下，应该可以看到README.md文件的内容了。
*_这一篇_就是测试结果。*


感谢廖雪峰老师的[git教程-远程仓库](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000)
