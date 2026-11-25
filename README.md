# Kypo MC

Minecraft 26.3 小服的公开页面。

- `index.html` —— 入服指南（GitHub Pages 根页面）
- `CNAME` —— 绑定 `guide.kypo.cn`
- `.github/ISSUE_TEMPLATE/whitelist.yml` —— 「申请白名单」表单

## 白名单是怎么自动加的

服务器上有个 cron，每 3 分钟拉一次本仓库里带 `whitelist` 标签、状态为 open 的 issue：

1. 从正文里解析 `角色名: xxx`
2. `whitelist add xxx`
3. 回一条评论
4. 去掉标签并关闭 issue

所以朋友只要点「New issue → 申请白名单」填个名字，几分钟后就能进服。

> 这个仓库没有任何构建步骤，纯静态。Pages 设置里 Source 选 `Deploy from a branch` → `main` → `/ (root)`。
