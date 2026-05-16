# find-new-word

Claude Code routine 的**内容生产工作区**。不是代码仓库,也不会自动发布到任何地方。

## 这个仓库是干什么的

每天由 Claude Code routine 自动跑游戏关键词调研,把结果以 PR 形式提交进来。后续可能还会扩展存放 AI 生成的文章草稿。

所有产出都需要**人工 review**。我会从这里挑选有价值的内容,手动搬到真正的网站仓库去发布。

## 目录结构

| 目录 | 用途 |
|------|------|
| `keyword-research/` | 每日游戏关键词调研报告 |
| `articles/drafts/` | AI 生成的文章草稿(未来扩展) |
| `templates/` | 输出模板,routine 按模板填内容 |
| `archive/` | 过期或不再使用的内容归档 |

## 命名约定

- 关键词调研:`keyword-research/YYYY-MM-DD.md`(例 `2026-05-17.md`)
- 文章草稿:`articles/drafts/YYYY-MM-DD-slug.md`

## 工作流程

1. **routine 自动跑** —— 每日定时触发,产出关键词调研或文章草稿
2. **PR 到 `claude/` 前缀分支** —— 例如 `claude/keywords-2026-05-17`,不允许直接在 `main` 提交
3. **人工 review** —— 我在 GitHub 上看 PR 内容,合格的 merge,不合格的关掉
4. **挑选搬运** —— merge 后从仓库里挑出有价值的产出,手动复制到生产网站仓库去发布

详细的写作风格、分支规范、提交信息格式见 `CLAUDE.md`。
