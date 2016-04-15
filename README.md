# linux_setup
![image](https://github.com/hejie/linux_setup/raw/master/pics/setup.jpg)

1.删除libreoffice
sudo apt-get remove libreoffice-common

2.删除Amazon的链接
sudo apt-get remove unity-webapps-common

3.命令行模式复制到系统剪切板
xclip -sel clip < ~/.ssh/id_rsa.pub

4.vim 系统剪切板
注意附加
sudo apt-get build-dep vim
sudo apt-get install python-dev
下载源码
git clone https://github.com/vim/vim.git
重新编译
./configure \ --enable-perlinterp --enable-pythoninterp --enable-rubyinterp --enable-cscope --enable-gui=auto --enable-gtk2-check --enable-gnome-check --with-features=huge --with-x --with-python-config-dir=/usr/lib/python2.7/config
make && sudo make install
输入reg 若寄存器列表里无”* 或 “+ 寄存器，则可能是由于没有安装vim的图形界面所致。Debian/Ubuntu下可以通过安装vim-gnome解决。
sudo apt-get install vim-gnome


