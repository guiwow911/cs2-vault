# CS2 Vault

一个纯静态、单文件的 CS2 开箱演示站，适合直接部署到 GitHub Pages。

## 功能与限制

- 网站数据仅保存在访问者当前浏览器的 `localStorage` 中。
- 登录、开发者模式和用户封禁均为前端演示功能，不是真实的服务端账号或管理系统。
- 开发者演示账号为 `1` / `1`，不能用于真实生产环境。
- 网站不连接 Steam、支付服务或任何外部 API。

## GitHub Pages 部署

本项目已包含 `.github/workflows/deploy-pages.yml`。推送到 GitHub 后：

1. 打开仓库的 **Settings → Pages**。
2. 将 **Build and deployment → Source** 设置为 **GitHub Actions**。
3. 打开 **Actions**，等待 `Deploy static site to GitHub Pages` 成功。
4. 网站地址通常为 `https://<GitHub用户名>.github.io/<仓库名>/`。

### 首次推送

在项目目录运行：

```bash
git init
git add .
git commit -m "Deploy CS2 Vault to GitHub Pages"
git branch -M main
git remote add origin https://github.com/<GitHub用户名>/<仓库名>.git
git push -u origin main
```

推送时请使用 GitHub 的浏览器登录、SSH 密钥或 Personal Access Token；不要把令牌写入项目文件。
