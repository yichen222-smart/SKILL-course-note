# course-note

根据课件（PDF/PPTX）自动生成 .md 格式的结构化课堂笔记。

## 快速部署

### 方法一：交给 AI 处理

把本仓库链接发给你的 Claude Code 或 Codex，告诉它"部署这个 skill"，它会自动完成以下操作：

```
https://github.com/yichen222-smart/SKILL-course-note
```

### 方法二：手动部署

```bash
# 1. 安装 Python 依赖
pip install pymupdf python-pptx

# 2. 安装 skill 到 Claude Code
npx skills add https://github.com/yichen222-smart/SKILL-course-note
```

## 功能

- 支持 PDF 和 PPTX 两种格式的课件
- 自动提取课件文字内容
- 按标题层级生成结构化笔记（一级/二级/三级标题）
- 保留核心定义、公式、表格、案例
- 自动标注关键术语英文原文
- 考点高亮标记
- 用户确认机制（文件路径、存储位置）

## 使用

1. 告诉 Claude "帮我根据课件做笔记"，提供课件文件路径
2. Skill 会先与你确认文件路径和存储位置
3. 自动提取课件内容并生成结构化笔记
4. 输出 Markdown 文件到指定位置

## 文件结构

```
course-note/
├── SKILL.md               # Skill 指令文件
├── requirements.txt        # Python 依赖
├── README.md
└── LICENSE
```

## 依赖

- Python 3.8+
- PyMuPDF（fitz）
- python-pptx

## 许可证

MIT
