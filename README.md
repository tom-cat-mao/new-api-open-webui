<div align="center">

![new-api](/web/public/logo.png)

# New API

🍥 **新一代大模型网关与AI资产管理系统**

<p align="center">
  <strong>中文</strong> | 
  <a href="./README.en.md">English</a> | 
  <a href="./README.fr.md">Français</a> | 
  <a href="./README.ja.md">日本語</a>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/Calcium-Ion/new-api/main/LICENSE">
    <img src="https://img.shields.io/github/license/Calcium-Ion/new-api?color=brightgreen" alt="license">
  </a>
  <a href="https://github.com/Calcium-Ion/new-api/releases/latest">
    <img src="https://img.shields.io/github/v/release/Calcium-Ion/new-api?color=brightgreen&include_prereleases" alt="release">
  </a>
  <a href="https://github.com/users/Calcium-Ion/packages/container/package/new-api">
    <img src="https://img.shields.io/badge/docker-ghcr.io-blue" alt="docker">
  </a>
  <a href="https://hub.docker.com/r/CalciumIon/new-api">
    <img src="https://img.shields.io/badge/docker-dockerHub-blue" alt="docker">
  </a>
  <a href="https://goreportcard.com/report/github.com/Calcium-Ion/new-api">
    <img src="https://goreportcard.com/badge/github.com/Calcium-Ion/new-api" alt="GoReportCard">
  </a>
</p>

<p align="center">
  <a href="https://trendshift.io/repositories/8227" target="_blank">
    <img src="https://trendshift.io/api/badge/repositories/8227" alt="Calcium-Ion%2Fnew-api | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/>
  </a>
</p>

<p align="center">
  <a href="#-快速开始">快速开始</a> •
  <a href="#-主要特性">主要特性</a> •
  <a href="#-部署">部署</a> •
  <a href="#-文档">文档</a> •
  <a href="#-帮助支持">帮助</a>
</p>

</div>

## 📝 项目说明

