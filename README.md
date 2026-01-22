# SUSTech Beamer 模板

南方科技大学 (Southern University of Science and Technology) LaTeX Beamer 演示文稿模板。

## 📸 预览

模板采用南科大官方 VI 配色：
- 🟠 南科大橙 RGB(237, 108, 0)
- 🟢 南科大墨绿 RGB(0, 63, 67)
- 🔵 南科大天青 RGB(43, 183, 179)

## 📁 文件结构

```
├── sustech_beamer.tex    # 主文档（在此编辑你的内容）
├── SUSTech.sty           # 主题样式文件
├── lib/
│   └── logo/             # Logo 文件夹
│       ├── 校徽.png
│       ├── 火炬+英文校名-上下.png
│       ├── 院徽+中英文-左右英文一行-彩色.png
│       └── ...
└── README.md
```

## 🚀 快速开始

### 1. 编译环境

- **编译器**：XeLaTeX（必须，用于支持中文）
- **推荐工具**：
  - VS Code + LaTeX Workshop 插件
  - TeXstudio
  - Overleaf（在线）

### 2. 编译方法

使用 XeLaTeX 编译 `sustech_beamer.tex`：

```bash
xelatex sustech_beamer.tex
```

或在 VS Code 中使用 LaTeX Workshop 插件，选择 `XeLaTeX` 编译方案。

### 3. 修改内容

打开 `sustech_beamer.tex`，修改以下信息：

```latex
\author{你的名字}
\title{你的标题}
\subtitle{副标题（可选）}
\institute{南方科技大学 \\ 你的院系 \\ 你的身份}
\date{日期}
```

### 4. 更换 Logo

修改 `\SustechLogo` 和 `\BgLogoPath` 变量：

```latex
% 标题页底部的 Logo
\newcommand{\SustechLogo}{lib/logo/院徽+中英文-左右英文一行-彩色.png}

% 背景水印 Logo
\newcommand{\BgLogoPath}{lib/logo/校徽.png}
```

可用的 Logo 文件：
- `校徽.png` - 校徽图案
- `火炬+英文校名-上下.png` - 火炬 + 英文校名（上下排列）
- `院徽+中英文-左右英文一行-彩色.png` - 院徽 + 中英文（左右排列，彩色）
- `院徽中英文+校徽图案-左右-彩色.png` - 院徽中英文 + 校徽图案（彩色）
- `院徽中英文+校徽图案-左右-黑白.png` - 院徽中英文 + 校徽图案（黑白）

### 5. 调整背景水印

背景水印参数可在 `sustech_beamer.tex` 中调整：

```latex
\newcommand{\BgLogoOpacity}{0.06}    % 透明度 (0-1，越小越淡)
\newcommand{\BgLogoScale}{0.9}       % 缩放比例
\newcommand{\BgLogoXShift}{6.0cm}    % 水平位移（正值向右，负值向左）
\newcommand{\BgLogoYShift}{-0.5cm}   % 垂直位移（正值向上，负值向下）
```

## 📝 使用示例

### 添加新的幻灯片

```latex
\begin{frame}{幻灯片标题}
    你的内容
\end{frame}
```

### 添加列表

```latex
\begin{frame}{列表示例}
    \begin{itemize}
        \item 第一项
        \item 第二项
        \item 第三项
    \end{itemize}
\end{frame}
```

### 添加图片

```latex
\begin{frame}{图片示例}
    \begin{figure}
        \centering
        \includegraphics[width=0.5\textwidth]{图片路径}
        \caption{图片标题}
    \end{figure}
\end{frame}
```

### 添加公式

```latex
\begin{frame}{公式示例}
    \begin{equation}
        E = mc^2
    \end{equation}
\end{frame}
```

### 分栏布局

```latex
\begin{frame}{分栏示例}
    \begin{columns}
        \begin{column}{0.5\textwidth}
            左侧内容
        \end{column}
        \begin{column}{0.5\textwidth}
            右侧内容
        \end{column}
    \end{columns}
\end{frame}
```

## ⚙️ 自定义样式

如需修改主题样式，请编辑 `SUSTech.sty` 文件：

- **修改颜色**：搜索 `\xdefinecolor` 或 `\setbeamercolor`
- **修改字体**：搜索 `\setCJKmainfont`
- **修改页脚**：搜索 `\setbeamertemplate{footline}`

## 📋 依赖包

模板依赖以下 LaTeX 包：
- `ctex` - 中文支持
- `tikz` - 绘图（用于背景水印）
- `hyperref` - 超链接
- `graphicx` - 图片插入
- `amsmath` - 数学公式
- `booktabs` - 表格美化
- `listings` - 代码高亮

## 🙏 致谢

本模板基于 [THU Beamer Theme](https://github.com/Trinkle23897/THU-Beamer-Theme) 修改而来，感谢原作者的贡献。

## 📄 许可证

MIT License
