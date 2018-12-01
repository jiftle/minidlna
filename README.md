# minidlna

#### Intridute
minidlna 1.2.1的克隆版本，添加rmvb格式支持。
参考https://blog.csdn.net/JOYIST/article/details/79191765


#### How to do

```
# ---------------------------
# install require library
# ---------------------------
sudo apt-get install build-essential libexif-dev libjpeg-dev libid3tag0-dev libflac-dev libvorbis-dev libsqlite3-dev libavformat-dev autoconf automake  
  
# ---------------------------
# complie install
# ---------------------------
./autogen.sh  
./configure  
make  
make install  
sudo cp ./linux/minidlna.inot.d.script.tmpl  /etc/init.d/minidlna  
sudo cp ./minidlna.conf  /etc/minidlna.conf  
  
# debug model run app 第一次启动使用-d –v选项看有没有出错  
sudo /usr/local/sbin/minidlnad -d -v  
# 没出错就ctrl+c 结束进程  
  
# normal model run as service 正常启动  
sudo service minidlna start  
# refresh server 刷新列表  
sudo service minidlna restart 
```
