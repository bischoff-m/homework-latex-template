# 📜 Homework LaTeX Template

This template provides basic structure, a header and commonly used packages for writing
simple homework assignments in LaTeX.

↪ [Preview](Exercise1/main1.pdf)

## Usage

Enter your name and student ID in the `Preamble/preamble.tex` file. For each assignment,
copy the `main<N>.tex` file to a new folder. Add the `.vscode` folder to your `.gitignore`
file after cloning this repository or delete it if you are not using VS Code.


## VS Code as LaTeX editor

If you want to use VS Code as your LaTeX editor, here is my recommended setup.

### Install local LaTeX and Perl distribution

I use the following on Windows, but you can use any other distributions.

- [MiKTeX](https://miktex.org/download)
- [Strawberry Perl](http://strawberryperl.com/)

### Install VS Code extensions

> [!NOTE]
> The extensions are listed in the `.vscode/extensions.json` file, so VS Code should ask
> you to install them automatically.

The [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
extension is a must-have. It provides core features for editing and compiling LaTeX
documents. Check out the manual for a full list of features.

Also, I find the [Rewrap](https://marketplace.visualstudio.com/items?itemName=stkb.rewrap)
extension useful for formatting the text. You can use `Alt + Q` to make the text fit the
page width.

### Configure workspace settings

The page width is set using the `editor.rulers` setting in the `.vscode/settings.json`
file.

Most of the time, I also find it useful to enable the `editor.formatOnSave` setting. This
is nice for, e.g. `align` environments, where the LaTeX Workshop extension will align the
`&` characters like below. However, it depends on the text you are writing whether this
works well or not.

```latex
Before formatting:

\begin{flalign*}
    \Pr(yes) &= \norm{\braket{\phi_{yes}}{\psi}}^2 & first & \\
    &= \norm{\braket{\phi_{yes}}{a \phi_{yes} + b \phi_{no}}}^2 & second & \\
    &= \norm{a \cdot 1 + b \cdot 0}^2 & third & \\
    &= \norm{a}^2 & fourth & \\
\end{flalign*}
```

```latex
After formatting:

\begin{flalign*}
    \Pr(yes) & = \norm{\braket{\phi_{yes}}{\psi}}^2                       & first  & \\
             & = \norm{\braket{\phi_{yes}}{a \phi_{yes} + b \phi_{no}}}^2 & second & \\
             & = \norm{a \cdot 1 + b \cdot 0}^2                           & third  & \\
             & = \norm{a}^2                                               & fourth & \\
\end{flalign*}
```

### Remarks

The [Github Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
extension saved me a lot of time, no matter what kind of document I was writing. So if you
have access to it (students have via [GitHub Education](https://education.github.com/)),
definitely give it a try.
