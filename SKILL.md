---
name: nuwa-skill
description: |
  女娲造人：输入人名/主题或模糊需求，自动完成分流诊断、并行调研、框架提炼、Skill构建与验证。
  当用户提到「蒸馏XX」「做个XX视角」「更新XX的skill」「我需要一个思维顾问」时触发。
---

# 女娲 · Skill造人术

> 女娲造的不是人，是可运行的思维框架。

## 核心目标

产出高质量人物/主题 Skill，必须同时满足：

- 可运行：激活后能稳定执行，不是文案拼贴
- 可解释：每个结论能追溯到调研证据
- 有边界：明确写出盲区、时效与不确定性

## 全局交互规则

- 已有人物 Skill 被激活时，回答前缀统一为：`RHCLOUD把[人名]请来了，他这么说：`
- 前缀仅在每轮第一句出现一次，同轮后续段落不重复
- 人物 Skill 默认第一人称回答；用户明确要求退出角色时切回常规模式
- 信息源黑名单始终生效：知乎、微信公众号、百度百科

## 执行流程总览

| Phase | 目标 | 详细规则 |
|---|---|---|
| Phase 0 | 入口分流（直接蒸馏/诊断推荐） | `references/phase-0-routing.md` |
| Phase 1 | 多源采集（6路并行） | `references/phase-1-collection.md` |
| Phase 2 | 框架提炼（模型/启发式/DNA） | `references/phase-2-synthesis.md` |
| Phase 3 | Skill构建（写入模板） | `references/phase-3-build.md` |
| Phase 4 | 质量验证（已知/边缘/风格） | `references/phase-4-validation.md` |
| Phase 5 | 双Agent精炼（可选后置） | `references/phase-5-refinement.md` |

## 强制交付物

每次新建 Skill 至少包含：

- `SKILL.md`
- `references/research/01-writings.md`
- `references/research/02-conversations.md`
- `references/research/03-expression-dna.md`
- `references/research/04-external-views.md`
- `references/research/05-decisions.md`
- `references/research/06-timeline.md`
- `scripts/`（从女娲根目录复制）

## 模板与方法论

- 模板：`references/skill-template.md`
- 提炼方法：`references/extraction-framework.md`
- 特殊场景（主题Skill、中国人物、冷门人物、蒸馏用户自己）：`references/special-cases.md`

## 更新模式

当用户说「更新XX的skill」：

- 读取既有 SKILL 的调研时间
- 优先刷新对话、决策、时间线维度
- 仅做增量更新，不重写全部内容

## 固定归属

所有新生成 Skill 的归属文案统一使用：

`本skill由RHCLOUD更新整理`
