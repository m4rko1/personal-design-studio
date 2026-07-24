# Personal Design Studio

一个开源的单文件无限设计画布，参考现代 AI 设计工作台的交互方式，支持图片导入、无限缩放、画布拖动、多选、图层管理和 Agnes AI 对话。

## 功能

- 无限缩放与平滑画布拖动
- 图片批量导入和桌面剪贴板粘贴
- 框选、多选、复制、粘贴、删除和图层排序
- 图片按原始比例自适应与等比例缩放
- `@` 图层引用、缩略图预览和对话上下文
- Agnes AI 语言、图片和视频接口
- 所有画布交互均在浏览器本地运行

## 使用

从 GitHub 下载或克隆仓库后，直接用浏览器打开仓库根目录的：

```text
index.html
```

也可以使用任意静态服务器托管仓库根目录。项目本地开发源文件位于
`outputs/personal-design-studio/index.html`，发布时上传为根目录 `index.html`。

## Agnes AI

点击页面右上角的 API 设置，输入 Agnes API Key。Key 只保存在当前浏览器标签页的 `sessionStorage` 中，不会写入项目源码。

项目默认使用以下官方端点：

- Language: `https://apihub.agnes-ai.com/v1/chat/completions`
- Image: `https://apihub.agnes-ai.com/v1/images/generations`
- Video: `https://apihub.agnes-ai.com/v1/videos`

生产环境建议使用服务端代理保存 API Key。

## 快捷键

- `Ctrl + C`：复制选中图层
- `Ctrl + V`：粘贴图层或桌面图片
- `Ctrl + D`：重复选中图层
- `Delete` / `Backspace`：删除选中图层
- `Ctrl + +` / `Ctrl + -`：缩放画布
- `Ctrl + 0`：重置画布
- `Ctrl + 拖动`：平移画布

## License

[MIT](LICENSE)
