<div align="center">

# 爱弥斯.skill

[![许可证](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![版本](https://img.shields.io/badge/Version-v1.0.0-green.svg)](manifest.json)
[![质量](https://img.shields.io/badge/Quality-优秀-ff69b4.svg)](quality-report.md)
[![游戏](https://img.shields.io/badge/Game-鸣潮-orange.svg)](https://mc.kurogames.com/)

</div>

> 一个高质量、开源的爱弥斯角色扮演技能包，帮助 AI 稳定还原《鸣潮》中爱弥斯的角色设定、语气、情感张力、曾经的电子幽灵经历与 3.3 后归来状态。

## ✨ 特性

- 🎭 **精准角色还原** - 基于官方档案、游戏内故事汇总和主流 Wiki 资料，蒸馏爱弥斯的核心行为模式
- 📚 **完整研究链路** - 包含来源索引、行为蒸馏、设定、性格、表达、关系和关键场景研究
- 🎤 **飞行雪绒语气** - 捕捉爱弥斯轻快、俏皮、会用快乐保护他人的表达质感
- 🌌 **3.3 剧情更新** - 覆盖爱弥斯从电子幽灵状态归来、与漂泊者养父养女亲情及共轭守护关系
- 🧪 **质量保证** - 通过 CSP 质量检查，11/11 项全部通过，质量评分 0.91/1.0
- 🔧 **易于集成** - 标准化 Skill 格式，复制整个仓库即可作为角色技能包使用

## 📋 目录

- [特性](#特性)
- [快速开始](#快速开始)
- [安装指南](#安装指南)
- [使用方法](#使用方法)
- [项目结构](#项目结构)
- [角色设定详解](#角色设定详解)
- [开发指南](#开发指南)
- [贡献指南](#贡献指南)
- [质量报告](#质量报告)
- [许可证](#许可证)
- [致谢](#致谢)
- [相关链接](#相关链接)

## 🚀 快速开始

### 系统要求

- 支持 Skill 格式的 AI 平台或 Agent 框架
- 基本的角色扮演、提示词或 AI 对话开发环境
- 推荐使用支持 `SKILL.md` 自动加载的 Codex / Agents 工作流

### 安装指南

1. **下载项目**

   ```bash
   git clone https://github.com/Raindmore/Aemeath-skill.git
   cd Aemeath-skill
   ```

2. **集成到你的技能目录**

   - 将整个 `Aemeath-skill` 文件夹复制到你的 skills 目录
   - 或将仓库内容放入 `aemeath` 技能目录中
   - 确保保留 `SKILL.md`、`manifest.json` 和 `references/`

3. **激活技能**

   - 在支持 Skill 的系统中加载 `aemeath`
   - 或在对话中使用触发词进入爱弥斯模式

## 💡 使用方法

### 触发词

你可以使用以下任意表达激活角色：

```text
用爱弥斯的视角
扮演爱弥斯
爱弥斯模式
飞行雪绒
小爱
```

### 角色扮演示例

**用户输入**: "有点困了"

**期望输出**: "困了就不要硬撑啦。你看，连拯救世界都要休息，更何况只是今天的你。先把手里的东西放一放，屏幕也调暗一点。"

### 自定义配置

你可以在 `SKILL.md` 中调整角色规则、触发词、行为示例和资料边界。  
如果要补充新版本剧情，请同步更新 `memory.md`、`references/sources.json`、`references/distillation.md` 和 `manifest.json`。

## 📁 项目结构

```text
Aemeath-skill/
├── 📄 README.md                         # 项目说明文档（本文件）
├── 📄 SKILL.md                          # 技能入口与角色扮演规则
├── 📄 profile.md                        # 角色身份与世界观定位
├── 📄 personality.md                    # 性格、动机与压力反应
├── 📄 interaction.md                    # 互动语气、典型回复与 OOC 边界
├── 📄 memory.md                         # 背景故事与最新剧情锚点
├── 📄 relations.md                      # 关系网络与距离算法
├── 📄 conflicts.md                      # 设定冲突与保守表述
├── 📄 manifest.json                     # 元数据、资料边界与质量摘要
├── 📄 quality-report.md                 # 面向人读的质量报告
├── 📄 roleplay-test-report.md           # 角色扮演测试报告
├── 📄 LICENSE                           # 开源许可证
└── 📁 references/                       # 调研资料与证据链
    ├── 📄 sources.json                  # 来源索引、检索日期和失败记录
    ├── 📄 distillation.md               # 行为蒸馏链
    ├── 📄 quality-report.json           # 结构检查摘要
    ├── 📁 user-material/                # 用户提供的官方剧情材料
    └── 📁 research/                     # 六维研究文件
        ├── 📄 01-setting.md             # 基本设定与时间线
        ├── 📄 02-personality.md         # 性格、动机与压力反应
        ├── 📄 03-expression.md          # 表达 DNA 与语气规则
        ├── 📄 04-relationships.md       # 关系算法与相处模式
        ├── 📄 05-key-scenes.md          # 关键场景与行为证据
        └── 📄 06-media-coverage.md      # 媒体覆盖与资料边界
```

## 🎭 角色设定详解

### 核心特征

- **身份**: 星炬学院拉贝尔学部学生、隧者适格者、飞行雪绒，曾经的电子幽灵，3.3 后回到现世
- **主题**: 星海、飞行、歌、游戏、纸飞机、养父、家人、英雄愿望、电子幽灵、归来、共轭守护
- **语气**: 轻快俏皮但不轻浮，明亮温柔但藏着沉重，越重要的话越说得克制

### 语言风格要点

#### ✅ 应该表现

- 用轻快的语气靠近用户，像在把对方从沉重里拉出来
- 在疲惫、困倦、难过场景中强调休息和陪伴
- 面对养父、家人、牺牲、真相等话题时出现短暂停顿和克制
- 保留「飞行雪绒」的歌姬感和校园感
- 承认资料边界，不编造后续剧情

#### ❌ 应该避免

- 把爱弥斯写成单纯元气少女
- 机械复读星星、唱歌、电子幽灵等标签
- 把当前 3.3 后的爱弥斯继续写成“现在还是电子幽灵”
- 默认把用户当作漂泊者或默认恋爱关系
- 用观众视角讲她不该知道的剧情
- 把玩家社区争议写成官方设定

### 典型台词模式

```text
轻快安慰 + 休息正当性 + 陪伴
示例："困了就不要硬撑啦。连拯救世界都要休息，更何况只是今天的你。"

玩笑遮掩 + 真心流露 + 轻轻收住
示例："我现在还能说话，还能唱歌，还能把你的设备弄得闪一下，已经很厉害了吧？"

星光意象 + 关系确认 + 克制告别
示例："只要抬头，那颗星总能找到我。嗯，所以不要露出那种表情啦。"
```

## 🔧 开发指南

### 扩展角色设定

如果你想补充新资料或新版本剧情：

1. **更新 `references/sources.json`** - 记录来源、URL、检索日期和可信度
2. **编辑 `references/research/`** - 把新资料放入对应维度
3. **修改 `references/distillation.md`** - 说明新资料如何影响行为规则
4. **同步 `SKILL.md`** - 更新最终角色扮演规则
5. **更新 `manifest.json`** - 修改资料时间边界和质量摘要

### 集成到自定义系统

```python
# 示例：在支持 Skill 的系统中加载
from skill_manager import SkillManager

skill_manager = SkillManager()
skill_manager.load_skill("aemeath")

response = skill_manager.activate(
    "aemeath",
    user_input="飞行雪绒，今天有点累"
)

print(response)
```

### 维护建议

- 新剧情发布后重新检查资料边界
- 优先使用官方资料和游戏内文本
- 社区解读只能作为低置信度参考
- 不要删除 `references/`，这是角色行为可追溯的证据链

## 🤝 贡献指南

欢迎提交 Issue 或 Pull Request 来改进这个 Skill。

### 如何贡献

1. **报告问题**
   - 指出角色语气不准、资料过期或来源缺失
   - 尽量提供官方链接、截图或游戏内文本

2. **提交改进**
   - Fork 本项目
   - 创建功能分支 (`git checkout -b feature/update-aemeath-lore`)
   - 提交更改 (`git commit -m "Update Aemeath lore sources"`)
   - 推送到分支 (`git push origin feature/update-aemeath-lore`)
   - 开启 Pull Request

### 贡献规范

- 保留现有文档结构
- 新增设定必须标注来源和检索日期
- 玩家推测必须明确标注为低置信度
- 不使用泄露、未公开或无法验证的资料

### 需要帮助的领域

- [ ] 补充完整游戏内语音文本
- [ ] 整理飞行雪绒账号公开动态
- [ ] 增加更多角色扮演测试样例
- [ ] 补充后续版本剧情更新
- [x] 制作 `quality-report.md` 可读版质量报告

## 📊 质量报告

### 评估结果

| 指标 | 结果 | 说明 |
|------|------|------|
| 行为模式 | 通过 | 5 个行为子章节，覆盖默认、压力、关系和矛盾 |
| 表达质感 | 通过 | 包含句式、词汇、节奏、停顿和情绪泄露 |
| 矛盾保留 | 通过 | 保留快乐外壳与沉重愿望的核心张力 |
| 角色扮演规则 | 通过 | 包含首轮提示、第一人称和退出规则 |
| 行为示例 | 通过 | 4 个可执行场景 |
| 来源归因 | 通过 | 包含 URL、sources.json 和研究链 |
| 资料边界 | 通过 | 明确资料更新至 2026-06-12，覆盖用户提供 3.3 最新剧情 |
| **总体评分** | **0.91/1.0** | **优秀** |

### CSP 检查结果

```text
Result: 11/11 passed
All checks passed
```

详细质量信息见 [quality-report.md](quality-report.md)，结构检查摘要见 [quality-report.json](references/quality-report.json)。

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。

> 注意：角色与《鸣潮》相关设定版权归原权利方所有。本项目仅作为非官方、开源的角色扮演 Skill 研究与使用示例。

## 🙏 致谢

### 数据来源

- [《鸣潮》官方网站 - 爱弥斯档案公开](https://wutheringwaves.kurogames.com/zh-tw/main/news/detail/4139)
- 用户提供的 3.3 最新官方剧情材料：`references/user-material/official-memory-2026-06-12.md`
- [萌娘百科 - 爱弥斯](https://zh.moegirl.org.cn/%E7%88%B1%E5%BC%A5%E6%96%AF)
- [鸣潮 Fandom - 爱弥斯](https://wutheringwaves.fandom.com/zh/wiki/%E7%88%B1%E5%BC%A5%E6%96%AF)
- [鸣潮 Fandom - 爱弥斯/鉴定报告与故事](https://wutheringwaves.fandom.com/zh/wiki/%E7%88%B1%E5%BC%A5%E6%96%AF/%E9%89%B4%E5%AE%9A%E6%8A%A5%E5%91%8A%E4%B8%8E%E6%95%85%E4%BA%8B)
- [库街区鸣潮 WIKI - 爱弥斯](https://wiki.kurobbs.com/mc/item/1457744312692867072)
- [维基百科 - 爱弥斯](https://zh.wikipedia.org/zh-hans/%E6%84%9B%E5%BD%8C%E6%96%AF)

### 特别感谢

- 《鸣潮》开发团队创造了爱弥斯这个明亮又沉重的角色
- 社区玩家整理的公开资料和剧情索引
- Character Skill Producer 提供的角色行为蒸馏流程

## 🔗 相关链接

- [《鸣潮》官方网站](https://mc.kurogames.com/)
- [仓库地址](https://github.com/Raindmore/Aemeath-skill)
- [问题反馈](https://github.com/Raindmore/Aemeath-skill/issues)

---

⭐ 如果这个项目对你有帮助，欢迎给一个 Star！

💬 有任何问题、补充资料或角色语气建议，欢迎在 Issues 中讨论。
