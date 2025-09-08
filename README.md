# 网盘搜索API

### 使用Docker部署


#### **前后端集成版**

##### 直接使用Docker命令

一键启动，开箱即用，无需任何配置

```
docker run -d --name pansou -p 80:80 ghcr.io/livecityccz/pansou-web
```

##### 使用Docker Compose（推荐）
```
# 下载配置文件
curl -o docker-compose.yml https://raw.githubusercontent.com/livecityccz/LinkVault/refs/heads/main/docker-compose.yml

# 启动服务
docker-compose up -d

# 查看日志
docker-compose logs -f
```

#### **纯后端API**

##### 直接使用Docker命令

```bash
docker run -d --name pansou -p 8888:8888 -v pansou-cache:/app/cache -e CHANNELS="tgsearchers3,xxx" ghcr.io/livecityccz/pansou:latest
```

##### 使用Docker Compose（推荐）

```bash
# 下载配置文件
curl -o docker-compose.yml  https://raw.githubusercontent.com/livecityccz/LinkVault/refs/heads/main/docker-compose.yml

# 启动服务
docker-compose up -d

# 访问服务
http://localhost:8888
```
