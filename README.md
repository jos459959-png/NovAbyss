# Novabyss 官网部署指南

## 文件结构

确保你的 GitHub 仓库包含以下文件：

```
├── index.html          # 主入口文件
├── assets/             # CSS 和 JS 文件
│   ├── index-xxx.js    # JavaScript 文件
│   └── index-xxx.css   # CSS 样式文件
├── images/             # 图片资源
│   ├── hero-bg-hd.png      # 首页背景图
│   ├── logo-new.png        # Logo
│   ├── manifesto-tools-new.png  # 第二页图片
│   ├── product-filter.jpg  # 产品图1
│   ├── product-led.jpg     # 产品图2
│   ├── product-tools.jpg   # 产品图3
│   ├── product-tester.jpg  # 产品图4
│   └── youtube-thumb.jpg   # 视频缩略图
└── README.md           # 本文件
```

## 部署步骤

### 1. 上传到 GitHub

1. 在 GitHub 创建一个新仓库（如 `NovAbyss`）
2. 将所有文件上传到仓库根目录
3. 确保文件结构如上所示

### 2. 连接 Vercel

1. 登录 [Vercel](https://vercel.com)
2. 点击 "Add New Project"
3. 导入你的 GitHub 仓库
4. **重要**：Framework Preset 选择 **"Other"**（不要选任何框架）
5. 直接点击 Deploy

### 3. 白屏问题排查

如果部署后出现白屏，请检查：

1. **文件名必须完全匹配** `index.html` 中的引用
2. `assets` 文件夹中的 JS/CSS 文件名必须与 `index.html` 中的一致
3. 所有图片必须在 `images` 文件夹中

### 4. 添加 Favicon（浏览器标签图标）

1. 准备一个 32x32 像素的 PNG 图标
2. 命名为 `favicon.png`
3. 放入 `images` 文件夹
4. 在 `index.html` 的 `<head>` 中添加：
   ```html
   <link rel="icon" type="image/png" href="./images/favicon.png" />
   ```

## 常见问题

**Q: 为什么部署后是白屏？**
A: 最常见原因是：
- JS/CSS 文件名不匹配（每次构建会生成新的 hash 名）
- 文件路径错误
- 文件没有正确上传到 GitHub

**Q: 如何更新网站内容？**
A: 修改代码后重新构建，将新的 `dist` 文件夹内容上传到 GitHub

## 技术栈

- React + TypeScript
- Tailwind CSS
- Framer Motion

## 品牌配色

- 背景色：`#0A1628`（深海蓝）
- 强调色：`#2D9C9C`（荧光青）
- 文字色：`#F3F4F6`（白色）

---

© 2025 Novabyss. All rights reserved.
