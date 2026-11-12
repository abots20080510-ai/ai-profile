# 工作流 · AI 音乐（Suno v6）

## 分工原则（核心）

> 旋律交给生成模型即兴产出，人耳圈选；AI 侧只做以下四件事：

1. **歌词打磨**——保留原句味道，改生硬处（详见提示词库"歌词打磨"）
2. **结构/曲式设计**——段落布局（A/B 段、间奏、反复记号）
3. **风格提示词**——曲风、乐器、情绪标签
4. **流程与转录**——成片后转录实录谱（简谱），作为最终曲谱形态

## 标准流程

```
歌词定稿 → 曲式设计（段落数/长度/BPM/调性）
  → Suno 提示词组装 → 生成 2-3 版 → 人耳 A/B 圈选
  → 优胜版微调重生成（最多 2 轮）
  → 成片 → 转录简谱（A4 纵向、双行歌词、含反复记号）
```

## Suno 提示词模板

```
【曲风标签】folk, acoustic, gentle, female vocal / male vocal
【情绪】nostalgic, warm, understated
【结构】intro - verse - chorus - verse - chorus - bridge - outro
【乐器】acoustic guitar, light percussion, wood fish accents (section boundaries only)
【排除】heavy drums, electronic, auto-tune
```

## 经验值

- 生成前把 BPM/调性写进提示词，虽然 Suno 不完全遵守，但方向不会跑偏
- 每轮生成保留所有版本标记编号，圈选记录版本号，避免"哪版好听"说不清
- 平台选择：国际网络环境下优先 Suno 官网免费版；国内平台注意歌词审查问题
