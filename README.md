<div align="center">

# AnyMovie

**一款注重视觉与遥控器体验的 Android TV / TVBox 播放器。**

沉浸背景 · 海报浏览 · 多源播放 · 手机扫码导入

[界面预览](#界面预览) · [功能介绍](#功能介绍) · [开始使用](#开始使用) · [下载安装](#下载安装)

</div>

![AnyMovie 沉浸式首页](docs/screenshots/home.png)

AnyMovie 希望让 TVBox 不仅能播放，也能拥有好看的界面和顺手的电视交互。

从浏览海报、查看详情，到选择播放来源，整个过程围绕遥控器设计。深色界面搭配影片背景、清晰的焦点反馈和克制的动效，让注意力回到内容本身。

## 界面预览

以下为应用实际运行截图，包含内容浏览、播放、导入和完整设置流程。部分内容页使用隔离测试数据填充，仅用于展示界面，不代表应用内置影视资源。扫码截图使用已失效的测试地址与配对码。

### 浏览与播放

| 海报首页 | 分类筛选 |
| :---: | :---: |
| ![海报首页与影片背景](docs/screenshots/home-catalog.png) | ![分类浏览与筛选](docs/screenshots/category.png) |

| 搜索与输入 | 影片详情与播放线路 |
| :---: | :---: |
| ![搜索键盘与结果](docs/screenshots/search.png) | ![影片详情与线路选择](docs/screenshots/detail.png) |

| 播放控制 | 倍速选择 |
| :---: | :---: |
| ![视频播放与遥控器操作栏](docs/screenshots/player.png) | ![播放倍速面板](docs/screenshots/player-speed.png) |

### 数据源导入

| 添加数据源 | 网址导入 |
| :---: | :---: |
| ![网址与手机扫码两种导入入口](docs/screenshots/source-import.png) | ![电视端网址输入](docs/screenshots/url-import.png) |

| 手机扫码导入 | 无源首页 |
| :---: | :---: |
| ![手机扫码导入面板，二维码为失效测试示例](docs/screenshots/qr-import.png) | ![无数据源的空态首页](docs/screenshots/empty-home.png) |

### 设置与影片资料

| 主站选择 | 显示设置 |
| :---: | :---: |
| ![内容来源选择](docs/screenshots/primary-site.png) | ![显示与动效设置](docs/screenshots/display-settings.png) |

| 播放设置 | 海报与简介 |
| :---: | :---: |
| ![播放解码设置](docs/screenshots/playback-settings.png) | ![TMDB 海报与简介配置](docs/screenshots/scraper-settings.png) |

<details>
<summary>展开更多设置截图：高级、存储、关于与隐私说明</summary>

| 高级设置 | 存储管理 |
| :---: | :---: |
| ![源兼容模式与网络选项](docs/screenshots/advanced-settings.png) | ![缓存、备份与重置](docs/screenshots/storage-settings.png) |

| 关于 | 免责与隐私说明 |
| :---: | :---: |
| ![关于与 TMDB 署名](docs/screenshots/about.png) | ![联网、本机数据与第三方代码说明](docs/screenshots/privacy.png) |

</details>

截图中的海报及背景图片来自相应数据源或 TMDB，版权归各自权利人所有。播放画面使用 Blender Foundation 的 *Big Buck Bunny* 预告片（[视频来源](https://media.w3.org/2010/05/bunny/trailer.mp4)）。

## 功能介绍

### 好看的大屏界面

- **沉浸式影片背景**：首页背景跟随当前焦点影片切换，配合片名与简介展示。
- **有层次的遮罩**：上下较暗、中间较轻，让背景可见，同时照顾前景内容的可读性。
- **海报式内容浏览**：分类分区、横向海报列表和继续观看入口，适合沙发上的浏览距离。
- **明确的焦点反馈**：海报缩放、图标反色和渐变动画，帮助快速识别当前选中位置。
- **统一的设置界面**：图标与文字结合，菜单获得焦点即展示对应选项。

### 从导入到播放

- **TVBox 配置接入**：支持 TVBox 配置及多种源类型，包含 JS / JAR 源的运行接入。
- **网址导入**：在电视上填写数据源地址，预览后确认导入。
- **手机扫码导入**：手机与电视连接同一局域网，扫码打开网页并提交配置，在电视端确认后生效。
- **多源搜索**：按来源展示搜索结果，方便选择可用资源。
- **详情页选源**：点击海报进入详情页，查看可用来源、播放线路和剧集，再选择播放。
- **播放控制**：基于 Media3，提供选集、线路切换、倍速、音轨及字幕相关操作。
- **继续观看**：保存播放进度，方便接着上次的位置观看。

### 资料与缓存

- **可选的 TMDB 刮削**：补充海报、背景图和影片简介；启用后优先展示匹配资料，不可用时回退到原站内容。
- **缓存优先的首页**：先展示已缓存内容，再在后台更新，减少反复等待。
- **减少重复请求**：刮削资料持久缓存、同一查询去重，并对 TMDB 公共图片设置有容量限制的磁盘缓存。
- **凭据本机保存**：TMDB API Key 或 Read Access Token 由用户自行填写。

## 开始使用

运行环境：**Android 7.0（API 24）及以上**，面向 Android TV、电视盒子和遥控器操作场景。

1. 打开应用，选择首页的 **导入数据源**，或进入 **设置 → 数据源**。
2. 选择 **网址导入** 或 **手机扫码导入**，提交配置并在电视端确认。
3. 在 **设置 → 选择主站** 中选择内容来源。
4. 浏览或搜索影片，进入详情页，选择来源、线路与剧集后播放。

需要海报与简介补充时，可前往 **设置 → 显示 → 海报与简介** 填写自己的 TMDB 凭据。

> 当前版本默认从无源状态启动，不自动加载测试源，也不提供演示内容。首次使用需要自行添加数据源；TMDB 刮削为可选功能。

**遥控器操作**

| 按键 | 操作 |
| --- | --- |
| 方向键 | 浏览内容、切换菜单与选项 |
| 确认键 | 打开详情、执行当前操作或选择播放 |
| 返回键 | 关闭当前面板或返回上一页 |

## 下载安装

前往 [Releases 下载最新安装包](https://github.com/OMOBruce/anymovie-releases/releases)。

- **universal**：通用安装包，不确定设备架构时优先选择。
- **arm64-v8a**：适用于 64 位 ARM 设备。
- **armeabi-v7a**：适用于 32 位 ARM 设备。

下载 APK 后通过电视或盒子的安装工具安装。当前为预览版本，仍在持续迭代；不同数据源与设备的兼容情况可能有所差异。

本仓库用于公开产品介绍、界面截图与安装包。应用源码保存在独立的私有仓库中；Releases 自动生成的 Source code 压缩包仅包含本仓库的公开文档与截图。

使用问题与建议可提交至 [Issues](https://github.com/OMOBruce/anymovie-releases/issues)，请附上应用版本、设备型号、复现步骤及已脱敏的错误信息。

## 关于内容与第三方服务

AnyMovie 是播放器项目，不托管影视资源。请自行提供并使用有权访问的数据源。

可选的影片资料补充使用 [TMDB](https://www.themoviedb.org/)。

This product uses the TMDB API but is not endorsed or certified by TMDB.
