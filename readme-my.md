[TOC]

# github-code 
  基础github使用笔记`myfirsttest`。
   
  use SSH: ` $ git clone git@github.com:wenjayliu/myfirsttest.git`  
  use https:` $ git clone https://github.com/wenjayliu/myfirsttest.git`

### 关联仓库
___
 - 先在github上建立仓库 
 - 不会像 `git clone` 那样在本地创建仓库文件夹
 - 本地倉庫 与 远程仓库 建立连接关系
 
```
1. 初始化 創建本地倉庫 将在本地运行目录下生产 `.git`文件夹（默认隐藏），且  默认本地为 `master` 分支
$ git init  
2. 关联远程（github网站）的自建仓库。
$ git remote add origin git@github.com:wenjayliu/myfirsttest.git
3. 下载远程的 `readme.md` 等文件 (远程默认为) `origin` 分支
$ git pull origin master    //慎用
```

___

### 提交
 - 本地修改后上传到远程服务器
```
$ git add .     						// 1 `.` 所有已修改的文件.  2文件名`,`分割
$ git commit -m "提交說明"
$ git push origin master

```

### 五個常用命令.
```
//下載倉庫
$ git clone <版本库的网址> 

//远程主机名
$ git remote  

//更新取回本地   (git merge origin/master)
$ git fetch <远程主机名>

//取回远程主机某个分支的更新，再与本地的指定分支合并  
$ git pull <远程主机名> <远程分支名>:<本地分支名>

//推送到远程主机  
$ git push <远程主机名> <本地分支名>:<远程分支名>
```
> 注意，分支推送顺序的写法是<来源地>:<目的地>，
s如果发现 “fatal: 远程 origin 已经存在” 的错误,执行下面指令后再执行上面指令



### clone
```javascript
$ git clone https://github.com/wenjayliu/react-newer.git

$ git fetch origin

$ git merge origin/master
```
### 回滾

1.查看日志

```javascript
$ git log 		//日志
$ q				//退出
$ git reset
$ git reset -hard "commit值"

```

### SSH 免密码
```
$ ls -al ~/.ssh                                      //展示文件  详细信息  路径 文件名  （查看是否有id_rsa.pub）
$ ssh-keygen -t rsa -b 4096 -C "865015063@qq.com"    //（生成ssh key）
$ eval "$(ssh-agent -s)"                             //(确保ssh-agent已启用 )
$ssh-add ~/.ssh/id_rsa                               //(将创建好的ssh key添加进ssh-agent)

				"将公钥的内容添加到你的github账户"
				
$ git remote add origin git@github.com:username/repositorie.git  //(修改远程项目地址为SSH传输方式)
$ git remote -v

```

### 其他

查看远程分支
    $ git branch -r
    
    

    
___
##  Markdown展示 `/readme.md`

```
	//展示图片
 ![](https://raw.github.com/meolu/walle-web/master/docs/logo.jpg)
```
- 效果

 ![](https://github.com/wenjayliu/base-css/blob/master/components/ullibeautify.PNG)
 

___
```
	//文本超链接
	[base css ol style](https://wenjayliu.github.io/base-css/components/ul-li-c.html)
```
- 效果
	[base css ol style](https://wenjayliu.github.io/base-css/components/ul-li-c.html)
	
___

```
[![Build Status](https://travis-ci.org/meolu/walle-web.svg?branch=master)]
[![GitHub forks](https://img.shields.io/github/forks/badges/shields.svg?style=social&label=Fork)]()
```
- 效果

[![Build Status](https://travis-ci.org/meolu/walle-web.svg?branch=master)](http://shields.io/)
[![GitHub forks](https://img.shields.io/github/forks/badges/shields.svg?style=social&label=Fork)]()







