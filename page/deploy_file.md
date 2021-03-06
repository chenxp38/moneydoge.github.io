## 服务端部署说明

---

#### mysql部署

- 直接从宝塔界面安装mysql，然后开放mysql的默认端口3306即可。后续我们要对数据库进行操作时，我们可以通过在使用Navicat对服务器上的数据库进行操作。

#### redis部署

- 在网上获取到redis的安装链接，在服务器安装后，我们开启一个screen用于运行redis，然后将redis放在后台运行即可。同样的，我们需要在宝塔界面开放redis的默认端口。

#### java部署

- 在网上获取java链接，在服务器上安装之后，部署对应的环境变量。然后在服务器的命令行上输入java -version有反应后代表java安装成功。

#### 后端程序的部署

- 在部署了基本环境之后，我们将后端程序通过IDEA的maven生成的jar包通过filezile传输到服务器上，然后输入java -jar *.jar即可完成对应的后端程序的部署。
- 需要注意的是：
  - 1.后端程序的端口不可以跟原本的默认端口重合，也不可以使用危险的端口（例如6666）。然后我们需要在宝塔界面开放我们服务端程序需要使用的端口即可完成后端程序的部署。
  - 2.后端程序需要运行的后台，可以使用screen来进行，通过screen -S生成screen，然后把后端程序放在这里运行即可完成后端程序在后台的部署。