# Databases Docker镜像环境
    MySQL-5.7 Redis-latest Memcached-latest

### 运行步骤
###### 1、克隆项目
    git clone https://github.com/jun3372/php-docker.git

###### 2、拷贝配置文件
    cp env-example .env

###### 3、启动项目
    docker-composer.exe up -d

### 启动所有环境
    docker-composer.exe up -d

### 启动指定镜像
    docker-composer.exe up -d {package name}

### 目录说明
    project                     docker克隆目录
    ├─app                       网站项目目录
    |   |-default               默认网站目录
    │   └─ ...                  更多虚拟机目录
    |-data                      数据存储目录
    |   |-mysql                 mysql数据目录
    |   |-redis                 redis数据目录
    |-nginx                     Nginx配置目录
    |   |-vhost                 虚拟机配置目录
    |   |   |-test.conf         测试虚拟机配置
    │   │   └─ ...              更多虚拟机配置
    |   |-logs                  日志存放目录
    |   |   |-nginx             nginx日志目录
    │   │   |   |- access.log   nginx成功日志
    │   │   |   └─ error.log    nginx失败日志
