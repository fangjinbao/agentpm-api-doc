# AgentPM API 文档

基于 [Mintlify](https://mintlify.com) 搭建的 AgentPM API 文档站点。

## 本地开发

需要 Node.js v20.17 及以上版本。

```bash
npm install
npm run dev
```

打开 http://localhost:3000 实时预览，修改文件后页面会自动刷新。

| 命令 | 说明 |
| --- | --- |
| `npm run dev` | 启动本地预览 |
| `npm run broken-links` | 检查失效链接 |

## 项目结构

```
.
├── docs.json                 # 站点配置：导航、主题色、Logo 等
├── index.mdx                 # 首页
├── claude/                   # Claude 模型：安装、配置、使用
├── gpt/                      # GPT（Codex）模型：安装、配置、使用
├── ide/                      # Trae、Cursor 模型配置
├── images/                   # 文档截图
├── logo/                     # 亮色 / 暗色 Logo
└── favicon.svg               # 站点图标
```

## 编写文档

- **新增页面**：创建 `.mdx` 文件，然后把路径（不带扩展名）加到 `docs.json` 的 `navigation` 中
- **页面头部**：每个页面以 frontmatter 开头

  ```mdx
  ---
  title: "页面标题"
  description: "页面描述"
  ---
  ```

- **组件**：可用组件参见 [Mintlify 组件文档](https://mintlify.com/docs/components)

## 部署

推送到 GitHub 后，在 [mintlify.com/start](https://mintlify.com/start) 连接仓库，之后每次推送到默认分支都会自动部署。
