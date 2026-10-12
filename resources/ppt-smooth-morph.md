# ppt-smooth-morph

为可编辑 PPTX 规划苹果发布会风格的连贯转场：让章节标题、图片、日期和关键指标在相邻页之间自然衔接，并保留正文、来源、页码及讲稿。

## 资源入口

- [源仓库](https://github.com/gongsunteng001-dotcom/ppt-smooth-morph)
- [完整 Skill 目录](https://github.com/gongsunteng001-dotcom/ppt-smooth-morph/tree/main/ppt-smooth-morph)
- [SKILL.md](https://github.com/gongsunteng001-dotcom/ppt-smooth-morph/blob/main/ppt-smooth-morph/SKILL.md)
- [本次核对的固定版本：f5f4018](https://github.com/gongsunteng001-dotcom/ppt-smooth-morph/tree/f5f4018b9e4f81e31f7c899be203d98da29b4f27)

核对日期：2026-10-12。固定版本指向当时检查的内容，源仓库的 `main` 分支可继续更新。

## 实际文件结构

```text
ppt-smooth-morph/                 # 源仓库根目录
├── README.md
└── ppt-smooth-morph/             # 要安装的完整 Skill 目录
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── references/
    │   ├── motion-patterns.md
    │   ├── native-pptx.md
    │   ├── plan-format.md
    │   └── reference-deck.md
    └── scripts/pptx_morph.py
```

安装时选取内层 `ppt-smooth-morph/`，并保留其中的参考文件、脚本及元数据。

## 在 Codex 中安装

如果目标 Codex 环境提供 `$skill-installer`，可以发送：

```text
使用 $skill-installer，将 GitHub 仓库
gongsunteng001-dotcom/ppt-smooth-morph 中的 ppt-smooth-morph 目录
安装到本机 Codex 的个人 Skills 目录。
安装后核对 SKILL.md、参考文件和脚本是否完整。
```

若需要与本次检查的文件完全一致，指定提交 `f5f4018b9e4f81e31f7c899be203d98da29b4f27`；也可以选择安装源仓库的最新版本。

完成安装后，在目标 Codex 中请求：

```text
使用 $ppt-smooth-morph 给这份 PPT 制作丝滑转场。
让章节标题自然衔接到正文，保持渐变照片稳定，
保留文字可编辑，并兼顾 WPS 播放。
```

同时提供需要处理的 PPTX 文件。

## 依赖与验证范围

- Python 3 与 `lxml`；安装背景时另需 `Pillow`。
- 按源 Skill 的要求，配合环境中的 Presentations Skill 完成制作、渲染与导出。
- 脚本提供文件检查、转场应用及内容保真验证；布局与对象几何变化仍需根据实际页面设计。
- PowerPoint 或 WPS 的实际播放效果取决于版本，交付前需在目标软件中放映检查。

## 维护与插件状态

源仓库继续作为更新入口，本资源目录通过链接收录。当前检查版本没有插件清单或 MCP 配置；要加入 ChatGPT 插件目录，需按 [OpenAI 插件打包文档](https://developers.openai.com/plugins/build/plugins)另行完成打包与安装。

当前检查版本未包含许可证文件；本目录记录资源入口与说明，不新增授权条款。
