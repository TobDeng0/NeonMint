# **NeonMint 模板文档**

![neonmint](https://github.com/user-attachments/assets/ae539704-2292-492f-882c-c90595b34717)

## 🎯 概述

**NeonMint** 是一个极简现代风格的模板，专为开发者和数字创意工作者设计。它采用深色基调搭配薄荷绿色点缀，提供干净、优雅且功能性强的视觉体验，非常适合作品集、仪表盘或技术类落地页使用。

## 📁 项目结构

```bash
└── 📁NeonMint
    └── 📁public
        ├── android-chrome-192x192.png
        ├── android-chrome-512x512.png
        ├── apple-touch-icon.png
        ├── favicon-16x16.png
        ├── favicon-32x32.png
        ├── favicon.ico
        └── 📁images
            ├── 📁posts    # 文章图片
            └── 📁projects # 项目图片
        └── site.webmanifest # PWA 配置文件
    └── 📁src
        ├── 📁components  # 可复用的UI组件
        │   ├── 📁blog    # 博客组件
        │   ├── 📁layout  # 布局组件
        │   ├── 📁portfolio # 作品集组件
        │   └── 📁ui      # UI 组件
        ├── 📁icons       # 图标(.svg)
        ├── 📁layouts     # 网站布局
        │   ├── Layout.astro           # 主应用布局
        │   ├── MarkdownAbout.astro    # 关于页面布局
        │   ├── MarkdownPostLayout.astro # 文章页面布局
        │   └── ProjectLayout.astro    # 项目页面布局
        ├── 📁pages       # 网站页面
        │   ├── about-me.md            # 关于页面
        │   ├── 📁blog   # 所有文章页面
        │   │   ├── index.astro        # 博客首页
        │   │   ├── 📁posts            # 博客文章
        ├── │   ├── └── index.astro     # 所有文章页面
        │   │   ├── 📁tags             # 博客标签
        │   │   └── 📁techs            # 博客技术
        │   ├── index.astro            # 首页
        │   ├── 📁portfolio
        │   │   └── 📁projects         # 项目作品
        │   ├── robots.txt.ts          # robots.txt 配置
        │   └── rss.xml.js             # RSS 配置
        ├── 📁scripts
        │   └── menu.js                # 菜单脚本
        ├── 📁styles
        │   └── global.css             # 全局样式
        └── 📁utils
            └── languages.ts           # 技术工具配置
    ├── .gitignore
    ├── astro.config.mjs
    ├── package-lock.json
    ├── package.json
    ├── README.md
    └── tsconfig.json
```

## 🛠️ 技术栈

- **框架**: Astro v5.6.1
- **UI 库**: Preact v10.26.2
- **样式**: TailwindCSS v4.0.8
- **图标**: astro-icon v1.1.5
- **语法高亮**: PrismJS v1.30.0
- **动画**: tailwindcss-animated v2.0.0
- **分析统计**: @vercel/speed-insights v1.2.0

## ✨ 核心特性

1. **🚀 性能优化**
   - 静态网站生成
   - 使用 Preact 进行部分水合（hydration）
   - 图片与资源优化

2. **💻 现代开发体验**
   - 支持 TypeScript
   - 热模块替换
   - ESLint 集成

3. **🔍 SEO 与分析**
   - 内建站点地图生成
   - RSS 订阅支持
   - Vercel Speed Insights

4. **🎨 样式与UI**
   - 使用 TailwindCSS 进行实用优先的样式设计
   - 动画组件
   - 响应式设计
   - 支持暗黑模式

## 🚀 快速开始

1. **📦 安装**

   ### 🚀**通过 Astro 安装**
   ```bash
   npm create astro@latest -- --template EFEELE/neonmint
   ```
   或者  
   ### 🔧**手动安装**
   
   #### 克隆仓库
   ```bash
   git clone https://github.com/EFEELE/NeonMint.git
   ```
   #### 安装依赖
   ```bash
   npm install
   ```

3. **⚡ 开发模式**
   ```bash
   npm run dev
   ```

4. **🏗️ 构建**
   ```bash
   npm run build
   ```

5. **👀 预览**
   ```bash
   npm run preview
   ```

## ⚙️ 配置

该项目通过以下关键文件进行配置：

- `astro.config.mjs`: 主要的 Astro 配置文件
- `tailwind.config.js`: TailwindCSS 配置
- `tsconfig.json`: TypeScript 配置

## 🎨 自定义设置

### 📄 添加新页面

在 `src/pages` 目录中创建新的 `.astro` 文件。文件名将决定路由路径。

### 🔧 添加新语言或技术

要将新的编程语言或技术工具添加到站点胶囊中，请按照以下步骤操作：

1. **🖼️ 添加 SVG 图标**：将该语言或工具的 SVG 文件放置在 `src/icons` 文件夹中。

    > **💡 推荐**：对于 SVG 图标，我推荐使用 [SVGL](https://svgl.app/)，这是一个优秀的高质量矢量图库，为大多数流行语言和技术提供了优化的图标。

2. **📝 注册语言**：打开 `utils/languages.ts` 文件，并按如下格式在 `languages` 对象中添加新条目：

   ```typescript
   html: {
       name: "HTML 5",
       iconName: "html",
   },
   ```

   其中：
   - [html](file://c:\Users\34446\Desktop\TWOS%20HOME\index.html)：是该语言的唯一标识符
   - `name`：是在界面上可见显示的名称
   - `iconName`：是 SVG 文件的名称（不带扩展名），必须与 `src/icons` 中的文件名完全匹配

完成这些步骤后，新的语言或技术将在站点的胶囊中可用。在创建或编辑项目或文章时可以选择它，相应的图标将在界面中正确显示。

如果在此过程中遇到任何问题，请尝试重新启动开发服务器。某些情况下，配置文件或静态资源的更改需要重启才能被正确检测。

要在用户界面中验证新语言是否已正确添加，请在重启服务器后检查可用技术列表。

---

### 🧷 Favicon 设置

要自定义站点的 favicon 和网页应用图标，您可以使用 [favicon.io](https://favicon.io/favicon-converter/) 生成所有必要的变体。上传您的标志或图标，该工具将为您创建一套针对各种设备和平台优化的文件。

将生成的文件放置在 `📂 public` 目录下，如下所示：

```bash
📂 public
├── 📄 android-chrome-192x192.png
├── 📄 android-chrome-512x512.png
├── 📄 apple-touch-icon.png
├── 📄 favicon-16x16.png
├── 📄 favicon-32x32.png
├── 📄 favicon.ico
└── 📄 site.webmanifest
```

> 💡 不要忘记更新 `site.webmanifest` 的内容，以匹配您的应用名称、描述和主题颜色，以便获得完整的 PWA 体验。

---

### 🎨 样式设置

- 使用 TailwindCSS 类进行样式设置
- 在 `src/styles/global.css` 中添加自定义样式

### 🧩 组件

- 在 `src/components` 中创建可复用的组件
- 使用 `astro-icon` 导入图标

## 🚀 部署

该站点配置为部署在 Vercel 上，但也可以部署到任何静态托管服务上。

## 🤝 贡献指南

1. Fork 仓库
2. 创建功能分支
3. 提交更改
4. 推送到分支
5. 创建 Pull Request

## 📄 许可证

该项目采用 MIT 许可证 —— 详见 LICENSE 文件了解详细信息。