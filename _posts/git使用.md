想要将自己的项目部署到远程仓库(国外github国内gitee),必须安装好git,具体安装方法一路点击下一步即可
安装好之后需要生成密钥对,如果没有设置git信息设置一下
        git config --global user.email "你的邮箱"
        git config --global user.name "你的名字"
    1.电脑本地生成密钥对
        终端运行ssh-keygen 命令 ,ssh key generate
        回车默认即可
        从生成本地文件路径中找到公钥C:/用户/asus/.ssh    id_rsa.pub  公钥  id_rsa私钥
        用文本方式打开,全选复制,在远程仓库设置中找到SSH公钥生成公钥即可使用SSH
**下面的方法是本人亲测最快的部署方法:**
在远程仓库中新建仓库,新建时注意把  使用readme.md取消勾选,(readme.md文件最好还是本地创建)
创建好之后,仓库会推荐几条命令,
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190812204047997.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xpeGlhbmcwMDA3MTY=,sie_16,color_FFFFFF,t_70)
把图中红框勾选的那条,复制上在想要部署到远程仓库的文件夹下,鼠标右键打开Git Bash 命令行工具
粘贴回车
如果报错,可以先使用git init然后在使用上面那条命令即可
进入ide中,我这里用的pycharm
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190812204417691.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xpeGlhbmcwMDA3MTY=,size_16,color_FFFFFF,t_70)
在红框中勾选你要上传的文件,点击右下角的commit保存或者点击commit旁边的小箭头选择,最上面的命令(保存并提交),如果只点击了保存的话在文件窗口中右击
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190812204652581.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xpeGlhbmcwMDA3MTY=,size_16,color_FFFFFF,t_70)
选择对应命令即可完成部署