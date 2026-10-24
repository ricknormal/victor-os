# 变更记录

格式参考 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)，版本号遵循[语义化版本](https://semver.org/lang/zh-CN/)。

## 谁维护哪些文件

| 类型 | 文件 | 说明 |
|---|---|---|
| 手写 | `AGENTS.md`、`00-purpose.md`、`01-principles.md`、`03-architecture.md`、`04-state.md`、`README.md` | 直接改 |
| 自动生成 | `02-charter.md`、`victor.md`、`diagram.png` | 由 `dsh-victor/export.mjs` 生成，别手改 |

---

## [0.1.0] - 2026-10-24

首个版本。把团队的工作方式从代码和聊天记录里抽出来，变成能搬走的文件。

内容对应插件 `dsh-victor` v0.2.0。

### 新增

- `AGENTS.md`：跨工具入口。采用 [AGENTS.md](https://agents.md) 开放格式，DSH、Codex、Cursor 等会读最近的一份；子目录可以放部门自己的。
- `00-purpose.md`：目的三条——经验可复用、新人第一天能上岗、文件能搬走。
- `01-principles.md`：公司理念六条（无限进步、接纳一切、互相告诫、团体荣誉、复利迭代、往外做）。
- `02-charter.md`：员工准则，每轮都要守的那份，由 `index.js` 的 DISCIPLINE 导出。
- `03-architecture.md`：四层结构（人 / victor / 员工 / 文件），以及"什么能搬、什么搬不走"的边界表。
- `04-state.md`：当前进度与交接，新会话开局先读。
- `victor.md`：合并版内核，给只能贴一段提示词的客户端用。
- `diagram.png`：架构导图。

### 说明

- 硬拦（同一个工具、同样的参数第二次直接拒绝）依赖宿主钩子，实现在插件里，不在本仓库。本仓库保存的是文字、结构与约定。
- `02-charter.md`、`victor.md`、`diagram.png` 一并提交，保证 clone 下来就能直接用；但它们由脚本生成，手改会在下次导出时被覆盖。
