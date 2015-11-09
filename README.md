# -YouCompleteMe
安装YouCompleteMe 在32位Ubuntu 15.10上

--------------------------------------------------------------------------
http://blog.csdn.net/leaf5022/article/details/21290509
http://zuyunfei.com/2013/05/16/killer-plugin-of-vim-youcompleteme/


---------------------------------------------------------------------------
一、下载LLVM库源码

mkdir ~/ycm_temp

cd ~/ycm_temp

wget http://llvm.org/releases/3.7.0/llvm-3.7.0.src.tar.xz

wget http://llvm.org/releases/3.7.0/cfe-3.7.0.src.tar.xz

tar -Jxf llvm-3.7.0.src.tar.xz

tar -Jxf cfe-3.7.0.src.tar.xz

mv  cfe-3.7.0.src llvm-3.7.0.src/tools/

mkdir ycm_build

cd ycm_build

二、编译LLVM
cmake -G "Unix Makefiles" -DEXTERNAL_LIBCLANG_PATH=~/ycm_temp/llvm_build/lib/libclang.so 
~/.vim/bundle/YouCompleteMe/third_party/ycmd/cpp

make

三、编译YouCompleteMe

cd ~/.vim/bundle/YouCompleteMe

./install.py --clang-completer


