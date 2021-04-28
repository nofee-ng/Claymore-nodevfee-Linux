## This NoDevFee program is out dated. Please use Next Generation NoFee (aka *nofee-ng*) at [https://github.com/nofee-ng/nofee-ng](https://github.com/nofee-ng/nofee-ng) . If you're looking for a Windows edtion, check [https://github.com/nofee-ng/eth-nodevfee](https://github.com/nofee-ng/eth-nodevfee) ##

---

ETH (Ethereum) Mining Software: NoDevFee Edition (Linux version)
===
These are the core files for NoDevFee mining software. And they **CAN NOT** be used stand alone. Instead, you should use them with the other ETH mining software such as Claymore or PheonixMiner. You can also download the bundled package in the release page.

### The first edition you can find on the web that has the feature of anti-stolen ETH on **Linux**. ###

### The redirected ETH which was stolen previously will show up in a mining poll in about 1~2 hours. Please be patient! ###

# Make sure you change the wallet address in `config.txt` and `nodevfeeWallet.txt`. #

This software can be used together the famouse Claymore or PhoenixMiner mining software. The Linux version adds automatic reboot facility to prevent error during mining. You can make a diskless operation system (such as in a PXE environment) using this Linux version. Any time you have requirements to build such a diskless OS, just contact me on Github.

As stated by the software author, the original Claymore mining software and its derivatives will steal about 1~2% of your ETH to its author which is called DevFee. In this edition I added a new feature: NoDevFee. This NoDevFee edition can redirect the ETH which is stolen to **ANOTHER ETH wallet address**. Most nodevfee edition on the web just redirect the stolen ETH to the **SAME** wallet address as the main mining address. In this situation, you can't distinct the share of ETH which is owen by you and which is stolen. 

## Usage ##

1. Change the file config.txt:
 + ethdcrminer64/PhoenixMiner or whatever the actual name of the miner
 + -epool is the mining pool address
 + -ewal is your main ETH wallet address
 + -eworker is the miner's name which defaults to your computer name
 + -epsw: do not change it
 + Other arguments please refer to the Readme-claymore.txt
2. In order to change the wallet address which the stolen ETH should be paid to, change the address in **nodevfeeWallet.txt**. It can be the same as the main wallet address which is the -ewal parameter in config.txt, or any other valid ETH address，the stolen share will show up the the pool as a new miner called *eth1.0*.
3. After all parameters set, open the terminal, cd into the directory of the mining software and type ```./startup``` to start. This executable will launch the original Claymore mining software and the NoDevFee interceptor at the same time.
4. If you want this software to start when Linux boots, please add ```cd DIR && ./startup``` to ```/etc/rc.local```，where DIR is the directory of your mining software.

---

## 该Linux版的NoDevFee程序已经过时。请使用下一代nofee挖矿软件*nofee-ng*：[https://github.com/nofee-ng/nofee-ng](https://github.com/nofee-ng/nofee-ng) ，如果你想使用Windows版，请查看 [https://github.com/nofee-ng/eth-nodevfee](https://github.com/nofee-ng/eth-nodevfee) ##

---

ETH(Ethereum)以太坊挖矿软件反抽水版（Linux版）
===
本软件提供了反抽水程序的核心功能。需要注意的是，本软件**不能单独使用**，它必须配合其它软件，如Claymore或PheonixMiner等一起使用。你也可以在release页面找到打包好的程序整个下载。

### 市面上第一个基于**Linux**的反抽水软件！ ###

### 反抽水的结果大概需要1~2小时才能在矿池中看到，请耐心等待 ###

# 使用前请确保您已更改 `config.txt` 及 `nodevfeeWallet.txt` 中的钱包地址 #

本软件配合著名的Claymore或PhoenixMiner等挖矿软件使用。Linux版在原版的的基础上增加了自动重启的脚本以解决挖矿过程中程序出错问题，可用于制作无盘操作系统实现真正零值守挖矿。如有无盘操作系统这方面的需求，请在Github上给我留言。

众所周知，Claymore原版及其它基于Claymore的探矿软件是会抽水的（大概1~2%）。相比原版，本版加入反抽水功能，能把劫持的算力重定向到**另一个ETH钱包地址**。市面上的反抽水软件均是重定向到同一个地址（即主钱包地址），*因而无法区别原来的算力和被劫持的算力*。

## 使用方法 ##

1. 修改配置文件config.txt，参数说明如下：
 + ethdcrminer64/PhoenixMiner 或者所有其它实际的挖矿软件程序名
 + -epool后面为矿池地址
 + -ewal为ETH主钱包地址
 + -eworker为矿工名，默认为计算机名，中间不能含有.
 + -epsw参数不要改
 + 其它参数请参考Readme-claymore.txt
2. 要修改劫持回来的钱包的地址，请修改**nodevfeeWallet.txt**里的地址，可以改成和config.txt中-ewal参数一样的主钱包地址，也可以用另外的地址，劫持回来的算力将以矿工名*eth1.0*显示
3. 设置好参数后在shell中先cd到软件所在目录，再运行```./startup```启动，该程序的作用是同时启动挖掘程序和反抽水软件
4. 如果需要自动启动，请修改```/etc/rc.local```，内容为```cd DIR && ./startup```，其中DIR为挖矿软件所在目录。
