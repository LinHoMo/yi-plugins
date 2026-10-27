# Yi 术数插件发行树

本仓库只放**可安装的产物**（含随包 Python 引擎与判据知识库）。它是自动生成物，
**不要手工编辑**——源在 [LinHoMo/Yi](https://github.com/LinHoMo/Yi) 的 `plugins/`，
由 `plugins/scripts/publish.mjs` 生成。

古籍案例库按隔离纪律**永不随包**；库内一切分数是古籍案例对齐分，不是现实命中率。

## 各宿主怎么装

| 宿主 | 目录 | 安装 |
|---|---|---|
| dsh | `dsh-plugin/` | `dsh plugin --profile <profile> add "link:./dsh-plugin"` |
| claude | `claude-plugin/` | `/plugin marketplace add LinHoMo/yi-plugins` → `/plugin install yi@yi-plugins`（309 批真机通过） |
| codex | `codex-plugin/` | `codex plugins install https://github.com/LinHoMo/yi-plugins` 或登记 .agents/plugins/marketplace.json |
| gemini | `gemini-plugin/` | `gemini extensions install https://github.com/LinHoMo/yi-plugins` |
| yan | `yan-plugin/` | Yan 市场添加来源 `https://github.com/LinHoMo/yi-plugins`，稀疏路径填 `yan-plugin` |

需要本机 **Python 3.10+**（引擎是 Python）与 **node**（MCP 入口）。

> ⚠ Claude 的市场条目（`.claude-plugin/marketplace.json`）**未真机验证**：
> 官方示例是「市场仓 → 独立插件仓」，这里改指同仓子目录。
> 未跑通前请用 `claude --plugin-dir ./claude-plugin` 本地试装。
