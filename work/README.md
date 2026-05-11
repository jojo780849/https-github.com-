# work-dashboard

Chris 的工作监控台合集 · 静态站点托管于 GitHub Pages。

## 在线访问

- 🌐 首页：https://jojo780849.github.io/work-dashboard/
- 🌫️ 埋汰线进度：https://jojo780849.github.io/work-dashboard/maitaixian-progress/

## 目录结构

```
work-dashboard/
├── index.html                       # 项目分类首页
├── README.md
└── maitaixian-progress/             # 埋汰线进度与人员工作计划
    └── index.html                   # 监控台（自带数据，单文件可分享）
```

## 新增看板的标准流程

1. 在仓库根目录新建一个分类目录，例如 `xxx-progress/`
2. 把单文件 HTML（数据已内联那种）放进去并重命名 `index.html`
3. 编辑根目录 `index.html`，在对应分类下加一个新的 `<a class="card">` 卡片
4. `git add . && git commit -m "..." && git push`
5. 等 1-2 分钟 GitHub Pages 重新部署即可

## 更新埋汰线监控台

源数据维护在工作区：`c:/Users/chrisciou/WorkBuddy/20260509152710/dashboard/data.js`

更新流程：
```powershell
cd c:/Users/chrisciou/WorkBuddy/20260509152710/dashboard
# 编辑 data.js
node build.js
# 复制到仓库
Copy-Item dashboard-standalone.html D:\github\work-dashboard\maitaixian-progress\index.html -Force
cd D:\github\work-dashboard
git add . ; git commit -m "update maitaixian dashboard" ; git push
```
