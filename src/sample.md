---
title: Presentation template
author: Ivan Trepakov
institute: University
---

# Пример слайда с кириллицей

## Теорема Пифагора

Основная формулировка содержит алгебраические действия ---
в прямоугольном треугольнике, длины катетов которого равны 
$a$ и $b$, а длина гипотенузы --- $c$, выполнено соотношение:
$$
a^2 + b^2 = c^2.
$$

## Пример программы

```{.python}
#$\ $Вычисление$\ $факториала$\ $числа$\ $n
def fact(n):
  if (n==1 or n==0):
    return 1
  else:
    return n * fact(n - 1)
```

# Sample slide

::: columns
:::: {.column width=48%}

```{=latex}
%% Set color of code formatting to CtpPeach in first column
\lstset{style=default,basicstyle={\ttfamily\color{CtpPeach}}}
```

## First column

- You can use all Markdown features and directly embed `\LaTeX`{=latex}
- `\uncover<2->{`{=latex} Beamer allows you to flexibly animate slides with `\uncover<X>` and `\only<X>` `}`{=latex}
- `\uncover<3->{`{=latex} For images it is better to use vector graphics, e.g. in `.svg` which is automatically converted into `.pdf` via `Makefile` magic `}`{=latex}
- `\uncover<4->{`{=latex} You can also use `.png` or `.jpg` but they usually look worse than `.svg`/`.pdf` `}`{=latex}
- `\uncover<5->{`{=latex} Or you can dive deep into Ti*k*Z `}`{=latex}
- `\uncover<6->{`{=latex} Links can also be embeded as QR codes into presentation with `\LaTeX }`{=latex}

::::
\vline
:::: {.column width=2%}
::::
:::: {.column width=48%}

## \centering Second column (centered)

```{=latex}
\only<1-2>{
```
- Markdown lists
- With beautiful math: $x^n + y^n = z^n$
- And *easy* **Markdown** `styles`
```{=latex}
}
```

```{=latex}
\only<3-4>{
\centering
\Begin{minipage}[c][.35\textheight][c]{.6\textwidth}
\Begin{mdframed}[backgroundcolor=maininverted,linecolor=maininverted]
```
![](images/sample/Markdown-mark.pdf)

<!-- Without minipage could be simply this:
![](images/sample/Markdown-mark.pdf){ width=60% }
-->
```{=latex}
\End{mdframed}
\End{minipage}
}
```

```{=latex}
\only<4>{
\centering
\Begin{minipage}[c][.35\textheight][c]{.6\textwidth}
\Begin{mdframed}[backgroundcolor=maininverted,linecolor=maininverted]
```
![](images/sample/Markdown-mark.svg.png)

<!-- Without minipage could be simply this:
![](images/sample/Markdown-mark.svg.png){ width=60% }
-->
```{=latex}
\End{mdframed}
\End{minipage}
}
```

```{=latex}
\only<5>{
\centering
\begin{tikzpicture}[every node/.style={text=black}]
  \begin{scope}[blend group = soft light]
    \fill[red!30!white]   ( 90:1.2) circle (2);
    \fill[green!30!white] (210:1.2) circle (2);
    \fill[blue!30!white]  (330:1.2) circle (2);
  \end{scope}
  \node at ( 90:2)    {Typography};
  \node at ( 210:2)   {Design};
  \node at ( 330:2)   {Coding};
  \node [font=\Large] {\LaTeX};
\end{tikzpicture}
}
```

```{=latex}
\only<6>{
\vspace{1em}
\centering
\qrcode[height=3cm]{https://texample.net/tikz/examples/}
\vspace{1em}
```
<https://texample.net/tikz/examples/>

```{=latex}
}
```


::::
:::

# Incremental code highlighting {.fragile}

::: columns
:::: column

```{=latex}
%% Set color of code formatting to CtpPeach in first column
\lstset{style=default,basicstyle={\ttfamily\color{CtpPeach}}}
```

## Beamer macros

- `\onslide<X>` macro can be used inside of code listings
  to provide custom animations
- `\setbeamercovered` macro controls how the elements are displayed
  when they are supposed to be hidden
- In this example `\setbeamercovered{transparent=40}` makes elements
  dimmed instead of being hidden completely

::::
:::: column

## Code sample

```{=latex}
\setbeamercovered{transparent=40}
```

```python
$\onslide<1        >$# Factorial example
$\onslide<1,2,6    >$def factorial(n):
$\onslide<1,3,4,7,8>$  if n < 2:
$\onslide<1,3,7,9  >$    return 1
$\onslide<1,3,4,7,8>$  else:
$\onslide<1,3,5,7  >$    return n * factorial(n-1)
```

::::
:::

# Conclusion

::: columns
:::: {.column width=10%}
::::
:::: {.column width=75%}

## \centering Summary

- Pandoc = Markdown + `\LaTeX`{=latex}
- Please use this template and never open ~~Google Slides~~ PowerPoint ever again

::::
:::: {.column width=10%}
::::
:::

# {.plain}

\vspace{.7\textheight}
\begin{beamercolorbox}[ht=4ex,dp=2ex,center]{title}
\large Thank you for your attention
\end{beamercolorbox}

