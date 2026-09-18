# Anki Cloze Note 生成 Skill

将任意知识内容（文档、笔记、教材片段）转化为符合记忆科学原则的 Anki Cloze Note。

基于 SuperMemo 20 条规则、最小信息原则、主动回忆与认知负荷理论设计，面向面试高频知识点优化。

## 特性

- **最小信息原则**：每张 Cloze 只考察一个知识点，卡片上下文独立
- **正确的 Note/Card 模型**：一个知识点 = 一个 Cloze；一个 Note 可包含多个属于同一认知单元的 Cloze
- **面试导向**：优先提取源码、机制、原理、参数、场景、性能优化、易混淆点
- **综合 + 原子分层**：先建整体认知的综合 Note，再拆分原子 Note
- **事实校验**：指出并更正输入中的错误或过时信息，不编造内容

## 输出格式

每行一个 Note，格式为：

```
Text | Example | Tag
```

## 安装

将本目录（含 `SKILL.md`）放入你的 agent skill 目录，例如：

- Codex / ZCode / Claude Code：`~/.agents/skills/anki-cloze-skill/`

## 使用

安装后对 agent 说：

> 以下是我今天阅读的一小节文档，请你把本节知识点制作成 Anki Cloze Note。
> （附上文档内容）

即可获得可直接导入 Anki 的 Cloze 制卡结果。
