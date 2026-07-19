# 预设备忘录

世界书与预设互转、备忘录、变量检查等工具。

## 安装

### 前提

请先安装 [酒馆助手 (JS-Slash-Runner)](https://github.com/n0vi028/JS-Slash-Runner)，版本 **4.8.19+**。

### 扩展管理器安装（推荐）

1. SillyTavern → **扩展** → **Install Extension**
2. 粘贴：`https://github.com/Nancyindaeyo/PresetWorldBookTransfer`
3. 刷新页面 → 启用 **预设备忘录**

扩展会自动在酒馆助手中注册脚本「预设备忘录」（去脚本化内测中可改为扩展直载，见下方维护说明）。

### 手动 CDN（不推荐）

```javascript
import 'https://cdn.jsdelivr.net/gh/Nancyindaeyo/PresetWorldBookTransfer@main/index.js'
```

可能产生双实例，无扩展 lifecycle 清理。

## 使用

- 预设管理器底部：书签图标
- 扩展菜单：**预设备忘录**

## 本仓库文件说明

| 文件 | 说明 |
| --- | --- |
| `manifest.json` | SillyTavern 扩展清单 |
| `bootstrap.js` | 扩展入口、生命周期 hooks |
| `index.js` | 打包后的功能 bundle |
| `README.md` | 本文件 |

源码与维护文档在 monorepo 的 `src/预设备忘录-ext/`、`docs/preset-memo/`，**不会**被 ST 执行。

## 卸载

在扩展列表删除「预设备忘录」→ 自动移除脚本树条目并清理 DOM。

## 更新

面板内可检测 GitHub 更新；也可在扩展列表手动更新。发版前维护者需 `pnpm build:preset-memo` 并提交本目录的 `index.js`。

## 维护

开发者文档见 monorepo **`docs/preset-memo/`**（迁移计划、架构、验收清单）。
