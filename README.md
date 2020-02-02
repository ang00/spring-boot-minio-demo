# spring-boot-minio-demo

- 安装 `minio`[文档](https://docs.min.io/cn/)
 - [下载](https://min.io/download) [文档](https://docs.min.io/cn/minio-server-configuration-guide.html)
 - docker 安装
   - 拉取
   
   ```docker pull minio/minio```
   
   - 运行
```shell script
docker run -p 9000:9000 --name minio \
-d --restart=always \
-e "MINIO_ACCESS_KEY=admin" \
-e "MINIO_SECRET_KEY=admin123456" \
-v ~/data/minio/data:/data \
-v ~/data/minio/config:/root/.minio \
minio/minio server /data
```
  - `docker-complse.yml` [下载](https://raw.githubusercontent.com/minio/minio/master/docs/orchestration/docker-compose/docker-compose.yaml)
```shell script
wget https://raw.githubusercontent.com/minio/minio/master/docs/orchestration/docker-compose/docker-compose.yaml
```
  - 运行 `docker-compose up`
- import pageage sdk

```shell
<dependency>
    <groupId>com.jlefebure</groupId>
    <artifactId>spring-boot-starter-minio</artifactId>
    <version>1.3</version>
</dependency>
```
