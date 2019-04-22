# RustConAsia 2019大会workshop

### 环境准备

- Rust 最新稳定版
- Docker 

对于Mac环境，使用

- Docker Desktop for Mac 

或者 

需要使用docker-machine配置好docker 

```
// 确保已安装VirtualBox
$ brew cask install virtualbox;
$ docker-machine create --driver virtualbox default
$ docker-machine env default
$ eval $(docker-machine env default)
```

安装好postgresql的docker镜像,,或者使用Sqlite/Mysql

```
$ docker pull postgres
$ docker run --name postgres -e POSTGRES_PASSWORD=123456 -d postgres 
```

配置Cargo 镜像

```
$  sudo vi ~/.cargo/config
```

```rust
[source.crates-io]
registry = "https://github.com/rust-lang/crates.io-index"
replace-with = 'ustc'
[source.ustc]
registry = "http://mirrors.ustc.edu.cn/crates.io-index"
```

安装好diesel-cli

```rust
$ cargo install diesel_cli --no-default-features --features postgres
```


