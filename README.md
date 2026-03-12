# GitHub Pages Deployment Guide

## 📁 文件已准备好

所有 HTML 文件已复制到 `github-pages/` 目录：
- `index.html` - 主页（画廊风格，展示所有 slides）
- `genai-anxiety-slide-lv-premium.html` - AI 焦虑悖论（LV Premium）
- `openclaw-workflow-lv-premium.html` - OpenClaw 工作流（LV Premium）
- `genai-anxiety-slide.html` - 原始版本

---

## 🚀 部署步骤（5 分钟完成）

### 步骤 1：创建 GitHub 仓库

1. 登录 https://github.com
2. 点击右上角 **+** → **New repository**
3. 填写：
   - **Repository name:** `slides`（或 `presentations`）
   - **Description:** "Presentation slides - LV Premium Collection"
   - **Public**（必须公开才能用 GitHub Pages）
   - ✅ 勾选 **Add a README file**
4. 点击 **Create repository**

---

### 步骤 2：上传文件

**方法 A：网页上传（最简单）**

1. 在刚创建的 repo 页面，点击 **Add file** → **Upload files**
2. 把 `github-pages/` 文件夹里的所有 `.html` 文件拖进去
3. 填写 Commit message：`Add presentation slides`
4. 点击 **Commit changes**

**方法 B：Git 命令行**

```bash
cd C:\Users\flora.liu\.openclaw\workspace\github-pages

# 初始化 git
git init

# 添加所有文件
git add .

# 提交
git commit -m "Add presentation slides"

# 添加远程仓库（替换 YOUR_USERNAME 为你的 GitHub 用户名）
git remote add origin https://github.com/YOUR_USERNAME/slides.git

# 推送
git branch -M main
git push -u origin main
```

---

### 步骤 3：开启 GitHub Pages

1. 在 repo 页面，点击 **Settings**（顶部导航）
2. 左侧菜单找到 **Pages**
3. **Source** 选择：
   - Deploy from a branch
   - Branch: **main** / Folder: **/** (root)
4. 点击 **Save**

---

### 步骤 4：等待部署（1-2 分钟）

1. 刷新 Pages 设置页面
2. 看到 **Your site is live at** 绿色提示
3. 复制链接，格式：
   ```
   https://YOUR_USERNAME.github.io/slides/
   ```

---

## 🌐 访问链接

部署完成后，任何人都可以访问：

**主页（画廊）：**
```
https://YOUR_USERNAME.github.io/slides/
```

**单页直接访问：**
```
https://YOUR_USERNAME.github.io/slides/genai-anxiety-slide-lv-premium.html
https://YOUR_USERNAME.github.io/slides/openclaw-workflow-lv-premium.html
```

---

## 🎨 自定义域名（可选）

如果想用自定义域名（如 `slides.yourname.com`）：

1. 在 Pages 设置页面，找到 **Custom domain**
2. 输入你的域名
3. 点击 **Save**
4. 在域名 DNS 设置添加 CNAME 记录：
   ```
   CNAME YOUR_USERNAME.github.io
   ```

---

## 📊 文件结构

```
github-pages/
├── index.html                          # 主页（画廊）
├── genai-anxiety-slide-lv-premium.html  # AI 焦虑（LV Premium）
├── openclaw-workflow-lv-premium.html    # OpenClaw 工作流（LV Premium）
└── genai-anxiety-slide.html             # 原始版本
```

---

## ✅ 检查清单

- [ ] 创建 GitHub 账号（如果没有）
- [ ] 创建公开 repo
- [ ] 上传所有 HTML 文件
- [ ] 开启 GitHub Pages
- [ ] 等待部署完成（1-2 分钟）
- [ ] 测试链接是否可以访问
- [ ] 分享给 xinyi 🎉

---

## 💡 更新文件

之后如果要更新 slides：

1. 修改本地 HTML 文件
2. 重新上传到 GitHub（覆盖原文件）
3. 或者用 git push：
   ```bash
   git add .
   git commit -m "Update slides"
   git push
   ```
4. GitHub Pages 会自动更新（约 1 分钟）

---

需要我帮你执行 git 命令吗？告诉我你的 GitHub 用户名～ 😊
