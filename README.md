# CodeC IDE

**一个面向算法竞赛的轻量级 C++ 集成开发环境**

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-lightgrey.svg)
![License](https://img.shields.io/badge/license-Proprietary-red.svg)
![Qt](https://img.shields.io/badge/Qt-6.12-41CD52.svg)

---

## 联系方式 & ADs

作者联系邮箱：mr_magnet@outlook.com / 3625099190@qq.com

洛谷团队：https://www.luogu.com.cn/team/135002

---

## 概述

CodeC IDE 是一款专为算法竞赛（OI / ACM-ICPC / Codeforces 等）设计的轻量级 C++ 集成开发环境。本项目旨在解决传统 IDE 在竞赛场景下的若干痛点：启动缓慢、界面冗余、编译器配置繁琐、测试流程不连贯……。

CodeC 采用 **C++17 + Qt 6 Widgets** 构建，编辑器核心基于 **QScintilla**，内置 **MinGW-w64 GCC** 工具链，安装后即可使用，无需额外配置环境。

---

## 特性

### 1. 极简启动

基于原生 Qt Widgets 构建，不依赖 Electron 或 Chromium。冷启动时间通常在 1 秒以内，内存占用低，适用于竞赛环境下的快速响应需求。

### 2. 内置编译器

安装包内置 MinGW-w64 GCC 工具链，用户无需单独安装或配置编译器，亦不依赖系统 `PATH` 环境变量。

### 3. 一键自测

支持打开包含 `.in` / `.out` 测试数据的题目文件夹，自动扫描所有测试点并批量运行。测试结果以卡片形式展示，涵盖 AC / WA / TLE / MLE / RE 等状态，并附带时间与内存占用信息。

### 4. 自动处理 freopen

在编译并测试时，程序会自动识别并注释源代码中的 `freopen` 语句，使用重定向方式注入测试数据。**原始源文件不会被修改。**

### 5. Markdown 题目面板

内置 Markdown 题目面板，支持实时渲染，并集成 LaTeX 公式解析（`$...$` 与 `$$...$$`），便于在编写代码的同时查阅题目。

### 6. 多标签编辑

支持多标签页并行编辑，每个标签维护独立的撤销栈，适用于同时处理多道题目的场景。

### 7. 主题系统

提供浅色（蓝白科技风）与深色两套主题，基于 QSS 实现。用户亦可自行修改或添加主题文件。

---

## 系统要求

| 项目 | 要求 |
|------|------|
| 操作系统 | Windows 10 / 11（64 位） |
| 磁盘空间 | 约 200 MB |
| 内存 | 建议 4 GB 以上 |
| 依赖 | 无（安装包已内置运行库与编译器） |

---

## 安装

1. 前往 [Releases](https://github.com/MrMagnets/CodeC-IDE/releases) 页面，下载最新版本的 `CodeC_Setup_v1.0.0.exe`。
2. 双击运行安装程序，按向导完成安装。
3. 安装完成后，可通过桌面快捷方式或开始菜单启动 CodeC IDE。

> **说明**：若 Windows 弹出 SmartScreen 警告，请点击「更多信息」→「仍要运行」。此为 Windows 对未经数字签名的应用程序的默认安全策略，不影响程序本身的安全性。

---

## 快速上手

### 编写与运行

1. 启动 CodeC IDE。
2. 在编辑区编写 C++ 代码。
3. 按 `F5` 编译并运行，或按 `F9` 仅编译。

### 自测流程

1. 准备一个题目文件夹，结构如下：

```text
problem/
├── 1.in
├── 1.out
├── 2.in
├── 2.out
└── ...
```

2. 点击工具栏「打开自测」，选择该文件夹。
3. 按 `Ctrl+F9` 编译并测试。
4. 在「测试结果」面板中查看各测试点的运行状态。

### 导入题目

1. 点击工具栏「导入题目」，选择 `.md` 格式的题目文件。
2. 右侧题目面板将显示渲染后的内容，支持 LaTeX 公式。

---

## 快捷键

| 快捷键 | 功能 |
|--------|------|
| `F5` | 编译并运行 |
| `F9` | 编译 |
| `Ctrl+F9` | 编译并测试 |
| `Ctrl+T` | 打开自测文件夹 |
| `Ctrl+N` | 新建文件 |
| `Ctrl+O` | 打开文件 |
| `Ctrl+S` | 保存 |
| `Ctrl+Shift+S` | 另存为 |
| `Ctrl+W` | 关闭当前标签页 |
| `Ctrl+/` | 注释 / 取消注释 |
| `Ctrl+Shift+T` | 切换主题 |
| `Ctrl+,` | 打开设置 |
| `F11` | 全屏 |

---

## 反馈

如在使用过程中遇到问题，或希望提出功能建议，欢迎通过 [Issues](https://github.com/MrMagnets/CodeC-IDE/issues) 反馈。

---

## 许可

Copyright (C) 2026 Magnet. All rights reserved.

本软件为**专有软件（Proprietary Software）**，采用**保留所有权利（All Rights Reserved）** 的授权模式。

**由于本软件为暂时不进行开源，开源后本部分作废。**

**允许**：
- 在个人学习、教学、算法竞赛等非商业场景下**免费使用**本软件。
- 在保留完整版权声明的前提下，**完整、原样地分发**本软件的安装包。

**禁止**：
- 对本软件进行**反编译、反汇编、修改**或**衍生**。
- 将本软件或其衍生作品用于**商业用途**（包括但不限于销售、租赁、嵌入商业产品）。
- 移除或修改本软件中的**版权声明**、**商标**或其他**所有权标记**。
- 将本软件的安装包**重新打包**后分发，或以其他方式**暗示您是本软件的作者**。

**源代码**：本软件的源代码**未公开**。未经版权所有者明确书面许可，任何人不得获取、复制、修改或分发源代码。

**免责声明**：本软件按“现状”提供，不附带任何明示或暗示的保证。使用本软件所产生的任何后果，由用户自行承担。

如需商业授权或其他许可，请通过上方邮箱联系作者。

---

## 致谢

本项目基于以下开源项目构建，谨向相关作者与社区致以谢意：

- [Qt](https://www.qt.io/)
- [QScintilla](https://riverbankcomputing.com/software/qscintilla/)
- [MinGW-w64](https://www.mingw-w64.org/)

---

**CodeC IDE** · 竞赛选手自己做给自己用的极简 C++ IDE

Copyright (C) 2026 Magnet. All rights reserved.
