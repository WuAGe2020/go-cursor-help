# 🚀 Cursor Free Trial Reset Tool

<div align="center">

[![Release](https://img.shields.io/github/v/release/yuaotian/go-cursor-help?style=flat-square&logo=github&color=blue)](https://github.com/yuaotian/go-cursor-help/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square&logo=bookstack)](https://github.com/yuaotian/go-cursor-help/blob/main/LICENSE)
[![Stars](https://img.shields.io/github/stars/yuaotian/go-cursor-help?style=flat-square&logo=github)](https://github.com/yuaotian/go-cursor-help/stargazers)

[English](#-english) | [中文](#-chinese)

<img src="https://ai-cursor.com/wp-content/uploads/2024/09/logo-cursor-ai-png.webp" alt="Cursor Logo" width="120"/>

</div>


# 🌏 Chinese

### 📝 问题描述

当看到以下提示时重置Cursor试用期：

```
Too many free trial accounts used on this machine.
Please upgrade to pro. We have this limit in place
to prevent abuse. Please let us know if you believe
this is a mistake.
```

### 💻 系统支持

**Windows** ✅ x64  
**macOS** ✅ Intel和M系列  
**Linux** ✅ x64和ARM64

### 📥 安装方法

#### 自动安装（推荐）

**Linux/macOS**
```bash
curl -fsSL https://raw.githubusercontent.com/yuaotian/go-cursor-help/master/scripts/install.sh | sudo bash
```

**Windows** (以管理员身份运行PowerShell)
```powershell
irm https://raw.githubusercontent.com/yuaotian/go-cursor-help/master/scripts/install.ps1 | iex
```

安装脚本会自动：
- 请求必要的权限（sudo/管理员）
- 关闭所有运行中的Cursor实例
- 备份现有配置
- 安装工具
- 添加到系统PATH
- 清理临时文件

#### 手动安装

1. 从[发布页面](https://github.com/yuaotian/go-cursor-help/releases)下载适合您系统的最新版本
2. 解压并以管理员/root权限运行：
   ```bash
   # Linux/macOS
   chmod +x ./cursor_id_modifier_*    # 添加执行权限
   sudo ./cursor_id_modifier_*

   # Windows (PowerShell 管理员)
   .\cursor_id_modifier_*.exe
   ```

#### 手动配置方法

1. 完全关闭 Cursor
2. 找到配置文件位置：
   - Windows: `%APPDATA%\Cursor\User\globalStorage\storage.json`
   - macOS: `~/Library/Application Support/Cursor/User/globalStorage/storage.json`
   - Linux: `~/.config/Cursor/User/globalStorage/storage.json`
3. 备份 `storage.json`
4. 编辑 `storage.json` 并更新以下字段（使用新的随机UUID）：
   ```json
   {
     "telemetry.machineId": "生成新的uuid",
     "telemetry.macMachineId": "生成新的uuid",
     "telemetry.devDeviceId": "生成新的uuid",
     "telemetry.sqmId": "生成新的uuid",
     "lastModified": "2024-01-01T00:00:00.000Z",
     "version": "1.0.1"
   }
   ```
5. 保存文件并重启 Cursor

### 🔧 技术细节

#### 配置文件
程序修改Cursor的`storage.json`配置文件，位于：
- Windows: `%APPDATA%\Cursor\User\globalStorage\`
- macOS: `~/Library/Application Support/Cursor/User/globalStorage/`
- Linux: `~/.config/Cursor/User/globalStorage/`

#### 修改字段
工具会生成新的唯一标识符：
- `telemetry.machineId`
- `telemetry.macMachineId`
- `telemetry.devDeviceId`
- `telemetry.sqmId`

#### 安全特性
- 自动备份现有配置
- 安全的进程终止
- 原子文件操作
- 错误处理和回滚

## 🔔 关注公众号
#### 获取更多精彩内容
- 第一时间获取最新版本更新
- CursorAI使用技巧和最佳实践
- 利用AI提升编程效率
- 更多AI工具和开发资源

![微信公众号二维码](img/wx_public_2.png)

## ⭐ Star History or Repobeats

[![Star History Chart](https://api.star-history.com/svg?repos=yuaotian/go-cursor-help&type=Date)](https://star-history.com/#yuaotian/go-cursor-help&Date)


![Repobeats analytics image](https://repobeats.axiom.co/api/embed/ddaa9df9a94b0029ec3fad399e1c1c4e75755477.svg "Repobeats analytics image")


## 📄 License

MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

