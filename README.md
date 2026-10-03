# novel-to-mini-game-lite

**把课文、小说片段、爆文、家史变成一个低配设备也能流畅运行的单文件小游戏。**
一次会话 · 一个 HTML · 零依赖 · 26KB 起步 · 双击离线可玩。

> A lite derivative of [zenstory-ai/novel-to-game](https://github.com/zenstory-ai/novel-to-game) (MIT):
> one session, one skill, one single-file HTML mini game that runs anywhere —
> built for low-end devices, classroom use, and Chinese creators.

[在线示例：桃花源记·寻向所志](examples/taohuayuan/index.html) —— 26KB，点开即玩。

## 为什么是 Lite

原版是给「想认真做一款改编游戏的人」的重装工作流（七技能、45-90 分钟、梦幻西游级示例）。
但低配用户的瓶颈其实是三件事，Lite 逐一对症：

| 瓶颈 | Lite 的做法 |
| --- | --- |
| token 预算 | 七阶段压成三步，设计文档限行数（10/30/20 行） |
| 会话长度 | 单技能单会话交付，不搞多文档接力 |
| 产出物性能 | 硬预算契约：<300KB、零依赖、禁 WebGL、核显 60fps（[budget.md](skills/novel-to-mini-game-lite/references/budget.md)） |

## 快速开始

需要任意一个支持 Agent Skills 的编码助手（Claude Code / Codex / Kimi Code 等）：

```bash
npx skills add tianqihuang63-png/novel-to-mini-game-lite -g -y -a claude-code -s '*'
```

然后对它说：

```text
把《桃花源记》变成一个能玩的小游戏
```

三步自动走完：速拆原文证据 → 从五大模板选型 → 按低配预算构建并自检。
产物在 `game-lite/项目名/`：三份迷你设计文档 + 一个 index.html + 一份如实的自检记录。

**手机党 / 零环境用户**：不装任何工具也能做，看 [prompt-packs/手机党5卡.md](prompt-packs/手机党5卡.md)——
网页版 AI 按五张卡逐条粘贴，同样出一个单文件游戏。

## 五大模板

选型不发明新类型，只从五个里挑（[templates.md](skills/novel-to-mini-game-lite/references/templates.md)）：

收集探索（景物意象多）· 抉择叙事（两难转折）· 文字冒险（对白心声）· 点击解谜（机关信物）· 卡片抉择（论据博弈）。

每个模板都强制同一个签名规范：**机制旁小字原文锚点**——玩家每触发一个机制，屏幕浮现对应的原文句子。
「AI 没有瞎编」这件事，玩家自己看得见。

## 中文场景速配

课文课文（语文课堂/课件）· 小红书爆文（互动引流，需作者授权）· 家族口述史（长辈向大字号）·
地方神话（文旅彩蛋）。详见 [SKILL.md 速配表](skills/novel-to-mini-game-lite/SKILL.md)。

## 示例

- [桃花源记：寻向所志](examples/taohuayuan/) —— 收集探索 + 双结局，26KB，
  附完整的「机制 ↔ 原文」对应表和三步文档样例。

## 合规

- 优先改编**公版文本**（作者逝世超 50 年），书单见 [docs/公版书单.md](docs/公版书单.md)；
- 改编受版权保护的网文/爆文需自行取得授权，本技能只处理你提供的文本，不传播文本；
- 生成物全年龄、无追踪、零网络请求。

## 致谢与许可

方法骨架（拆书证据 → 方向选择 → 设计 → 构建 → 证据化验收）衍生自
[zenstory-ai/novel-to-game](https://github.com/zenstory-ai/novel-to-game)，MIT License。
需要 45-90 分钟的完整改编工作流时，请直接用原版——它非常出色。
本项目同样以 MIT 发布，详见 [LICENSE](LICENSE) 与 [NOTICE.md](NOTICE.md)。