> [!NOTE]
> 本项目为开源项目，在 [One API](https://github.com/songquanpeng/one-api) 的基础上进行二次开发

> [!IMPORTANT]
> - 本项目仅供个人学习使用，不保证稳定性，且不提供任何技术支持
> - 使用者必须在遵循 OpenAI 的 [使用条款](https://openai.com/policies/terms-of-use) 以及**法律法规**的情况下使用，不得用于非法用途
> - 根据 [《生成式人工智能服务管理暂行办法》](http://www.cac.gov.cn/2023-07/13/c_1690898327029107.htm) 的要求，请勿对中国地区公众提供一切未经备案的生成式人工智能服务

### 🎯 Open-WebUI 集成特性

新版 New API 现已深度集成 [Open-WebUI](https://github.com/open-webui/open-webui)，提供完整的 AI 应用解决方案：

#### ✨ 集成优势
- **开箱即用**：Docker Compose 一键部署，自动配置服务间的连接
- **统一管理**：New API 负责后端 API 管理，Open-WebUI 提供前端对话界面
- **多模型支持**：通过 New API 统一接口，支持 OpenAI、Claude、Gemini 等主流模型
- **安全隔离**：服务间通过 Docker 网络安全通信，仅暴露必要端口

#### 🏗️ 架构说明
```
用户访问
    ↓
Open-WebUI (localhost:8000) - 提供类 ChatGPT 界面
    ↓
New-API (localhost:3000) - API 网关和管理系统
    ↓
各种 AI 服务提供商 (OpenAI/Claude/Gemini 等)
```

#### 🚀 部署体验
- **一体化部署**：一个命令启动完整 AI 应用栈
- **数据持久化**：配置和对话数据自动保存
- **灵活扩展**：可根据需求独立升级或替换组件

---

## 🤝 我们信任的合作伙伴

<p align="center">
  <em>排名不分先后</em>
</p>

<p align="center">
  <a href="https://www.cherry-ai.com/" target="_blank">
    <img src="./docs/images/cherry-studio.png" alt="Cherry Studio" height="80" />
  </a>
  <a href="https://bda.pku.edu.cn/" target="_blank">
    <img src="./docs/images/pku.png" alt="北京大学" height="80" />
  </a>
  <a href="https://www.compshare.cn/?ytag=GPU_yy_gh_newapi" target="_blank">
    <img src="./docs/images/ucloud.png" alt="UCloud 优刻得" height="80" />
  </a>
  <a href="https://www.aliyun.com/" target="_blank">
    <img src="./docs/images/aliyun.png" alt="阿里云" height="80" />
  </a>
  <a href="https://io.net/" target="_blank">
    <img src="./docs/images/io-net.png" alt="IO.NET" height="80" />
  </a>
</p>

---

## 🙏 特别鸣谢

<p align="center">
  <a href="https://www.jetbrains.com/?from=new-api" target="_blank">
    <img src="https://resources.jetbrains.com/storage/products/company/brand/logos/jb_beam.png" alt="JetBrains Logo" width="120" />
  </a>
</p>

<p align="center">
  <strong>感谢 <a href="https://www.jetbrains.com/?from=new-api">JetBrains</a> 为本项目提供免费的开源开发许可证</strong>
</p>

---

## 🚀 快速开始

### 使用 Docker Compose（推荐）

```bash
# 克隆项目
git clone https://github.com/QuantumNous/new-api.git
cd new-api

# 编辑 docker-compose.yml 配置（已包含 New-API、Open-WebUI 和 Watchtower 自动更新）
nano docker-compose.yml

# 启动服务（包含 New-API、Open-WebUI 和 Watchtower 自动更新）
docker-compose up -d

# 查看 Watchtower 自动更新日志
docker logs watchtower -f
```

#### 🔧 服务说明

Docker Compose 配置包含以下服务：

- **New-API**（端口 3000）：主要的 API 网关服务
- **Open-WebUI**（端口 8000）：Web 界面服务
- **PostgreSQL**：数据库服务
- **Redis**：缓存服务
- **Watchtower**：自动更新服务

#### 🔄 自动更新功能（Watchtower）

项目集成了 Watchtower 服务，提供以下功能：

- **自动监控**：每 12 小时检查一次新镜像版本
- **自动更新**：发现新版本时自动下载并重启容器
- **清理旧镜像**：更新后自动清理旧版本镜像节省空间
- **服务管理**：仅更新正在运行的容器，忽略已停止的容器

如需禁用自动更新，可在 `docker-compose.yml` 中注释掉 watchtower 服务部分。

<details>
<summary><strong>使用 Docker 命令</strong></summary>

```bash
# 拉取最新镜像
docker pull calciumion/new-api:latest

# 使用 SQLite（默认）
docker run --name new-api -d --restart always \
  -p 3000:3000 \
  -e TZ=Asia/Shanghai \
  -v ./data:/data \
  calciumion/new-api:latest

# 使用 MySQL
docker run --name new-api -d --restart always \
  -p 3000:3000 \
  -e SQL_DSN="root:123456@tcp(localhost:3306)/oneapi" \
  -e TZ=Asia/Shanghai \
  -v ./data:/data \
  calciumion/new-api:latest
```

> **💡 提示：** `-v ./data:/data` 会将数据保存在当前目录的 `data` 文件夹中，你也可以改为绝对路径如 `-v /your/custom/path:/data`

</details>

---

🎉 部署完成后：
- **New-API 管理界面**：访问 `http://localhost:3000` 进行 API 配置和管理
- **Open-WebUI 聊天界面**：访问 `http://localhost:8000` 进行 AI 对话

💡 **Open-WebUI 集成说明**：
- 新版 docker-compose.yml 已集成 Open-WebUI 服务
- Open-WebUI 会自动连接到 New-API 作为后端服务
- 无需额外配置，开箱即用，提供类似 ChatGPT 的对话界面

📖 更多部署方式请参考 [部署指南](https://docs.newapi.pro/installation)

---

## 📚 文档

<div align="center">

### 📖 [官方文档](https://docs.newapi.pro/) | [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/QuantumNous/new-api)

</div>

**快速导航：**

| 分类 | 链接 |
|------|------|
| 🚀 部署指南 | [安装文档](https://docs.newapi.pro/installation) |
| ⚙️ 环境配置 | [环境变量](https://docs.newapi.pro/installation/environment-variables) |
| 📡 接口文档 | [API 文档](https://docs.newapi.pro/api) |
| ❓ 常见问题 | [FAQ](https://docs.newapi.pro/support/faq) |
| 💬 社区交流 | [交流渠道](https://docs.newapi.pro/support/community-interaction) |

---

## ✨ 主要特性

> 详细特性请参考 [特性说明](https://docs.newapi.pro/wiki/features-introduction)

### 🎨 核心功能

| 特性 | 说明 |
|------|------|
| 🎨 全新 UI | 现代化的用户界面设计 |
| 🌍 多语言 | 支持中文、英文、法语、日语 |
| 🔄 数据兼容 | 完全兼容原版 One API 数据库 |
| 📈 数据看板 | 可视化控制台与统计分析 |
| 🔒 权限管理 | 令牌分组、模型限制、用户管理 |

### 💰 支付与计费

- ✅ 在线充值（易支付、Stripe）
- ✅ 模型按次数收费
- ✅ 缓存计费支持（OpenAI、Azure、DeepSeek、Claude、Qwen等所有支持的模型）
- ✅ 灵活的计费策略配置

### 🔐 授权与安全

- 🤖 LinuxDO 授权登录
- 📱 Telegram 授权登录
- 🔑 OIDC 统一认证
- 🔍 Key 查询使用额度（配合 [neko-api-key-tool](https://github.com/Calcium-Ion/neko-api-key-tool)）

### 🚀 高级功能

**API 格式支持：**
- ⚡ [OpenAI Responses](https://docs.newapi.pro/api/openai-responses)
- ⚡ [OpenAI Realtime API](https://docs.newapi.pro/api/openai-realtime)（含 Azure）
- ⚡ [Claude Messages](https://docs.newapi.pro/api/anthropic-chat)
- ⚡ [Google Gemini](https://docs.newapi.pro/api/google-gemini-chat/)
- 🔄 [Rerank 模型](https://docs.newapi.pro/api/jinaai-rerank)（Cohere、Jina）

**智能路由：**
- ⚖️ 渠道加权随机
- 🔄 失败自动重试
- 🚦 用户级别模型限流

**格式转换：**
- 🔄 OpenAI ⇄ Claude Messages
- 🔄 OpenAI ⇄ Gemini Chat
- 🔄 思考转内容功能

**Reasoning Effort 支持：**

<details>
<summary>查看详细配置</summary>

**OpenAI 系列模型：**
- `o3-mini-high` - High reasoning effort
- `o3-mini-medium` - Medium reasoning effort
- `o3-mini-low` - Low reasoning effort
- `gpt-5-high` - High reasoning effort
- `gpt-5-medium` - Medium reasoning effort
- `gpt-5-low` - Low reasoning effort

**Claude 思考模型：**
- `claude-3-7-sonnet-20250219-thinking` - 启用思考模式

**Google Gemini 系列模型：**
- `gemini-2.5-flash-thinking` - 启用思考模式
- `gemini-2.5-flash-nothinking` - 禁用思考模式
- `gemini-2.5-pro-thinking` - 启用思考模式
- `gemini-2.5-pro-thinking-128` - 启用思考模式，并设置思考预算为128tokens

</details>

---

## 🤖 模型支持

> 详情请参考 [接口文档 - 中继接口](https://docs.newapi.pro/api)

| 模型类型 | 说明 | 文档 |
|---------|------|------|
| 🤖 OpenAI GPTs | gpt-4-gizmo-* 系列 | - |
| 🎨 Midjourney-Proxy | [Midjourney-Proxy(Plus)](https://github.com/novicezk/midjourney-proxy) | [文档](https://docs.newapi.pro/api/midjourney-proxy-image) |
| 🎵 Suno-API | [Suno API](https://github.com/Suno-API/Suno-API) | [文档](https://docs.newapi.pro/api/suno-music) |
| 🔄 Rerank | Cohere、Jina | [文档](https://docs.newapi.pro/api/jinaai-rerank) |
| 💬 Claude | Messages 格式 | [文档](https://docs.newapi.pro/api/anthropic-chat) |
| 🌐 Gemini | Google Gemini 格式 | [文档](https://docs.newapi.pro/api/google-gemini-chat/) |
| 🔧 Dify | ChatFlow 模式 | - |
| 🎯 自定义 | 支持完整调用地址 | - |

### 📡 支持的接口

<details>
<summary>查看完整接口列表</summary>

- [聊天接口 (Chat Completions)](https://docs.newapi.pro/api/openai-chat)
- [响应接口 (Responses)](https://docs.newapi.pro/api/openai-responses)
- [图像接口 (Image)](https://docs.newapi.pro/api/openai-image)
- [音频接口 (Audio)](https://docs.newapi.pro/api/openai-audio)
- [视频接口 (Video)](https://docs.newapi.pro/api/openai-video)
- [嵌入接口 (Embeddings)](https://docs.newapi.pro/api/openai-embeddings)
- [重排序接口 (Rerank)](https://docs.newapi.pro/api/jinaai-rerank)
- [实时对话 (Realtime)](https://docs.newapi.pro/api/openai-realtime)
- [Claude 聊天](https://docs.newapi.pro/api/anthropic-chat)
- [Google Gemini 聊天](https://docs.newapi.pro/api/google-gemini-chat)

</details>

---

## 🚢 部署

> [!TIP]
> **最新版 Docker 镜像：** `calciumion/new-api:latest`

### 📋 部署要求

| 组件 | 要求 |
|------|------|
| **本地数据库** | SQLite（Docker 需挂载 `/data` 目录）|
| **远程数据库** | MySQL ≥ 5.7.8 或 PostgreSQL ≥ 9.6 |
| **容器引擎** | Docker / Docker Compose |

### ⚙️ 环境变量配置

<details>
<summary>常用环境变量配置</summary>

| 变量名 | 说明 | 默认值 |
|--------|------|--------|
| `SESSION_SECRET` | 会话密钥（多机部署必须） | - |
| `CRYPTO_SECRET` | 加密密钥（Redis 必须） | - |
| `SQL_DSN` | 数据库连接字符串 | - |
| `REDIS_CONN_STRING` | Redis 连接字符串 | - |
| `STREAMING_TIMEOUT` | 流式超时时间（秒） | `300` |
| `AZURE_DEFAULT_API_VERSION` | Azure API 版本 | `2025-04-01-preview` |
| `ERROR_LOG_ENABLED` | 错误日志开关 | `false` |

📖 **完整配置：** [环境变量文档](https://docs.newapi.pro/installation/environment-variables)

</details>

### 🔧 部署方式

<details>
<summary><strong>方式 1：Docker Compose（推荐）</strong></summary>

```bash
# 克隆项目
git clone https://github.com/QuantumNous/new-api.git
cd new-api

# 编辑配置（包含 New-API、Open-WebUI 和 Watchtower 服务）
nano docker-compose.yml

# 启动服务（New-API + Open-WebUI + Redis + PostgreSQL + Watchtower）
docker-compose up -d

# 监控自动更新日志
docker logs watchtower -f
```

**服务说明：**
- **New-API**：运行在端口 3000，提供 API 管理界面
- **Open-WebUI**：运行在端口 8000，提供 Web 聊天界面
- **Redis**：缓存服务
- **PostgreSQL**：数据库服务（可选 MySQL）
- **Watchtower**：自动更新服务，每 12 小时检查并更新容器镜像

**访问地址：**
- 管理界面：`http://localhost:3000`
- 聊天界面：`http://localhost:8000`

**Watchtower 管理：**
- 查看更新日志：`docker logs watchtower`
- 手动触发更新：`docker-compose restart watchtower`
- 禁用自动更新：在 `docker-compose.yml` 中注释 watchtower 服务

</details>

<details>
<summary><strong>方式 2：仅 Docker 部署 New-API</strong></summary>

**使用 SQLite：**
```bash
docker run --name new-api -d --restart always \
  -p 3000:3000 \
  -e TZ=Asia/Shanghai \
  -v ./data:/data \
  calciumion/new-api:latest
```

**使用 MySQL：**
```bash
docker run --name new-api -d --restart always \
  -p 3000:3000 \
  -e SQL_DSN="root:123456@tcp(localhost:3306)/oneapi" \
  -e TZ=Asia/Shanghai \
  -v ./data:/data \
  calciumion/new-api:latest
```

💡 **提示**：此方式仅部署 New-API 服务，如需 Open-WebUI 界面，请使用 Docker Compose 方式

> **💡 路径说明：**
> - `./data:/data` - 相对路径，数据保存在当前目录的 data 文件夹
> - 也可使用绝对路径，如：`/your/custom/path:/data`

</details>

<details>
<summary><strong>方式 3：宝塔面板</strong></summary>

1. 安装宝塔面板（≥ 9.2.0 版本）
2. 在应用商店搜索 **New-API**
3. 一键安装

📖 [图文教程](./docs/BT.md)

</details>

### ⚠️ 多机部署注意事项

> [!WARNING]
> - **必须设置** `SESSION_SECRET` - 否则登录状态不一致
> - **公用 Redis 必须设置** `CRYPTO_SECRET` - 否则数据无法解密

### 🔄 渠道重试与缓存

**重试配置：** `设置 → 运营设置 → 通用设置 → 失败重试次数`

**缓存配置：**
- `REDIS_CONN_STRING`：Redis 缓存（推荐）
- `MEMORY_CACHE_ENABLED`：内存缓存

---

## 🔗 相关项目

### 上游项目

| 项目 | 说明 |
|------|------|
| [One API](https://github.com/songquanpeng/one-api) | 原版项目基础 |
| [Midjourney-Proxy](https://github.com/novicezk/midjourney-proxy) | Midjourney 接口支持 |

### 配套工具

| 项目 | 说明 |
|------|------|
| [neko-api-key-tool](https://github.com/Calcium-Ion/neko-api-key-tool) | Key 额度查询工具 |
| [new-api-horizon](https://github.com/Calcium-Ion/new-api-horizon) | New API 高性能优化版 |

---

## 💬 帮助支持

### 📖 文档资源

| 资源 | 链接 |
|------|------|
| 📘 常见问题 | [FAQ](https://docs.newapi.pro/support/faq) |
| 💬 社区交流 | [交流渠道](https://docs.newapi.pro/support/community-interaction) |
| 🐛 反馈问题 | [问题反馈](https://docs.newapi.pro/support/feedback-issues) |
| 📚 完整文档 | [官方文档](https://docs.newapi.pro/support) |

### 🤝 贡献指南

欢迎各种形式的贡献！

- 🐛 报告 Bug
- 💡 提出新功能
- 📝 改进文档
- 🔧 提交代码

---

## 🌟 Star History

<div align="center">

[![Star History Chart](https://api.star-history.com/svg?repos=Calcium-Ion/new-api&type=Date)](https://star-history.com/#Calcium-Ion/new-api&Date)

</div>

---

<div align="center">

### 💖 感谢使用 New API

如果这个项目对你有帮助，欢迎给我们一个 ⭐️ Star！

**[官方文档](https://docs.newapi.pro/)** • **[问题反馈](https://github.com/Calcium-Ion/new-api/issues)** • **[最新发布](https://github.com/Calcium-Ion/new-api/releases)**

<sub>Built with ❤️ by QuantumNous</sub>

</div>
