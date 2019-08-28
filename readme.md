# 初始化Git仓储/（仓库）

- 这个仓库会存放，git对我们项目代码进行备份的文件
- 在项目目录右键打开 git bash here
- 执行命令`git init`  备注（进入仓库里面）

## 自报家门（配置信息）
- 就是在git中设置当前使用的用户是谁
- 每一次备份都会把当前备份者的信息存储起来
- 命令：
    + 配置用户名: `git config --global user.name "xiaoming"` 
    + 配置邮箱: `git config --global user.email "xiaoming@sina.cc"`

## 把大象放到冰箱要几步
1.打开冰箱门
2.放大象
3.关上冰箱

## 把代码存储到.git仓储中
1.放到大门口 
+ `git add ./readme.md`   把指定的文件放到大门口
+ `git add ./`   把所有的修改的文件添加到大门口  
+ `git add .` **git add .** ：会监控工作区的状态树，使用它会把工作时的所有变化提交到暂存区，包括文件内容修改(modified)以及新文件(new)，但不包括被删除的文件。

2.把仓储门口的代码放到仓储房间里 

+ `git commit -m "我们完成了第一个功能！"`   备注（这是对这次的代码提交的说明）
+ `git commit --all -m "一些说明"`   备注 ： **--all表示把所有修改的文件一次性提交到版本库**
~~~注意如果第2步中的代码少写了 -m 会进入一个输出窗口，执行以下操作
1.按esc 
2.在英文输入状态下输入:q! 退出窗口（添加感叹号!为强制退出，不加为退出） 
~~~

# 可以一次性把我们修改的代码放到房间里（版本库）

~~~
git commit --all -m "注释说明"
--all 表示把所有修改的文件提交到版本库
~~~



# 查看当前的状态

- 输入 git status看窗口中绿色的字，检查当前是否把文件放到暂存区了
- 可以用来查看当前代码有没有被放到仓储中去
（status状态）
- 命令: `git status`



# git中的忽略文件

- .gitignore,在这个文件中可以设置要忽略的文件或者目录。
- 被忽略的文件不会被提交到仓储中去。
- 在.gitignore中可以书写要被忽略的文件的路径，以/开头，一行写一个路径，这些路径所对应的文件都会被忽略，不会被提交到仓储中
  - 写法 
    - `/.idea` 会忽略.idea 文件
    - `/js` 会忽略js目录中的所有文件
    - `/js/*.js` 会忽略js目录下所有js文件

# 查看日志

查看历史提交的日志

```
   git log 查看日志详细信息
   git log --oneline 更精简的日志信息

```

# 版本回退

## 回退到指定的版本

~~~
git reset --hard head~0
//表示回退到上一次代码提交的时候
~~~



~~~
git reset --hard head~1
//表示回退到上上次代码提交的时候
~~~

