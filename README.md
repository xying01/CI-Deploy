# CI-Deploy
auto to deploy a TAC for testing Talend DQ QA patches
1. 如何把本地project 上传到github 上（9步）

 第一步：我们需要先创建一个本地的版本库（其实也就是一个文件夹）。
 你可以直接右击新建文件夹，也可以右击打开Git bash命令行窗口通过命令来创建。
 现在我通过命令行在桌面新建一个TEST文件夹（你也可以在其他任何地方创建这个文件夹），并且进入这个文件夹
1）mkdir CI-Deploy(结果是D：/ 多了一个 文件夹)
2）cd CI-Deploy
3)git init
4) copy 你得文件到 CI-Deploy
5)git add . (把该目录下的所有文件添加到仓库，注意点是用空格隔开的)
6)用git commit把项目提交到仓库
7)在Github上创建一个Git仓库。 (你可以直接点New repository来创建，比如我创建了一个TEST2的仓库)
8)在Github上创建好Git仓库之后我们就可以和本地仓库进行关联了，根据创建好的Git仓库页面的提示，可以在本地TEST仓库的命令行输入：
$ git remote add origin https://github.com/guyibang/TEST2.git
        注意origin后面加的是你Github上创建好的仓库的地址。
9)关联好之后我们就可以把本地库的所有内容推送到远程仓库（也就是Github）上了，通过：
   $ git push -u origin master
  由于新建的远程仓库是空的，所以要加上-u这个参数，等远程仓库里面有了内容之后，下次再从本地库上传内容的时候只需下面这样就可以了：
       $ git push origin master
 上传项目的过程可能需要等一段时间，完成之后是这样的：
 
 
 
 备注：
 另外，这里有个坑需要注意一下，就是在上面第七步创建远程仓库的时候，如果你勾选了Initialize this repository with a README（就是创建仓库的时候自动给 你创建一个README文件），那么到了第九步你将本地仓库内容推送到远程仓库的时候就会报一个failed to push some refs to  https://github.com/guyibang/TEST2.git的错。
参考 文献： 
https://blog.csdn.net/zamamiro/article/details/70172900

      

   
