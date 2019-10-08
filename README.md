

值得推荐的其他客户端electron-ssr
first step:install shadowsocks-qt5

#Ubuntu 14.04及更高版本
#添加ppa源
sudo add-apt-repository ppa:hzwhuang/ss-qt5
sudo apt-get update
sudo apt-get install shadowsocks-qt5

如果你的系统是ubuntu18+，在你的/etc/apt/sources.list.d目录下，看这个文件(hzwhuang-ubuntu-ss-qt5-bionic.list )将里面的bionic改成xenial ,保存再运行 sudo apt-get update ,最后再运行一次 sudo apt-get install shadowsocks-qt5 就好了。
因为在ppa:hzwhuang/ss-qt5 并没有18.04版本的源，所以再执行update时会出现这个错误。
second step:run shadowsocks-qt5

sudo ss-qt5

but if you get this problem

ss-qt5: error while loading shared libraries: libQtShadowsocks.so.1: cannot open shared object file: No such file or directory
apt install libqtshadowsocks libqtshadowsocks-dev仍无效
ubunut 16.04 4.10.0-30-generic

you can use this

cp /usr/lib/libQtShadowsocks.so /usr/liblibQtShadowsocks.so.1

then rerun the commant:

sudo ss-qt5

third step:set the config-----

connection->add
input you config like this
这里写图片描述

click 'ok', and start connect
forth: set the config of chrome

use switchyomega , according to the page:
http://jingyan.baidu.com/article/11c17a2c121c0ff446e39d16.html

if you still can not connect to google,please set the Proxy servers protocal like this
这里写图片描述

then you can use auto or Goagent
这里写图片描述

这里写图片描述

reference:
https://github.com/shadowsocks/shadowsocks-qt5/issues/511
http://jingyan.baidu.com/article/11c17a2c121c0ff446e39d16.html
