# Swivel 简体中文版

基于 [jonathanlotan/Swivel v1.0.0](https://github.com/jonathanlotan/Swivel/tree/v1.0.0) 的非官方简体中文本地化副本。上游采用 MIT 许可证，版权归 Jonathan Lotan 所有。

## 下载使用

点击 **Swivel-zh-Hans-macOS.zip**，选择下载原始文件（Download raw file），解压后打开 **Swivel 中文版.app**。这是为 Apple 芯片 Mac 构建的应用，已在本机 macOS 27.2 上实际启动。

本副本使用独立应用标识和独立设置，不覆盖原版。使用时建议先退出原版，避免两个轮盘同时响应。应用运行于菜单栏，不显示 Dock 图标。登录启动需自行开启。

- `Swivel-zh-Hans-macOS.zip`：可运行应用。
- `Swivel-zh-Hans-source.zip`：完整中文源码及翻译映射。
- `VALIDATION.md`：范围、测试和已知限制。
- `SHA256SUMS.txt`：压缩包校验值。
- `LICENSE`：上游 MIT 许可证。

## 中文范围

菜单、设置、欢迎页、轮盘、裁剪、元数据、暂存架、转换工具、内部错误提示、Finder 服务与扩展名称、快捷指令描述等已中文化。格式名、单位、物理按键名和用户内容保留原样。

## 构建

使用 Xcode 26+（本次使用 27.2）和 XcodeGen。解压源码，在源码目录运行：

```sh
cd Converter
xcodegen generate
xcodebuild -project Converter.xcodeproj -scheme Converter -configuration Release -derivedDataPath /tmp/swivel-zh-build build
```

产物为 `/tmp/swivel-zh-build/Build/Products/Release/Swivel中文版.app`。此中文副本已修改产品名称，上游 Makefile 中固定的原版产品路径需自行适配，直接使用以上命令即可。

## 限制

本机临时签名，未使用官方 Developer ID 或苹果公证；“快捷指令”可能无法发现该副本的 App Intents。PDF 压缩样例在本机和未修改的官方源码上均未缩小，应用会提示并保留原件。详见验证说明。

此仓库用于私人保存，不代表上游官方发行版。
