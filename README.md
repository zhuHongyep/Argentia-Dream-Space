# Argentia Dream Space

基于 MkDocs 的中文个人网站，包含首页、文章、项目和关于页面。

## 本地预览（PowerShell）

在项目目录依次运行：

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs serve
```

在浏览器中访问 http://127.0.0.1:8000 。修改 Markdown 后会自动刷新。

构建检查：

```powershell
.\.venv\Scripts\python.exe -m mkdocs build --strict
```

## 个性化

- `mkdocs.yml`：网站标题、简介、导航与主题。
- `docs/index.md`：首页。
- `docs/posts/`：文章；新增文章后，在目录页和 `mkdocs.yml` 中添加链接。
- `docs/projects.md`：项目展示。
- `docs/about.md`：个人介绍与公开联系方式。
- `docs/stylesheets/extra.css`：颜色与排版。

目前个人介绍和部分内容为示例，请在发布前替换。
已配置仓库 `https://github.com/zhuHongyep/Argentia-Dream-Space`，预期网站地址为 `https://zhuhongyep.github.io/Argentia-Dream-Space/`。

## 发布到 GitHub Pages

1. 在 GitHub 创建公开仓库。若希望网址为 `https://你的用户名.github.io/`，仓库名使用 `你的用户名.github.io`（用户名小写）；普通仓库的网址为 `https://你的用户名.github.io/仓库名/`。
2. 将本目录的源码推送到仓库的 `main` 分支，确保包含 `.github/workflows/deploy.yml`。
3. 打开仓库 **Settings → Pages → Build and deployment → Source**，选择 **GitHub Actions**。
4. 打开 **Actions → 发布个人网站 → Run workflow**，或向 `main` 推送修改以触发发布。
5. 工作流成功后，在 **Settings → Pages** 中查看网站地址。

工作流通过 GitHub 自动提供的权限发布，无需手动填写访问令牌。若仓库实际使用其他默认分支，请相应修改工作流中的 `branches`。

后续只需修改 Markdown 并推送，网站便会自动重新构建和发布。

## 官方参考

- [MkDocs 入门](https://www.mkdocs.org/getting-started/)
- [GitHub Pages 建站说明](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
