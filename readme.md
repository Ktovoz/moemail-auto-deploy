# Moemail 自动化部署方案

## 功能概述

该解决方案提供了一个自动化部署 Moemail 的完整工具，包含以下功能：

- 提供全流程自动化部署 Moemail 的解决方案
- 新增工作流可构建并发布 Moemail 自动化部署执行文件
- 提供友好的自动化部署菜单，包含多种部署选项

## 部署选项

> **重要提醒**：在所有需要访问GitHub或Cloudflare的操作中，系统会提示您手动登录相应平台。登录完成后，请按回车键继续，程序将自动保存cookie并继续执行后续操作。您可以随时管理和删除这些cookie文件。

### 1. 全流程部署

一键完成所有部署步骤，自动执行以下所有操作。

### 2. 创建 GitHub App

自动创建并获取以下必要参数：

| 参数 | 说明 |
|------|------|
| **AUTH_GITHUB_ID** | GitHub App 的客户端 ID |
| **AUTH_GITHUB_SECRET** | GitHub App 的客户端密钥 |
| **AUTH_SECRET** | 认证加密密钥 |

### 3. 创建 Cloudflare 资源

自动在 Cloudflare 创建并获取以下必要资源和参数：

| 参数 | 说明 |
|------|------|
| **CLOUDFLARE_ACCOUNT_ID** | Cloudflare 账户 ID |
| **DATABASE_NAME** | D1 数据库名称 |
| **DATABASE_ID** | D1 数据库 ID |
| **KV_NAMESPACE_ID** | Cloudflare KV 命名空间 ID，用于存储网站配置 |

> **注意**：**CLOUDFLARE_API_TOKEN** 仍需手动生成，并在 `.env` 文件中填写：
> ```
> CLOUDFLARE_API_TOKEN = xxxxx
> ```

### 4. 自动部署

- 自动 fork 项目仓库
- 自动填入所有环境变量到 `.env` 文件
- 自动运行部署流程

## Cookie管理说明

所有自动化操作中保存的cookie信息仅用于完成部署流程，您可以随时管理和删除这些cookie文件。建议在部署完成后检查并清理不需要的cookie文件，以确保账户安全。
