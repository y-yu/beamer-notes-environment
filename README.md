`notes`: Beamer environment like `\note` command
=================================

![example image](https://y-yu.github.io/beamer-notes-environment/beamer_notes_environment.png)

See also an [example PDF file](https://github.com/y-yu/beamer-notes-environment/blob/master/beamer_notes_environment.pdf). This PDF file was created by [Overleaf](https://www.overleaf.com/).

## How to Use

```tex
\usepackage{xsavebox}

\newenvironment{notes}
  {%
    \begin{xlrbox}{NotesBox}
    \begin{minipage}{\textwidth}
    \begin{itemize}
    \setlength{\itemindent}{0em}
  }{%
    \end{itemize}
    \end{minipage}
    \end{xlrbox}
    \note{\theNotesBox}}

\begin{document}

\begin{frame}{Example Slide}
  Something you need.

  \begin{notes}
    \item This is a pen
    
    \item I like it
  \end{notes}
\end{frame}

\end{document}
```

See also an [exaple TeX file](https://github.com/y-yu/beamer-notes-environment/blob/master/beamer_notes_environment.tex).
