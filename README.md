# OracleTools

Oracle Cloud 甲骨文云实例管理 Telegram 机器人，支持多账号、多区域管理，自动抢机、VNC 控制台、一键重装系统等功能。

## 功能特性

- **多账号管理**：支持同时管理多个 OCI 账号
- **自动抢机**：自动轮询创建 ARM/AMD 实例，支持多可用域切换
- **区域订阅**：支持为账号订阅新区域
- **VNC 控制台**：通过浏览器 noVNC 远程访问实例控制台
- **一键重装系统**：通过 VNC 控制台自动执行 netboot.xyz 安装 Debian，根据实例架构（ARM/AMD64）和所在大洲自动选择配置
- **实例管理**：查看实例详情、启动/停止/重启、删除实例、替换引导卷等
- **Cloudflare Tunnel**：自动建立公网隧道，无需公网 IP 即可访问控制台

## 下载

下载对应平台的程序：

| 平台 | 文件 |
|------|------|
| Linux amd64 | `OracleTools_linux_amd64_v1/OracleTools` |
| Linux arm64 | `OracleTools_linux_arm64/OracleTools` |
| Linux 386 | `OracleTools_linux_386/OracleTools` |
| Windows amd64 | `OracleTools_windows_amd64_v1/OracleTools.exe` |
| Windows arm64 | `OracleTools_windows_arm64/OracleTools.exe` |
| Windows 386 | `OracleTools_windows_386/OracleTools.exe` |
| macOS amd64 | `OracleTools_darwin_amd64_v1/OracleTools` |
| macOS arm64 | `OracleTools_darwin_arm64/OracleTools` |

## 使用方法

```bash
# Linux / macOS
./OracleTools --token="<Bot Token>" --chatid="<Admin Chat ID>"

# Windows
.\OracleTools.exe --token="<Bot Token>" --chatid="<Admin Chat ID>"
```

## 参数说明

| 参数 | 说明 |
|------|------|
| `--token` | Telegram 机器人 Token |
| `--chatid` | 管理员的 Telegram Chat ID |

## 获取参数

- **Bot Token**：在 Telegram 找 [@BotFather](https://t.me/BotFather) 创建机器人获取
- **Chat ID**：在 Telegram 找 [@myidbot](https://t.me/myidbot) 发送 `/getid` 获取

## OCI 配置文件

程序启动后会引导配置 OCI 账号，配置文件格式参考 [OCI SDK 配置文档](https://docs.oracle.com/en-us/iaas/Content/API/Concepts/sdkconfig.htm)。