怎样将本地文件上传到GitHub

设置git的用户名和密码就不说了

第一步、git init
成功后  在文件下面 会生成一个 .git文件  如果你看不到 那就是隐藏了

第二步、git add .      /*注意add后面有个空格*/
成功后 无提示 直接下一步

第三步、git commit -m "css"           /* 分号里面写的是 描述区域*/
成功后 就会显示出你的文件

第四步 $ ssh-keygen -t rsa -C "xxx@outlook.com"   /*生成本地ssh密钥*/
成功后 看到 一长串 最后 有个虚线框  应该就是成功了

第五步、在远程创建ssh 密钥 在github里面新建ssh密钥 具体操作点击你的头像 点击下拉栏的倒数第二个 也就是  Settings 再找到 SSH and GPG keys 再然后点击 右上角的  New SSH key  title名字随便取  下面的文本框的内容 在C盘用户下面找到 .ssh 文件 打开下面的 id_rsa.pub 复制到 GitHub里面 再然后点击 Add SSH key

第六步、新建仓库  进入 仓库主页 点击 New   填写仓库名字 需英文 下面的描述可以不用写  再然后 直接 Create repository

以上三步是我使用 ssh协议的  也可以使用 https 协议 

第七步、git remote add origin     github的仓库地址
成功后 没有反应

第八步、git push -u origin master /*提交*/
成功后  下面会加载上传的文件


过滤文件
1、输入 touch .gitignore ，生成“.gitignore”文件。

2、打开”.gitignore” 文件，输入你要忽略的文件夹及其文件就可以了。（注意格式:文件夹后面 加上 \ 文件的话直接写文件名）


克隆到本地
git clone 远程仓库的ssh地址



更新代码
第一步：查看当前的git仓库状态
git status

第二步：更新全部
git add *

第三步：接着输入git commit -m "更新说明"
git commit -m "更新说明"

第四步：push到远程master分支上
git push 远程地址 master   /*注意这里看你的分支叫啥名字 就上传啥名字*/


总结: 现在大多数用的是ssh，少用https,  git 的ssh key 只需要创建一次即可   做项目优先选码云（没用过 以后到公司有需要的话，再用吧），找项目用 github（找资料一直用的就是这个 香的丫批 嘻嘻 ）。



