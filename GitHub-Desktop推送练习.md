# 学习笔记：GitHub Desktop 推送流程练习

日期：2026-07-30

## 今天踩过的坑

- 在 GitHub 网站提前建好空仓库后，GitHub Desktop 点 Publish 会报：
  `Repository creation failed. (name already exists on this account)`
- 原因：云端已有同名仓库，Desktop 不能再创建一份
- 解决：用命令行把本地仓库牵手到云端
  - `cd /d "G:\AI财务自动化学习\xingxing-ai-finance-road"`
  - `git remote add origin https://github.com/taoqibao1081-sudo/xingxing-ai-finance-road.git`
  - `git branch -M main`
  - `git push -u origin main`
- Windows 命令行跨盘符切换目录要加 `/d` 参数，否则白切

## 以后日常推送三步曲（用 GitHub Desktop）

1. 在本地文件夹里改文件 / 加文件
2. 打开 GitHub Desktop，左下角写 Summary，点 **Commit to main**
3. 点顶部的 **Push origin**，把改动推到 GitHub 云端

## 验证小技巧

- 推送完去 `https://github.com/taoqibao1081-sudo/xingxing-ai-finance-road` 刷新，能看到新文件就成功了
