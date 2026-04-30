# ai-chat-hub

AI Chat Hub - 一个基于 Vue3 + Vite 构建的 AI 聊天应用。

## 📖 简介

这是一个纯前端静态页面应用，通过 OpenRouter API 进行对话。

## 🚀 部署方式

本项目使用 GitHub Actions 自动部署到 GitHub Pages。

### 自动部署流程

1. **触发条件**：
   - 推送到 `main` 分支时自动触发部署
   - 或者在 GitHub Actions 页面手动触发（workflow_dispatch）

2. **部署步骤**：
   - GitHub Actions 会自动检出代码
   - 上传 `html/` 目录作为静态站点内容
   - 自动部署到 GitHub Pages

3. **访问地址**：
   ```
   https://<你的GitHub用户名>.github.io/ai-chat-hub/
   ```

### 首次配置 GitHub Pages

如果是第一次部署，需要在 GitHub 仓库中进行以下设置：

1. 进入仓库的 **Settings** → **Pages**
2. 在 **Build and deployment** 部分：
   - **Source**: 选择 "GitHub Actions"
3. 保存设置

## 📁 项目结构

```
ai-chat-hub/
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions 部署配置
├── html/                    # 构建好的静态页面（直接部署）
│   ├── assets/             # 静态资源文件
│   └── index.html          # 入口文件
└── README.md               # 项目说明文档
```

## 🔧 本地开发

如果你需要修改和重新构建项目：

1. 确保你已经安装了 Node.js 和 npm
2. 在项目根目录运行：
   ```bash
   # 安装依赖（如果需要）
   npm install
   
   # 本地开发服务器
   npm run dev
   
   # 构建生产版本到 html/ 目录
   npm run build
   ```

3. 将构建后的 `html/` 目录提交到 Git，推送后会自动部署

## 📝 技术栈

- **前端框架**: Vue3 + Vite
- **API 集成**: OpenRouter API
- **部署平台**: GitHub Pages
- **CI/CD**: GitHub Actions

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License