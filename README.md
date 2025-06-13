# ieeeconf-template

Template with my references for IEEE conferences with double column

## Revise Utils

Revise box:

```tex
\begin{revisebox}{3.2} % {1}为审稿意见编号
···
\end{revisebox}
```

Revise highlight:

```tex
\revise{3.2}{text}
```

### Problem shooting

#### Package soul Error: Reconstruction failed

在使用 LaTeX 的 soul 宏包进行文本高亮时，可能会遇到 "Package soul Error: Reconstruction failed" 错误。这通常是由于 \hl 命令处理特殊字符、数学模式或跨行文本时的限制所导致。

示例问题

```tex
\documentclass{article}
\usepackage{soul}
\begin{document}
\hl{This is a \cite{example} test.} % 会导致错误
\end{document}
```

解决方法

1. 使用 \protect 命令保护特殊字符

当高亮内容中包含如 \cite 等命令时，可以通过 \protect 来避免错误。

示例：

```tex
\documentclass{article}
\usepackage{soul}
\begin{document}
\hl{This is a \protect\cite{example} test.} % 正常工作
\end{document}
```
