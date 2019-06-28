## 命令格式：


```
docker run ubuntu:15.10 /bin/echo "Hello world"
```


- 讲解：
    - 1 ：docker: Docker 的二进制执行文件。
    - 2 ：run:与前面的 docker 组合来运行一个容器
    - 3 ：ubuntu:15.10指定要运行的镜像，Docker首先从本地主机上查找镜像是否存在，如果不存在，Docker 就会从镜像仓库 Docker Hub 下载公共镜像。
    - 4 /bin/echo "Hello world": 在启动的容器里执行的命令
--------------------------

## 常用命令

- docker stop 停止容器



- docker ps 查看

    · CONTAINER ID:容器ID
    
    · NAMES:自动分配的容器名称
    

- docker logs 查看容器内的标准输出



- docker pull training/webapp  # 载入镜像
- docker run
```
docker run -d -P training/webapp python app.py

docker run --name mysql5.7 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5.7

参数说明：
-d:让容器在后台运行。
-P:将容器内部使用的网络端口映射到我们使用的主机上。
```


- docker port 查看端口映射
-  docker top 来查看容器内部运行的进程
-  docker inspect 来查看 Docker 的底层信息
-  docker images 来列出本地主机上的镜像。
```
REPOSITORY：表示镜像的仓库源

TAG：镜像的标签

IMAGE ID：镜像ID

CREATED：镜像创建时间

SIZE：镜像大小
```

- docker tag 命令，为镜像添加一个新的标签


- docker exec 进入容器
```
docker exec -it 775c7c9ee1e1 /bin/bash 
参数说明 
775c7c9ee1e1 是容器id
```


- docker build 命令 构建镜像
```
docker build -t file-auto .
参数解释：
file-auto 构建出来的镜像名
. 当前文件夹下

```



---------------------

