# 维护说明

本目录已按 GitBook 友好的方式拆分为多页 Markdown：

- 首页使用 README.md
- 目录导航使用 SUMMARY.md
- GitBook 根目录通过仓库根部的 .gitbook.yaml 指向 gitbook-manual/

## 图片说明

当前 `gitbook-manual/` 已改为引用本地图片，图片统一存放在 `gitbook-manual/assets/`。

如果后续重新从石墨导出并生成文档，建议继续保持这种结构：

1. 先导出原始 Markdown
2. 提取图片到本地目录
3. 重新生成 `gitbook-manual/`
4. 再执行本地图片替换

## 更新方式

如果石墨原文再次更新，推荐按以下顺序执行：

`.\manual\extract-markdown-images.ps1 -SourcePath '东华理工大学超算平台用户手册.md'`

`.\manual\prepare-gitbook.ps1`

`.\manual\localize-gitbook-images.ps1`

其中：

- `extract-markdown-images.ps1` 用于将图片落到本地
- `prepare-gitbook.ps1` 用于重新生成分章节文档
- `localize-gitbook-images.ps1` 用于把分章节文档中的图片改成相对本地路径
