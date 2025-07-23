# anki-sync-server-docker
anki-sync-server的docker镜像构建仓库，每天定时判断是否有版本更新

如何使用

- Docker Hub

```shell
docker run -d \
    -e "SYNC_USER1=admin:admin" \
    -p 8080:8080 \
    --mount type=volume,src=anki-sync-server-data,dst=/anki_data \
    --name anki-sync-server \
    xuanyue1024/anki-sync-server
```

- 阿里云镜像

```shell
docker run -d \
    -e "SYNC_USER1=admin:admin" \
    -p 8080:8080 \
    --mount type=volume,src=anki-sync-server-data,dst=/anki_data \
    --name anki-sync-server \
    crpi-9ovxnbm4ma0mwo5y.cn-chengdu.personal.cr.aliyuncs.com/xuanyue1024/anki-sync-server
```

每天自动构建时间：

- 中国标准时间：04:00
- 20:00 UTC

Docker Hub:[https://hub.docker.com/r/xuanyue1024/anki-sync-server/tags](https://hub.docker.com/r/xuanyue1024/anki-sync-server/tags)

官方anki发行版：[https://github.com/ankitects/anki/releases](https://github.com/ankitects/anki/releases)
