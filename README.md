# WeCom ↔ Open WebUI 网关（支持文本与生图）

> 通过 **企业微信·微信客服** 与 **Open WebUI** 双向打通：在微信里轻量对话，在 WebUI 中完整保留会话上下文与标题，支持图片输入与模型出图。

## ✨ 特性

- 一处对话、两处可见（微信 ↔ Open WebUI）
- 标题自动生成（沿用 WebUI 原生）
- 图片：先图后文自动合并入模；模型出图自动压缩上传后下发
- 速率限制与重试：命中 95001 自动入队 + 指数回退
- 无前端侵入：遵循 Open WebUI 的后端受控、UI 兼容流程
- 与企业微信有关的相关参数请前往企业微信-微信客服后台获取

## 📦 目录结构

```
.
├─ app.py
├─ docker-compose.yml
└─ .env.wecom
```

## 🚀 快速开始（Docker Compose）

```bash
docker compose up -d
```

默认端口映射：见 docker-compose.yml

## 🔧 环境变量


## 调试接口
- GET /healthz
- GET /debug/ping-openwebui
- GET /debug/state?ext_uid=OPENID
- GET /debug/ratelimit

## 效果
<img width="1134" height="844" alt="image" src="https://github.com/user-attachments/assets/2cb4147e-fb13-4dc0-8a7d-7c93a905d746" />
<img width="1798" height="1244" alt="image" src="https://github.com/user-attachments/assets/2a92129f-7906-488e-9bee-208e44cf0fab" />


