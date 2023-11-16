# AnotherGit

Want to use 2 or more github accounts? Try it in Windows sandbox directly! | 想在一台电脑使用多个Github账户？AnotherGit能一键在Windows沙盒中启用另一用户。

## 前言

这也许是一个很小众的需求：在一台(Windows)电脑上，使用不同的Github账号，进行commit并push到Github上。

可以写脚本进行切换，操作完再切回来（后面可能写写）；也可以直接写个“脚本”，双击配置文件打开Windows自带的沙盒，开箱即用，沙盒中直接配置好了第二个Github账号的身份。

## 使用方法

1. 在Windows上启用Windows Sandbox（[参考链接](https://learn.microsoft.com/zh-cn/windows/security/application-security/application-isolation/windows-sandbox/windows-sandbox-overview)）
2. 将本仓库下载到本地，并修改```Codes/main.wsb```中的配置。包括：本仓库下载到的位置（第4行）、你宿主机上Git安装的位置（第9行）
3. 修改```Codes/ToCopy/.gitconfig```中你的Github邮箱和用户名
4. 将```Codes/ToCopy/.ssh```下的```id_rsa```和```id_rsa.pub```替换为具有Github操作权限的ssh key（[参考链接](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)）
5. 双击```Codes/main.wsb```（选择“通过沙盒打开”）
6. 在沙盒中进行地使用Git吧！身份已经切换为了新配置的Github用户，```git```也被添加到了环境变量中
