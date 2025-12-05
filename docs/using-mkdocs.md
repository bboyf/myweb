
# 使用 MkDocs 和 Material for MkDocs 创建一个博客或文档网站
## 第一步：安装 MkDocs 和 Material for MkDocs
  1. 安装 MkDocs
  使用 pip 安装 MkDocs：
  ```bash
  pip install mkdocs
  ```
  2. 安装 Material for MkDocs 主题
  ```bash
  pip install mkdocs-material
  ```
## 第二步：创建一个新项目
  1. 创建项目目录,进入项目
  ```bash
  mkdir myweb
  cd myweb
  ```
  2. 项目结构
  ```perl
  myweb/
  ├── docs/
  │   └── index.md
  └── mkdocs.yml
  ```
- docs/ 文件夹用于存放文档内容。
- mkdocs.yml 是项目的配置文件，包含主题、导航等设置。

## 第三步：修改 mkdocs.yml 配置文件
1. 打开 mkdocs.yml 配置文件，修改配置以启用 Material 主题：
```yaml
site_name: My Blog
theme:
  name: material
  site_url: https://github.com/your_username/myweb.git
```

## 第四步：编辑文档内容
1. 在 docs/ 文件夹中，编辑 index.md 文件：
```markdown
# Welcome to My Blog

这是我用 MkDocs 和 Material for MkDocs 创建的第一个博客。

## 我的第一篇文章

这里是一些内容
```
2. 你可以继续在 docs/ 文件夹中添加其他 .md 文件，扩展文档内容。

## 第五步：运行本地开发服务器
1.  启动本地开发服务器：
```bash
mkdocs serve
```
2.  访问 http://localhost:8000 即可查看你的博客。

## 第六步：构建静态网站
1.  构建静态网站：
```bash
mkdocs build
```
2.  构建后的静态网站将位于 site/ 文件夹中。

## 第七步：部署到 GitHub Pages
1.  将 site/ 文件夹中的内容部署到你的网站服务器上。
2.  你可以使用 GitHub Pages、Netlify、Vercel 等服务来部署你的网站。

### 步骤 1：创建 GitHub 仓库
1. 登录 GitHub 并点击右上角的 "+" 按钮，选择 New repository 创建一个新仓库。

2. 选择一个仓库名（例如 my-blog），并点击创建。

### 步骤 2：将本地项目推送到 GitHub
1. 在本地项目文件夹中初始化 Git 仓库
```bash
  git init
  ```
2. 添加远程仓库
```bash
  git remote add origin https://github.com/your_username/myweb.git
  ```
3. 添加文件到暂存区
```bash
  git add .
  ```
4. 提交文件
```bash
  git commit -m "Initial commit"
  ```
5. 推送到 GitHub
```bash
  git push -u origin master
  ```
### 步骤 3：使用 mkdocs gh-deploy 部署到 GitHub Pages
1. 安装 GitHub Pages 插件（如果尚未安装）：
```bash
pip install mkdocs-git-committers
```
2. 部署到 GitHub Pages
```bash
mkdocs gh-deploy
```
3. 访问 https://your_username.github.io/myweb 即可查看你的博客。



## 更新文档内容并重新部署
1. 修改文档：编辑 index.md 或其他文档文件
2. 提交修改：
```bash
git add .
git commit -m "Update index.md"
git push origin master  # 或者是 main 分支
```
3. 重新部署到 GitHub Pages
```bash
mkdocs gh-deploy
```
4. GitHub Pages 更新：GitHub Pages 会自动更新你的网站内容。
