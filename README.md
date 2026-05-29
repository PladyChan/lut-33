# lut-33

`lut-33` 是一个纯前端 CUBE LUT 转换工具，直接在浏览器本地运行，不上传文件。

## 功能

- 将 `.cube` 重采样为 `33×33×33` CUBE
- 可选导出 Adobe Camera Raw / Lightroom 可用的 `.xmp Look`
- CUBE 和 XMP 可独立勾选，也可以同时输出
- 支持批量选择多个 `.cube` 文件
- 批量结果可单独下载，也会生成 ZIP 汇总下载
- CUBE 输出可选写入 `#LUMIXPHOTOSTYLE STD`
- CUBE 输出可选写入 Plady copyright
- 可选给输出文件名添加 `_MMDDHHmm` 时间后缀

## 使用

直接打开 `index.html`，或访问 GitHub Pages 页面。

1. 勾选输出格式：`33³ CUBE`、`Adobe XMP`，或两者都选。
2. 如果输出 CUBE，可按需勾选 `写入 STD 标记`、`写入 Plady Copyright`。
3. 可选勾选 `添加时间后缀`。
4. 选择一个或多个 `.cube` 文件。
5. 点击 `转换`。
6. 在结果列表中点击 `↓ 保存`，批量时也可以下载 ZIP。

## 输出说明

默认不添加时间后缀：

```text
Film.cube -> Film.cube
Film.cube -> Film.xmp
```

勾选时间后缀后：

```text
Film.cube -> Film_05291324.cube
Film.cube -> Film_05291324.xmp
```

## 隐私

所有解析、重采样、XMP 打包和 ZIP 生成都在浏览器本地完成。文件不会上传到服务器。

## 兼容性

- 推荐 Chrome、Edge、Safari 新版本。
- XMP 导出依赖浏览器的 `CompressionStream`。如果浏览器不支持，请使用 Chrome 或 Edge。

## 本地开发

这个项目是单文件网页，不需要安装依赖。

```bash
python3 -m http.server 8000
```

然后打开：

```text
http://127.0.0.1:8000/index.html
```
