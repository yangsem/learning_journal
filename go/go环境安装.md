# Go环境安装

## 1. Linux环境安装

- 到官网下载安装包，`go1.22.5.linux-amd64.tar.gz`，[下载地址](https://go.dev/dl/)
- 创建存放go安装包的位置：`mkdir ~/bin/go`
- 解压 安装包`tar zxvf go1.14.7.linux-amd64.tar.gz -C ~/bin/go`
- 设置环境变量到`~/.baserc`：`export PATH=~/bin/go/bin:$PATH`，然后`source .bashrc`
- 输入`go`，验证是否go生效

- 会导致vscode的go插件报错

## 2. Linux下使用gvm安装

[gvm github](can't load package: package ./cmd/dist: found packages build.go (main) and notgo120.go (building_Go_requires_Go_1_20_6_or_later) in /home/yangsem/.gvm/gos/go1.22.5/src/cmd/dist)

```
$ sudo apt-get install bison
$ bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
$ source ~/.bashrc
$ gvm install go1.4 -B
$ gvm use go1.4
$ export GOROOT_BOOTSTRAP=$GOROOT
$ gvm install go1.17.13
$ gvm use go1.17.13
$ export GOROOT_BOOTSTRAP=$GOROOT
$ gvm install go1.20
$ gvm use go1.20
```

安装新版本时根据报错安装依赖的版本即可

查看go 安装了哪些版本：

```
$ gvm list
```
