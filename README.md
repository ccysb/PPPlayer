<h1 align="center">
  <img src="static/logo.svg" alt="ppplayer" width="300" />
  <br>
  <a href="https://github.com/ccysb/PPPlayer/releases">PPPlayer 桌面版</a>
  <br>
</h1>
<div align="center">

[![](https://img.shields.io/github/v/release/ccysb/PPPlayer?label=Release&logo=github)](https://github.com/ccysb/PPPlayer/releases)
[![](https://img.shields.io/badge/license-MIT-blue.svg)](#许可证)
[![](https://img.shields.io/badge/Python-3.11%2B-3776AB.svg)](https://www.python.org/)
</div>
<div align="center">

[![](https://raw.githubusercontent.com/CodePhiliaX/resource-trusteeship/main/readmex.svg)](https://readmex.com/ccysb/PPPlayer)
[![](https://deepwiki.com/badge.svg)](https://deepwiki.com/ccysb/PPPlayer)
[![](https://img.shields.io/badge/Ask_Zread-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQuOTYxNTYgMS42MDAxSDIuMjQxNTZDMS44ODgxIDEuNjAwMSAxLjYwMTU2IDEuODg2NjQgMS42MDE1NiAyLjI0MDFWNC45NjAxQzEuNjAxNTYgNS4zMTM1NiAxLjg4ODEgNS42MDAxIDIuMjQxNTYgNS42MDAxSDQuOTYxNTZDNS4zMTUwMiA1LjYwMDEgNS42MDE1NiA1LjMxMzU2IDUuNjAxNTYgNC45NjAxVjIuMjQwMUM1LjYwMTU2IDEuODg2NjQgNS4zMTUwMiAxLjYwMDEgNC45NjE1NiAxLjYwMDFaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00Ljk2MTU2IDEwLjM5OTlIMi4yNDE1NkMxLjg4ODEgMTAuMzk5OSAxLjYwMTU2IDEwLjY4NjQgMS42MDE1NiAxMS4wMzk5VjEzLjc1OTlDMS42MDE1NiAxNC4xMTM0IDEuODg4MSAxNC4zOTk5IDIuMjQxNTYgMTQuMzk5OUg0Ljk2MTU2QzUuMzE1MDIgMTQuMzk5OSA1LjYwMTU2IDE0LjExMzQgNS42MDE1NiAxMy43NTk5VjExLjAzOTlDNS42MDE1NiAxMC42ODY0IDUuMzE1MDIgMTAuMzk5OSA0Ljk2MTU2IDEwLjM5OTlaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik0xMy43NTg0IDEuNjAwMUgxMS4wMzg0QzEwLjY4NSAxLjYwMDEgMTAuMzk4NCAxLjg4NjY0IDEwLjM5ODQgMi4yNDAxVjQuOTYwMUMxMC4zOTg0IDUuMzEzNTYgMTAuNjg1IDUuNjAwMSAxMS4wMzg0IDUuNjAwMUgxMy43NTg0QzE0LjExMTkgNS42MDAxIDE0LjM5ODQgNS4zMTM1NiAxNC4zOTg0IDQuOTYwMVYyLjI0MDFDMTQuMzk4NCAxLjg4NjY0IDE0LjExMTkgMS42MDAxIDEzLjc1ODQgMS42MDAxWiIgZmlsbD0iI2ZmZiIvPgo8cGF0aCBkPSJNNCAxMkwxMiA0TDQgMTJaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00IDEyTDEyIDQiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIxLjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K&logoColor=ffffff
)](https://zread.ai/ccysb/PPPlayer)
[![](https://img.shields.io/badge/图表-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=digitalocean)](https://gitdiagram.com/ccysb/PPPlayer)


</div>
# PPPlayer — pywebview 桌面版

> 本项目由 **AI 编写**，整体设计思路（架构、功能取舍、UI/交互方案）也来自 AI。它是对「用 Python + pywebview 做一个轻量桌面视频聚合播放器」这一想法的落地实现。

PPPlayer 是一款基于 **Python + pywebview** 的开源视频聚合播放桌面应用。它聚合多种影视 CMS API 接口（苹果CMS / 飞飞CMS / 海洋CMS 等），内置 M3U8 智能广告过滤与媒体嗅探，所有数据均保存在本地。

## 技术栈

- **Python 3.11+** + uv 包管理
- **pywebview** — 无边框桌面窗口容器（自定义标题栏、边缘缩放、Aero Snap）
- **Flask** — 内置 HTTP 服务器（`127.0.0.1:19527`，嵌入 pywebview）
- **前端** — 原生 CSS（单一设计系统 `style.css`，含语义化组件类 + 轻量工具类层 `u-*`）+ Alpine.js + HLS.js + XGPlayer（弹出播放页）

## 界面预览

截图存放于 [`doc/img/`](doc/img/)，更多说明见 [文档索引](doc/README.md)。

| 主界面 · 卡片墙瀑布流 | 设置中心 · 基础 |
|:---:|:---:|
| ![主界面](doc/img/main.png) | ![设置中心-基础](doc/img/base.png) |

| 设置中心 · 布局（卡片标签自定义） | 设置中心 · API 源 |
|:---:|:---:|
| ![设置中心-布局](doc/img/layout.png) | ![设置中心-API源](doc/img/api.png) |

| 编辑 API 源 | 设置中心 · 数据（Gist 云同步） |
|:---:|:---:|
| ![编辑API源](doc/img/edit-api.png) | ![设置中心-数据](doc/img/data.png) |

## 功能

- 多 CMS 源支持（苹果CMS JSON / 飞飞CMS XML / 海洋CMS 自动适配）
- 搜索、分类浏览、自动加载（滚动无限加载）/ 分页两种模式
- 收藏、播放历史、搜索历史
- 卡片标签自定义（四角 + 标题下方双行）
- CMS 源分类黑名单（按源独立配置）
- **源连接检测** — 设置「API 源」中可单源「检测连接」或「检测全部」，状态以彩色圆点（绿/红/灰）显示，检测中图标旋转
- 片头片尾跳过、自动连播、倍速记忆
- **M3U8 智能去广告**（默认开启）— 自动识别并剔除片头 / 片中广告切片（基于切片源目录签名差异与 `#EXT-X-DISCONTINUITY` 分段），只播放正片；关闭则原样加载
- 主题系统 — 浅色 / 深色 / 跟随系统，叠加 **九套视觉风格**（默认 / NFT / 像素风 / 赛博朋克 / 手绘插画 / 现实·超现实 / 简约 / 未来主义 / 波普艺术），独立组合
- 数据导入导出（JSON 格式，含收藏 / 历史 / 源 / 配置）
- **GitHub Gist 云同步**（设置中心 → 数据）— 把全部本地数据同步到你自己的**私密 Gist**，多设备保持一致：配置 GitHub Token 后自动查找并绑定已有同步 Gist（按固定标记识别，**避免重复创建**），支持「上传到 Gist」/「从 Gist 拉取」，界面展示绑定状态、最近同步时间、最近操作结果与错误信息。Token 仅保存在本地 `data/gist_sync.json`、不明文回显、不随数据上传；拉取只覆盖应用数据、不影响凭据。Token 需具备 gist 读写权限（Fine-grained token 需 `Gists: write`）
- **切源 / 切分类 / 搜索的毛玻璃等待层** — 整页重载时（切换 API 源、切换分类、搜索、首次加载）内容区与导航菜单叠加一层毛玻璃模糊 + 居中加载动画，弱响应期间给出明确反馈；该层被限制在主内容容器内，**绝不遮挡顶部标题栏**（窗口标题栏始终清晰可交互）。无限滚动「加载更多」为增量追加，不触发模糊层
- **播放页全屏控制栏** — 全屏时鼠标移到**顶部**显示顶栏（返回 / 集数 / 全屏 / 置顶 / 窗口按钮），移到**底部**显示底部控件与「设置 / 选集」入口，静止约 3 秒自动隐藏；顶栏图钉按钮可**固定 / 取消固定**控制栏（固定时常显，状态持久化）。拖动进度条 / 点击控件 / 鼠标悬停 / 设置面板打开时均**不会误隐藏**；窗口模式下顶栏保持常显（兼作拖拽标题栏），原交互不受影响
- **播放背景切换** — 播放设置中可选「封面」（视频外留白用封面图模糊填充，默认）或「黑底」（纯黑填充），选择持久化
- **GitHub 更新镜像回退** — 检查更新与下载均**先直连 GitHub**，遇到连接失败 / 非 200 / 下载流中断时自动改用 `https://cdn.gh-proxy.org/` 镜像重试，解决国内网络下 GitHub 不可达导致「检查更新没反应」；两路都失败才明确报错。Gist 同步含 Token，**不走第三方镜像**
- **滚动条跟随主题** — 主内容、设置面板、播放器侧栏、选集列表等所有滚动区域的滚动条颜色统一取主题令牌（`--line-strong` / `--ink-3`），深浅色与九套视觉风格切换时自动同步

## 🌴 注意事项

- 仅此Github发布，请勿上当受骗；请各管理者不要宣传及引流本软件。
- 强烈倡导合法观影，本软件仅作为播放工具，不涉及资源存储或分发。
- 仅供个人学习交流之用，24小时内请自觉卸载，勿作商业用途。
- 在开始使用前，请务必详读并同意用户协议，确保遵守相关规定。

## 获取影视 API 源（JSON 接口）

PPPlayer 本身不内置片源数据，需要自行添加**影视 CMS 采集接口**作为「API 源」。项目支持苹果CMS（JSON）、飞飞CMS / 海洋CMS（XML）等常见格式，并会**按接口实际返回内容自动识别 JSON / XML**，无需手动选择。

### 获取方法一：GitHub 代码搜索

在 GitHub 代码搜索里查找 `provide/vod`：

```
https://github.com/search?q=provide%2Fvod&type=code
```

> GitHub 代码搜索通常需要登录。结果里形如 `https://域名/api.php/provide/vod` 的地址就是采集接口，复制出来即可。

### 获取方法二：向 AI 询问

在豆包、DeepSeek 等 AI 助手里直接输入：

```
cms影视采集接口大全
```

AI 会整理出一批公开采集接口地址，从中挑选可用的按下方格式填入即可。

> 接口由第三方站点提供，AI 给出的地址也可能过时或失效，稳定性与内容均由对方决定；请以「检测连接」结果为准，并自行判断合规性与可用性。

### 常见接口格式

苹果CMS 系接口的四种常见写法（`example.com` 换成实际域名）：

```
https://example.com/api.php/provide/vod
https://example.com/api.php/provide/vod/at/xml
https://example.com/api.php/provide/vod/at/json
https://example.com/inc/apijson.php
```

| 形式 | 说明 |
|---|---|
| `/api.php/provide/vod` | 苹果CMS 标准采集入口，最常见；返回格式由服务端决定，应用会自动探测 JSON / XML |
| `.../provide/vod/at/xml` | 路径末尾 `at/xml` 强制返回 XML（飞飞CMS / 海洋CMS 常用） |
| `.../provide/vod/at/json` | 路径末尾 `at/json` 强制返回 JSON，推荐优先尝试 |
| `/inc/apijson.php` | 部分老版 / 定制苹果CMS 的独立 JSON 接口 |

### 在 PPPlayer 中填入

1. 打开 **设置中心 → API 源 → 新增**，把上面的完整接口地址粘贴到「源地址」。
2. **只填接口地址本身即可**（到 `provide/vod` 或 `.php` 为止），不要手动拼 `?ac=videolist&pg=1`：分类、分页、搜索参数由应用自动追加并去重。若只填站点根地址（如 `https://example.com`），应用会尝试补成标准苹果CMS路径。
3. 用「检测连接」确认返回是否正常（绿点可用 / 红点不可用）；检测通过后在首页顶部切到该源即可浏览。

> 提示：部分源不支持搜索（返回纯文本提示），应用会自动关闭该源的搜索入口；源地址里若把 `?` 误写成 `&`，应用也会容错处理。

## 安装

PPPlayer 提供以下几种安装方式，按需选择：

| 方式 | 适用场景 | 是否需要 Python |
|---|---|---|
| 下载编译好的二进制文件 | 只想使用软件，不想配置开发环境 | 否 |
| PowerShell 一键安装 | Windows 用户，想自动下载并创建快捷方式 | 否 |
| 通过 AI 助手安装 | 不熟悉命令行，希望 AI 代为操作 | 否 |
| 从源码运行 | 开发者，需要改代码或跟进最新源码 | 是（Python 3.11+ / uv） |

### 方式一：下载编译好的二进制文件

1. 打开 Releases 页面：<https://github.com/ccysb/PPPlayer/releases/latest>
2. 下载 `ppplayer.exe`（Windows 单文件）或 `ppplayer-portable.zip`（便携包，解压后得到同样的 exe）。
3. 把 exe 放到任意目录（如 `D:\Apps\`），双击运行即可，无需安装 Python 或依赖。

> 单文件 exe 已内置全部运行依赖；`data/` 配置目录会在 exe 所在位置自动生成。便携包只是用 zip 分发同一个 exe，功能完全相同。

### 方式二：PowerShell 一键安装

打开 PowerShell（Win + X → 「终端」或「PowerShell」，**无需管理员权限**），整段复制执行：

```powershell
$dir = "$env:LOCALAPPDATA\PPPlayer"
New-Item -ItemType Directory -Force $dir | Out-Null
Invoke-WebRequest -Uri "https://github.com/ccysb/PPPlayer/releases/latest/download/ppplayer.exe" -OutFile "$dir\ppplayer.exe" -UseBasicParsing
$ws = New-Object -ComObject WScript.Shell
$sc = $ws.CreateShortcut("$env:USERPROFILE\Desktop\PPPlayer.lnk")
$sc.TargetPath = "$dir\ppplayer.exe"
$sc.Save()
Start-Process "$dir\ppplayer.exe"
```

命令做了四件事：下载最新版 exe 到 `%LOCALAPPDATA%\PPPlayer\`、在桌面创建「PPPlayer」快捷方式、启动程序。`releases/latest/download` 会自动指向最新版本，无需手动改版本号；`-UseBasicParsing` 用于兼容旧版 Windows PowerShell 5.1。

若只想下载、不创建快捷方式，用这一行即可：

```powershell
Invoke-WebRequest -Uri "https://github.com/ccysb/PPPlayer/releases/latest/download/ppplayer.exe" -OutFile "$env:USERPROFILE\Desktop\ppplayer.exe" -UseBasicParsing
```

> 国内直连 GitHub 可能缓慢或失败，可先配置系统代理后重试，或改用上方 Releases 页面手动下载。上面的命令直接粘贴到终端窗口逐行执行即可，无需保存为脚本文件。

### 方式三：通过 AI 助手安装和启动

把下面这段整段发给豆包、DeepSeek 等能执行本机命令的 AI 助手，它会自动完成下载、创建快捷方式、启动与验证：

```
请帮我在这台 Windows 电脑上安装并启动 PPPlayer：
1. 用 PowerShell 下载最新版单文件 exe：
   https://github.com/ccysb/PPPlayer/releases/latest/download/ppplayer.exe
   保存到 %LOCALAPPDATA%\PPPlayer\ppplayer.exe
2. 在桌面创建名为「PPPlayer」的快捷方式，指向该 exe。
3. 启动它，并确认窗口标题显示为 PPPlayer。
4. 如果下载失败，把具体报错原样告诉我，不要自行更改下载地址或来源。
```

> 适用场景：不熟悉命令行、希望 AI 代操作的用户。请确认助手具备在本机执行命令的权限；下载来源只使用上面给出的 GitHub 官方地址，避免第三方站点提供的安装包。

### 方式四：从源码运行（开发者）

适合需要修改代码、跟进最新提交或排查问题的用户，需 Python 3.11+ 与 uv：

```bash
git clone https://github.com/ccysb/PPPlayer.git
cd PPPlayer
uv sync
```

然后按下方「运行」章节启动。

### 验证安装

无论用哪种方式，启动后请确认：

1. 窗口正常打开，标题为 **PPPlayer**（首次启动约 1280×800）。
2. 设置中心 → 基础页可正常打开，且没有提示配置读写失败。
3. 「关于」页显示的版本号与 GitHub Releases 最新版的 tag 一致。
4. 若双击 exe 后没有反应，在 exe 所在目录打开 PowerShell 执行 `.\ppplayer.exe` 观察报错输出。

## 运行

> 仅「从源码运行」需要执行下面的命令；二进制用户直接双击 exe，Docker 用户按上方 Docker 章节启动即可。

```bash
uv run main.py
```

首次启动会自动打开 pywebview 窗口（1280×800），标题为 "PPPlayer"。

## Docker 部署（GHCR 一条命令）

镜像已发布到 GitHub Container Registry，**无需克隆源码**，一条命令即可启动 Web 版：

```bash
docker run -d --name ppplayer -p 19527:19527 \
  -v ppplayer-data:/app/data \
  --restart unless-stopped \
  ghcr.io/ccysb/ppplayer:latest
```

浏览器访问 `http://localhost:19527/`（播放页 `http://localhost:19527/player`）。配置写入命名卷 `ppplayer-data`，容器重建不丢。

常用操作：

```bash
docker logs -f ppplayer          # 查看日志
docker pull ghcr.io/ccysb/ppplayer:latest   # 拉取最新镜像
docker stop ppplayer && docker rm ppplayer  # 停止并删除容器
```

> 私有仓库或 GHCR 包未设为 Public 时，需先 `docker login ghcr.io`（用户名 GitHub ID，密码为具备 `read:packages` 的 PAT）。镜像发布由 `.github/workflows/docker-publish.yml` 在 push main / 手动触发时自动完成。

## Docker 本地 Web 冒烟测试

想用本地源码构建镜像验证（不启动 pywebview 桌面窗口）时：

```bash
docker compose up -d --build
docker compose logs -f web
docker compose ps
```

浏览器访问：

- `http://localhost:19527/` — 主页面
- `http://localhost:19527/player` — 播放页面

停止服务：

```bash
docker compose down
```

> 注意：容器只提供 Web 服务，不启动 pywebview，无法验证独立播放器窗口居中、置顶、拖拽、全屏等桌面能力；这些必须在 Windows 真机执行 `uv run main.py` 验证。容器与桌面端不要同时运行并共用同一份 `data/`，避免配置互相覆盖。

## 构建与发布（Windows 单文件 exe）

通过 GitHub Actions（`.github/workflows/build.yml`）自动构建发布 **Windows 单文件 exe**，产物为 `ppplayer.exe`（单文件）与 `ppplayer-portable.zip`（便携包）。构建期写回版本号并嵌入 Windows 版本资源，源码不维护固定版本常量。

CI 流程、本地打包命令、版本号来源与应用内自更新的完整说明见 **[构建与发布](doc/构建与发布.md)**。

## 项目结构

```
PPPlayer/
├── pyproject.toml           # uv 项目配置（版本号唯一来源：project.version）
├── uv.lock                  # 依赖锁文件
├── Dockerfile               # Web 镜像（最小依赖，不导入 main.py）
├── docker-compose.yml       # 本地 Web 开发/测试服务（19527 -> 19527，image 指向 GHCR）
├── .dockerignore            # 排除桌面端/临时文件，缩小镜像构建上下文
├── requirements.web.txt     # 容器 Web 最小依赖
├── main.py                  # 入口：启动 Flask + pywebview、托盘、窗口管理、系统事件
├── README.md                # 本文件
├── logo.ico                 # 应用图标
├── .github/workflows/
│   ├── build.yml            # CI：版本计算 + 打包 + 版本资源 + 发布 Release
│   └── docker-publish.yml   # CI：构建并推送 Web 镜像到 GHCR（latest + 版本 tag）
├── data/                    # 运行时生成（首次启动后存在）
│   ├── config.json          # 本地配置（源、收藏、历史、设置）—— Gist 同步的数据内容
│   └── gist_sync.json       # Gist 凭据/状态（Token、gist_id、最近同步时间）—— 独立存储，不被同步覆盖
├── doc/                     # 文档与截图
│   ├── README.md            # 文档索引
│   ├── 构建与发布.md         # CI / 打包 / 版本 / 自更新
│   ├── M3U8去广告与同源代理.md # 播放列表过滤与同源代理原理
│   └── img/                 # 界面截图（main / base / layout / api / edit-api / data）
├── src/
│   ├── server.py            # Flask 应用，挂载所有路由
│   ├── gist_sync.py         # GitHub Gist 数据同步（查找/绑定/上传/拉取）
│   ├── updater.py           # 应用内更新（检查/下载/镜像回退/自更新重启）
│   ├── config_store.py      # 配置持久化（config.json 读写）
│   ├── cms/
│   │   ├── base.py          # CMS 抽象基类
│   │   ├── detector.py      # CMS 类型自动检测
│   │   ├── endpoint.py      # 接口地址拼接与容错
│   │   ├── http.py          # 网络请求（IPv4 优先 / TLS Happy Eyeballs / 绕系统代理）
│   │   ├── apple_cms.py     # 苹果CMS (JSON API)
│   │   ├── feifei_cms.py    # 飞飞CMS (XML API)
│   │   └── haiyang_cms.py   # 海洋CMS (XML/JSON API)
│   └── parser/
│       ├── sniffer.py       # 媒体嗅探器
│       └── m3u8_filter.py   # M3U8 智能广告过滤
└── static/
    ├── index.html           # 前端主页面（Alpine.js）
    ├── player.html          # 弹出播放页（XGPlayer 竖滑）
    ├── logo.svg / logo.ico  # 前端 Logo
    ├── thumb.svg            # 卡片占位图
    ├── css/
    │   └── style.css        # 设计系统「纸上观影 / Paper & Reel」+ 工具类层
    ├── js/
    │   ├── api.js           # API 调用封装
    │   ├── app.js           # 主应用逻辑 (Alpine.js)
    │   ├── window-chrome.js # 无边框窗口拖拽 / 缩放 / Aero Snap
    │   └── alpine.min.js    # Alpine.js（本地内联依赖）
    └── vendor/              # 第三方前端库（XGPlayer / Swiper / HLS.js 等）
```

## API 路由

| 路由 | 说明 |
|---|---|
| `GET /` | 返回 index.html |
| `GET /static/<path>` | 静态文件 |
| `GET /api/hls?url=<url>` | 播放列表代理：后端拉取 + 智能去广告，并把内部所有 CDN 地址改写为同源代理；302 到 `.m3u8` 结尾地址供播放器识别为 HLS |
| `GET /api/media?url=<url>` | 媒体字节代理（切片 `.ts/.m4s`、密钥 `.key`、字幕 `.vtt` 等），转发 `Range` 请求支持拖动进度，同源返回规避跨域 |
| `GET /api/serve_m3u8/<sid>` | 返回已暂存的过滤后播放列表（`.m3u8` 结尾，供播放器识别为 HLS） |
| `GET /api/parse?url=<url>` | 媒体嗅探解析 |
| `GET /api/cms/classes?source=<url>` | 获取 CMS 分类 |
| `GET /api/cms/videos?source=<url>&ac=&pg=&t=&wd=` | 获取视频列表 |
| `GET /api/cms/detail?source=<url>&id=<id>` | 获取视频详情 |
| `GET /api/cms/check?source=<url>` | 检测 CMS 源连通性（设置中心「检测连接」调用） |
| `GET /api/gist/status` | Gist 同步状态（绑定/最近同步时间/错误，Token 只回掩码） |
| `POST /api/gist/configure` `{token}` | 校验 Token 并自动查找绑定已有同步 Gist |
| `POST /api/gist/upload` | 上传本地全部数据到 Gist（未绑定则自动查找/创建） |
| `POST /api/gist/pull` | 从 Gist 拉取并覆盖本地数据 |
| `POST /api/gist/unbind` / `clear` | 解除绑定 / 清除本地凭据 |
| `GET /api/update/status` · `POST /api/update/start` · `POST /api/update/apply` | 应用内更新：状态 / 下载 / 应用并重启 |
| `GET /player` | 弹出式竖滑播放页 |

## M3U8 智能去广告 + 同源代理

播放全程**只与本地 Flask 服务（127.0.0.1:19527）同源通信**，从根源规避 CDN 跨域失败；后端按 discontinuity 切段、归并正片源、剔除广告，并把所有 CDN 地址改写为同源代理。原理、流程图与相关路由见 **[M3U8 智能去广告 + 同源代理](doc/M3U8去广告与同源代理.md)**。

## 主题与风格

- 浅色 / 深色 / 跟随系统（设置中心 → 基础 → 主题）
- 九套视觉风格（设置中心 → 基础 → 主题风格），与明暗模式独立组合，由 `style.css` 中 `html[data-theme="..."]` 令牌覆盖实现
- 独立播放器页（`/player` 与弹出播放器窗口）固定夜间主题 + 默认视觉风格，不随主应用主题/风格切换；播放背景的封面 / 黑底模式仍可切换

## 许可证

MIT
*（本项目由 AI 编写、设计思路亦来自 AI；内容仅供学习交流参考，请勿用于任何商业或侵权行为。）*
