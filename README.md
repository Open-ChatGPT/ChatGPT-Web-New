# ChatGPT Web New

- **源自项目仓库**: [Chanzhaoyu](https://github.com/Chanzhaoyu/chatgpt-web)
- **基于项目仓库**: [Kerwin1202](https://github.com/Kerwin1202/chatgpt-web)
- **项目预览Web**: [Ai.Bot-t.me](https://ai.bot-t.me)

## 仓库特色功能

- [ ] 使用 OAuth 实现登录功能
- [ ] 更新 UI 框架
- [ ] 添加 OpenAI ChatGPT 插件功能
- [x] 注册、登录及重置密码
- [x] 同步历史会话
- [x] 前端页面设置 API key
- [x] 自定义敏感词
- [x] 每个会话设置独有 Prompt
- [x] 用户管理
- [x] 多 Key 随机

## 安装与运行

### 前置要求

#### Node
确保您的 Node 版本满足 `^16 || ^18 || ^19` 的要求。

```bash
node -v
```

#### PNPM
如果你没有安装过 `pnpm`:

```bash
npm install pnpm -g
```

### 安装依赖

#### 后端
进入文件夹 `/service` 运行以下命令:

```bash
pnpm install
```

#### 前端
根目录下运行以下命令:

```bash
pnpm bootstrap
```

### 测试环境运行

#### 后端服务
进入文件夹 `/service` 运行以下命令:

```bash
pnpm start
```

#### 前端网页
根目录下运行以下命令:

```bash
pnpm dev
```

## 环境变量

详细的环境变量配置请查看[这里](#环境变量):

```bash
/service/.env.example
```
### 使用 Railway 部署 

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/XLQ1-1?referralCode=jtcX_T)

## 打包与部署

### 使用 Docker

#### Docker 参数示例

![Docker参数](./docs/docker.png)

#### Docker build & Run

```bash
docker build -t chatgpt-web .
# 前台运行
docker run --name chatgpt-web --rm -it -p 127.0.0.1:3002:3002 --env OPENAI_API_KEY=your_api_key chatgpt-web
# 后台运行
docker run --name chatgpt-web -d -p 127.0.0.1:3002:3002 --env OPENAI_API_KEY=your_api_key chatgpt-web
```

### 手动打包

#### 后端服务
复制 `service` 文件夹到你有 `node` 服务环境的服务器上。

```bash
# 安装
pnpm install
# 打包
pnpm build
# 运行
pnpm prod
```

#### 前端网页
1. 修改根目录下 `.env` 文件中的 `VITE_GLOB_API_URL` 为你的实际后端接口地址
2. 根目录下运行以下命令，然后将 `dist` 文件夹内的文件复制到你网站服务的根目录下

```bash
pnpm build
```

## 贡献

如果你想为此项目做出贡献，欢迎查看[贡献指南](./CONTRIBUTING.md)。

## 赞助

如果你觉得这个项目对你有帮助，请给我点个Star。并且情况允许的话，可以给我一点点支持，总之非常感谢支持～

## License
MIT © [Nb112211](./license)