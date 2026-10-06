# zhangzzzgog.github.io

个人主页源码，纯静态 HTML + CSS，无需构建。

## 首次部署（GitHub Pages）

```bash
# 1. 在 GitHub 新建一个公开仓库，仓库名必须是：zhangzzzgog.github.io

# 2. 本地初始化并推送
cd site
git init
git add .
git commit -m "Initial personal site"
git branch -M main
git remote add origin git@github.com:zhangzzzgog/zhangzzzgog.github.io.git
git push -u origin main

# 3. GitHub 仓库 → Settings → Pages → Source 选 "Deploy from a branch"，
#    Branch 选 main / (root)，保存。约 1 分钟后访问 https://zhangzzzgog.github.io
```

## 日常更新

```bash
# 修改 index.html / style.css 后
git add . && git commit -m "Update" && git push
```

## 文件说明

| 文件 | 作用 |
|---|---|
| `index.html` | 页面内容（发表论文 / 在研 / 项目 / 关于） |
| `style.css` | 设计变量（`:root` 内的颜色、字体）与样式，含深色模式 |
| `CV_ZhangYilin_EN.pdf` | 简历 PDF，页面顶部「CV (PDF)」链接指向它；更新简历时替换此文件即可 |
| `.nojekyll` | 告诉 GitHub Pages 不要用 Jekyll 处理，直接托管静态文件 |

## 本地预览

```bash
python3 -m http.server 8000   # 然后打开 http://localhost:8000
```
