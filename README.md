1. 克隆当前仓库
2. 在本地目录下创建 .env.litellm 环境变量文件
3. 在环境变量配置文件中配置密钥，对应的是 config.yaml 中的每一个环境变量。
4. 使用 docker 创建一个容器。详情请看 docker-compose.yml

我的 .env.litellm 文件内容如下：
```aiignore
# 在这里填入你的 API Keys，这里的环境变量，淫荡与 confi.yaml 中的设置，一一对应
OPENAI_API_KEY=xxxx
Deepseek_API_KEY=xxxx
GOOGLE_API_KEY=xxxx

# 下面是代理设置，前面的 host 部分之所以这么写，是因为用 docker-compose 启动了，要用这个 host 才能在容器内访问宿主机的端口
HTTP_PROXY=http://host.docker.internal:12334
HTTPS_PROXY=http://host.docker.internal:12334
```
