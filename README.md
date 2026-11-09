# officebuddy-docs

OfficeBuddy 产品文档，基于 [Mintlify](https://mintlify.com) 托管。

## 本地预览

```bash
# 安装 Mintlify CLI（需要 Node 18+）
npm i -g mintlify

# 在仓库根目录启动预览（4321 端口）
mintlify dev
```

## 目录结构

```
docs.json                # Mintlify 配置：导航、主题色、页脚（站点的"大脑"）
index.mdx                # 文档首页（Hero + 卡片入口）
getting-started/         # 安装、快速上手
product/                 # 产品功能页
faq.mdx                  # 常见问题
images/                  # 图片资源
```

## 部署上线

1. 把本仓库推到 GitHub
2. 打开 [dashboard.mintlify.com](https://dashboard.mintlify.com)，用 GitHub 登录
3. 「Add deployment / Import repository」选择本仓库 → 自动构建部署
4. 绑定自定义域名（如 `docs.你的域名.com`），DNS 加一条 CNAME 指向 Mintlify 分配的地址

之后每次 `git push` 自动重新部署。

## 写作约定

- 每页一个主题，页面尽量短（参考 docs.astravia.dev 的分步式结构）
- 操作步骤用 `<Steps>`，提示用 `<Note>` / `<Warning>`
- 导航变更只改 `docs.json`，页面文件名即 URL
