# 儿童脑筋急转弯题库

本仓库仅存放公开题目数据，不包含小程序源码、访问令牌、朗读密钥或用户数据。

## 数据入口

https://raw.githubusercontent.com/ssf1226/brain-teaser-questions/main/questions.json

`questions.json` 包含 `schemaVersion: 1`、内容版本 `version` 和 `questions` 数组。当前首批 559 题，三个年龄段为 `3-5`、`6-8`、`9-10`。

每题字段：稳定 `id`、年龄 `ageGroup`、分类 `category`、题干 `question`、答案 `answer`、解释 `explanation`、提示 `hint`、难度 `difficulty`、陪读说明 `reading`、状态 `status`、兼容旧 ID 的 `legacyIds` 和旧题干的 `legacyQuestions`。

## 更新规则

- 优先在小程序项目的审核数据中修改，然后执行构建和导出脚本；不要编辑生成的运行时 JS。
- `id` 发布后不得重排或用于另一道题。修正题干时保留旧题干到 `legacyQuestions`，确保旧掌握记录仍有效。
- 停用题目设为 `disabled`，尽量保留条目，不复用 ID。
- 每次更新须运行校验、查看 Git diff，再提交推送；可通过恢复旧版完整 JSON 回滚。
- 客户端本次启动使用固定快照，新下载数据在下次冷启动启用。不是实时推送。
- GitHub 链接是否可用于微信正式版，需单独验证合法请求域名及真机网络。请求失败时客户端保留本地题库。

## 内容说明

内容经过编辑筛选，包含经典题型改写和自主编写。仓库公开不代表所有内容均已获得第三方再授权，也不自动授予商业转载许可。如发现不严谨或侵权内容，请提交 Issue，附题目 ID。
