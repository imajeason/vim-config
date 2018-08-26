# vim-config
my vim config to share amongst my machines

一、安装vim

yum install -y gcc gcc-c++ ruby ruby-devel lua lua-devel  \
    ctags git python python-devel \
    tcl-devel ncurses-devel \
    perl perl-devel perl-ExtUtils-ParseXS \
    perl-ExtUtils-CBuilder \
    perl-ExtUtils-Embed \
    vim-enhanced

#ubuntu
#sudo apt-get install libncurses5-dev


cd ~
git clone https://github.com/vim/vim.git
cd vim
./configure --with-features=huge \
--enable-multibyte \
--enable-rubyinterp=yes \
--enable-pythoninterp=yes \
--with-python-config-dir=/usr/lib64/python2.7/config/ \
--enable-python3interp=yes \
--with-python3-config-dir=/usr/local/lib/python3.7/config-3.7m-x86_64-linux-gnu/ \
--enable-perlinterp=yes \
--enable-luainterp=yes \
--enable-gui=gtk2 --enable-cscope \
--prefix=/usr/local/vim


make && make install

二、安装vundle
git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
