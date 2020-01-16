
# Placeholder for Readme; below are from @yangao07 's config

## Configuration without sudo permission (For C/C++ and Python)
### 1. install vim, enable python support
```
git clone https://github.com/vim/vim.git
cd vim
./configure --enable-pythoninterp
make
cp src/vim ~/bin
```
### 2. clone .vim directory
```
git clone https://github.com/yangao07/my.vim.git
mv my.vim ~/.vim
```
### 3. download libclang.so
```
wget https://releases.llvm.org/7.0.1/clang+llvm-7.0.1-x86_64-linux-gnu-ubuntu-18.04.tar.xz
tar xf clang*
```
vimrc:
```
let g:clang_library_path="/path/to/clang+llvm/lib"
```
### 4. vim command :BundleInstall
```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/vundle
vim
:BundleInstall
```
### 5. install YouCompleteMe
```
cd ~/.vim/bundle/YouCompleteMe
./install.py --clang-completer
```
### 6. set .ycm_extra_conf.py
vimrc:
```
let g:ycm_global_ycm_extra_conf='/path/to/.ycm_extra_conf.py'
```
