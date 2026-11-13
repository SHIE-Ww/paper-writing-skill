# Paper Writing Skill

面向科研论文的轻量级 Agent Skill：**故事构建 → 分段写作 → 语言精修 → 框架图设计**。适用于 Codex、Claude Code 和其他支持 [Agent Skills](https://agentskills.io/specification) 的工具。

> AI 辅助论证和表达，不代替作者提出研究贡献，也不编造文献、实验或结果。

## 功能

| 任务 | 使用方式 |
| --- | --- |
| 论文主线 | 区分“老问题，新方法”与“发现新问题”，梳理动机、创新点和证据 |
| 反向审稿 | 对每项核心主张提出反驳，定位证据缺口 |
| 分章节写作 | 参考同领域论文的结构，先定段落任务，再逐段修改 |
| 语言润色 | 删除空话和过度防御，保留必要的科学限定 |
| 框架图 | 设计多种布局方案，规划可编辑的 PPT 矢量重绘 |

## 安装

复制 [`skills/paper-writing`](./skills/paper-writing/) 文件夹到 Agent 的 Skill 目录，例如 Codex：

```bash
mkdir -p ~/.agents/skills
cp -R skills/paper-writing ~/.agents/skills/paper-writing
```

上述命令在**已下载或克隆本仓库的根目录**执行。其他 Agent 使用各自支持的技能目录。

## 使用示例

```text
使用 paper-writing，帮我检查论文的动机和创新点。
我会给出问题现象、失败案例、相关工作、方法模块和实验；
请先整理“挑战—模块—证据”对应关系，再以审稿人视角质疑。
```

```text
使用 paper-writing，只修改下面的引言段落。
参考我提供的已定稿摘要和论文主线，保留技术事实和原意，
标出逻辑跳跃与模板化表达；不要重写整章。
```

```text
使用 paper-writing，基于摘要、引言和方法设计 5–6 种框架图布局。
先比较布局与信息流，不要虚构模块；再给出可编辑 PPT 的重绘步骤。
```

## 目录

```text
skills/paper-writing/
├── SKILL.md               # 执行规则与工作流
└── references/
    └── prompts.md         # 按任务复用的提示词
```

**隐私**：仓库只包含通用方法和指令；不包含原始演示文稿、个人信息、研究材料或未经授权的内容。