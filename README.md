Ubuntu系统Aleo zk.work 挖矿教程，Windows系统可以安装wsl Ubuntu子系统进行挖矿
一、使用FoxWallet 或Leo Wallet 创建Aleo钱包，获取钱包地址
  Fox谷歌浏览器插件： https://play.google.com/store/search?q=fox+wallet&c=apps&hl=zh_CN
  Leo谷歌浏览器插件： https://play.google.com/store/search?q=leo+wallet&c=apps&hl=zh_CN
二、Windows系统安装Wsl Ubuntu，若系统为Ubuntu或已安装wsl跳过该步骤
  1.在开始菜单中，搜索 "PowerShell"，然后右键点击，选择 "以管理员身份运行"。
    wsl --install --d ubuntu-22.04
  这会自动下载并安装 Ubuntu 22.04 LTS。
  设置 Ubuntu安装完成后，WSL 会自动启动 Ubuntu。你需要设置用户名和密码。
三、下载挖矿软件
  打开网址 https://github.com/6block/zkwork_aleo_gpu_worker/releases
  找到最新的挖矿软件 aleo_prover-v0.1.1_hot.tar.gz 并下载
  也可以使用wget获取最新挖矿软件：
  wget https://github.com/6block/zkwork_aleo_gpu_worker/releases/download/v0.1.1-hot/aleo_prover-v0.1.1_hot.tar.gz
  下载完成之后进行解压：
  tar -zvxf aleo_prover-v0.1.1_hot.tar.gz
  cd aleo_prover
  设置挖矿软件权限：
  chmod +x aleo_prover
  运行挖矿命令：
  替换 aleoxxx 为你自己的aleo钱包地址  myprove为矿工名称，可以自定义
  ./aleo_prover --pool aleo.hk.zk.work:10003 --address aleoxxx --custom_name myprove
四、查看挖矿进程以及奖励
  替换 aleoxxx 为上一步的aleo钱包地址，既可以在Zk.work网站上查询你的挖矿进程
  https://zk.work/en/aleo/address/aleoxxx/dashboard
说明：大陆机器由于网络问题需要运行VPN，若出现 Unable to link to pool 字样，则是自己的网络问题,此时若可以正常访问 https://www.google.com/ 
以clash为例，此时需要开启TUN 模式
