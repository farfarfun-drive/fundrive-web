# fundrive-web

占位仓库，规划中的 Web 界面形态的 fundrive，当前还没有任何功能代码。建库只是先把名字和
位置占下来，等 fundrive 产品线需要浏览器端界面时在这里开工。

## 规划中的职责

为 [fundrive](https://github.com/farfarfun-drive/fundrive) 的统一网盘接口提供浏览器端的
文件管理界面。按组织内 `submodule-workspace-governance` 的约定，`-web` 结尾的仓库属于
service 形态，其运行时服务要同时做两件事：在自己的 base path 下托管构建好的静态资源，
并把所有后端路径（`/api/**` 以及 `/healthz` 等）反向代理到
[fundrive-api](https://github.com/farfarfun-drive/fundrive-api) 的地址。

## 当前状态

- 仓库里只有这份 README：没有前端源码，也没有 `package.json`。
- npm / PyPI 上都没有 `fundrive-web` 包，没有可安装或可部署的产物。
- [fundrive-dev](https://github.com/farfarfun-drive/fundrive-dev) 的 `scripts/setup.sh` 里
  留了注释说明将来要接入这类带进程的 app，但还没有把本仓库纳入子模块。

## 安装与替代方案

本仓库暂无可运行产物。现在要操作网盘，用命令行形态的核心包：

```bash
pip install fundrive
```

各网盘驱动按需单独安装，例如阿里云盘：

```bash
pip install fundrive-alipan
```

蓝奏云另有一个已经可用的 PyQt6 桌面客户端，需要图形界面可以先用它：

```bash
git clone https://github.com/farfarfun-drive/funlanzou.git
```

想一次拉齐整条产品线做跨包联调：

```bash
git clone --recurse-submodules https://github.com/farfarfun-drive/fundrive-dev.git
cd fundrive-dev
```

## 关于组织

[farfarfun-drive](https://github.com/farfarfun-drive) 是 farfarfun 旗下专注网盘 / 云存储
方向的组织，围绕 fundrive 这套统一接口维护主框架、各网盘驱动包、子模块编排仓库和桌面
客户端。本仓库是这条产品线为 Web 界面形态预留的位置，尚未进入开发。

- 🏠 组织主页：<https://github.com/farfarfun-drive>
- 🏠 上级组织：<https://github.com/farfarfun>
- 📧 联系：farfarfun@qq.com

本项目基于 [MIT](LICENSE) 协议开源。
