# 扁鹊 · bianque

> 分层代码审查：按「正确性 → 安全 → 性能 → 错误处理 → 可读性 → 测试」六层清单逐条审查，输出分级结论与修复建议。

## 审查流程

1. **拿输入**：diff/代码片段 + 变更意图（缺失则停下问用户，不脑补）
2. **定领域**：Web 后端 / ETL / 前端 / 并发 / 存储 / 安全 / 算法，叠加领域失败模式
3. **六层清单**：正确性 → 安全 → 性能 → 错误处理 → 可读性 → 测试
4. **定级**：🔴 blocker / 🟠 major / 🟡 minor / 💡 nit，逐条一句话问题 + 一句话建议

内置 9 条可机械检测的危险模式（命令注入 / eval / innerHTML / pickle.loads / os.system…），命中后按输入可控性定级。

## 触发场景

- 「review 一下」「帮我 review」「审查这段代码」「PR review」「看看这个 diff」
- 不触发：直接改代码/修 bug（按用户要求直接改）；领域架构评审（→ domain-modeling）；技能质量评估（→ darwin）

## 安装

```bash
git clone https://github.com/mrzhangkris/bianque.git ~/.dsh/skills/bianque
```

## 相关技能

- 华佗 `huatuo` 审技能 · 皋陶 `gaotao` 意图把关 · 达尔文 `darwin-skill` 优化

## 许可

MIT © 2026 mrzhangkris
