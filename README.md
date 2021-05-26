# Overleaf-Compatible Undergraduate Thesis Template (Tongji Univ.)

**NOTE**

* Please select `main.tex` as the main file and compile it with `XeLaTeX` (suggested) or `LuaLaTex`.
* Till May 26th, 2021, our "great"🙄 `1.tongji.edu` is not able to support uploading `.pdf` files (but only MS Word files). 

## Compile it locally on Mac (on LaTeX-Workshop)

```shell
# Install BasicTex: https://mirrors.chevalier.io/CTAN/systems/mac/mactex/mactex-basictex-20210325.pkg
sudo tlmgr update --self

sudo tlmgr install texliveonfly
sudo tlmgr install latexmk
sudo tlmgr install adjustbox
sudo tlmgr install tcolorbox
sudo tlmgr install collectbox
sudo tlmgr install ucs
sudo tlmgr install environ
sudo tlmgr install titling
sudo tlmgr install enumitem
sudo tlmgr install rsfs
sudo tlmgr install tocloft
sudo tlmgr install xcolor
sudo tlmgr install trimspaces
sudo tlmgr install zhnumber
sudo tlmgr install ctex
sudo tlmgr install needspace
sudo tlmgr install xecjk
sudo  tlmgr install subfigure 
sudo  tlmgr install cases 
sudo  tlmgr install algorithms 
sudo  tlmgr install multirow

sudo tlmgr update --self --all
```

### XeLaTeX

Add the following attribute to your `setting.json`:

```json
"latex-workshop.latex.recipe.default": "latexmk (xelatex)",
"latex-workshop.latex.tools": [
    {
        "name": "xelatexmk",
        "command": "latexmk",
        "args": [
            "-xelatex",
            "-aux-directory=_out",
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "-shell-escape",
            "%DOC%"
        ]
    }
],
"latex-workshop.latex.recipes": [
    {
        "name": "latexmk (xelatex)",
        "tools": [
            "xelatexmk"
        ]
    }
]
```

## Call for contribution

- Create a `.sty` file regarding the project.

---

## LICENSE

We follow WTFPLv3.1 as our license. 

## Credit

Initial template provided by Yukuan HU, maintained/promoted by Ganler.
