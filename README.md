# test
This is a test for relation of git and  github
> 参考链接：https://blog.csdn.net/black_sneak/article/details/139600633
## Firststep
![image](https://github.com/user-attachments/assets/4f9462ac-2271-4e99-ba69-dcc02a1fd6d9)
## git&github绑定
### 2.4.1 得到ssh keys
输入 cd ~/.ssh，返回 "no such file or directory" 表明电脑没有ssh key，需要创建ssh key；

故在终端输入 ssh-keygen -t rsa -C “git账号”；

连续进行 3 次回车Enter（确认），得到如下截图中的信息即可； 

按路径进入 .ssh，里面存储的是两个 ssh key 的秘钥，id_rsa.pub 文件里面存储的是公钥，id_rsa 文件里存储的是私钥，不能告诉别人。打开 id_rsa.pub 文件，复制里面的内容。
### 2.4.2 绑定ssh密钥
1、接下需要登录到自己的 GitHub 上边添加这个密匙；

2、填写名字并且填写复制的公钥（id_rsa.pub内容），添加后配置完成。；

3、点击 Add SSH key，我们就成功添加 SSH Key 啦！

4、我们回到 Git bash上边，输入：ssh -T git@github.com
来检查是否成功绑定。如果输入代码之后再选择 yes 出来是这样说明就成功啦！！！ 

5、剩余简单的配置内容。
将 name 最好和 GitHub 上边的一样，email 是一定要是注册 GitHub 的那个邮箱地址

这两个的顺序可以颠倒，没有固定的顺序。

``` git config --global user.name “gitname”
git config --global user.email “git邮箱” ```

截止到这里的操作，已经完成本地 Git 与远程的 Github 绑定，这意味着我们已经可以通过 Git 向 GitHub 提交代码啦！

2.5 使用Git将代码提交到GitHub
该过程需要使用经常的接触的两个 Git 命令，包括：push和 pull

push：该单词直译过来就是 “推” 的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例：

git push origin master
pull：该单词直译过来就是 “拉” 的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例： 

git pull origin master
2.5.1 克隆仓库
1、将我们的库克隆下来到本地电脑中，方便以后进行上传代码。

2、点进仓库之后点击 Code，点击 ssh 会看到一串网址（http也可以），这个地址就是代码地址，git clone 命令会用的到。

3、接下来我们就开始选择文件存储地方了，在本地电脑中找到存储文件的地方，然后右键选择 Git Bash Here： 

4、在终端输入 git clone 地址（这个地址就是刚刚库那个Code的上代码地址）

该过程有时候可能会需要输入 Github 账号密码啥的，记得不要输错啦！ 

如下图所示，指定目录已经存在了我们的库文件 

2.5.2 上传代码
1、打开这个文件夹，然后在其中创建一个任意格式，任意名称的文件（这里新建了一个测试文件）。

2、在这个文件夹里面右键 git bash 进黑框框，git add 我们新增的文件

3、之后输入然后 git commit -m “测试是否成功” 引号内的内容可以随意改动，这个语句的意思是 给你刚刚上传的文件一个备注，方便查找记忆而已；

4、接着输入 push 指令 git push origin main，如下图所示就代表成功了；

5、打开 GitHub，看到刚刚上传的文件，显示成功。

到这里，本篇博客针对 Github 平台的使用教程就已经结束了！！！
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/black_sneak/article/details/139600633
