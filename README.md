# 2025 Hong Kong Forum on Neutron Scattering — 静态网页

这个目录包含会议的静态网页（`index.html` 及相关样式/图片引用）。下面是把这个网站部署到 GitHub Pages 的简要说明。

两种常用部署方式（任选其一）：

1) 使用仓库根目录直接托管（推荐用于个人用户页面）
   - 新建一个 GitHub 仓库，仓库名如果为 `USERNAME.github.io`，GitHub Pages 会把仓库根目录作为网站根。
   - 将本目录下的文件移动或复制到仓库根，然后 push 到 `main`（或 `master`）分支即可。

2) 使用本仓库并通过 GitHub Actions 自动部署（当前仓库已包含示例 workflow）
   - 我已添加一个 Actions workflow，会把仓库内的 `./网页` 目录内容发布到 `gh-pages` 分支。
   - 工作流程触发条件：每次 push 到 `main` 分支时自动运行。
   - 发布后你的网站 URL 通常为 `https://<USERNAME>.github.io/<REPO>/`（如果你使用的是项目页面）。

快速命令（在 `网页` 目录或上级目录执行，替换 `<USERNAME>` 和 `<REPO>`）：

```bash
# 在本地初始化并推送到新仓库（若尚未有 repo）
git init
git add .
git commit -m "Initial commit: add conference webpage"
# 创建远程仓库（手工在 GitHub 上创建或使用 gh CLI: gh repo create <USERNAME>/<REPO> --public --source=. --remote=origin --push）
git remote add origin https://github.com/<USERNAME>/<REPO>.git
git branch -M main
git push -u origin main
```

部署后检查：在 Actions 页或仓库 Settings -> Pages 中确认 `gh-pages` 分支是否为 Pages 的发布源，以及访问 `https://<USERNAME>.github.io/<REPO>/`。

如果你希望我继续：
- 我可以帮你生成仓库并把代码推上去（需要你在本机授权我或使用 GitHub CLI/提供 PAT）。
- 或者我可以把网站重定位到仓库根（把 `index.html` 移出 `网页` 目录），以便直接作为用户/组织页面。

需要我继续执行哪一步？
