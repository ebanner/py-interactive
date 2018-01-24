# PYNT (PYthon iNTeractive)

[![Built with Spacemacs](https://cdn.rawgit.com/syl20bnr/spacemacs/442d025779da2f62fc86c2082703697714db6514/assets/spacemacs-badge.svg)](http://spacemacs.org)

Jupyter notebooks for software engineers.

- [🎥 Feature Tour (YouTube)](http://www.youtube.com/watch?v=qqJbaoS_sH0 "pynt Demo")

![Demo](/img/demo.gif)

## Quick Start

```shell
git clone https://github.com/ebanner/pynt.git
echo '(load-file "~/pynt/pynt/pynt.el")' >> .emacs
emacs my-python-file.py
M-x pynt-mode RET
```

## What is pynt?

pynt is fundamentally a python to jupyter notebook (`.py` to `.ipynb`) converter.

pynt takes a python file and produces a jupyter notebook. The resulting jupyter notebook can be opened in a [jupyter notebook web browser client](#jupyter-notebook-web-browser-client) or within emacs with a [Emacs IPython Notebook client](https://github.com/ebanner/pynt/blob/dev/README.md#emacs-ipython-notebook-client).

In addition an emacs package called `pynt-mode` is included. `pynt-mode` provides an interface for invoking pynt as well as tooling for making the transition from code and jupyter notebook (and vice-versa) seamless (i.e. by scrolling jupyter cells with lines of code).

One way to think about pynt is it is a tool which produces a *dynamic* (or *live*) log. A dynamic log is in contrast to a *static* (or *dead*) log which you could produce by, say, inserting print statements between each line of your code. pynt does this automatically *without you having to modify the existing code*.

Yet another way to think about pynt is as a debugger. But rather than operating at one line at a time (as with traditional debuggers) you have access to *every line of code at all times*.

## What are pynt use cases?

pynt shines in the following two scenarios:

1. When you wish to acquaint/familiarize yourself with new code
2. When you wish to modify existing (familiar) code
3. When you wish to produce documentation of code

Regarding new code, a common workflow of mine is to paste the code into a jupyter notebook, split up each line of code into its own cell, and evaluate each cell to see the effect of each line of code. *This is exactly what pynt does*.

Regarding familiar (existing) code, pynt allows you to, say, modify an existing line of code, evaluate that line, and visually verify that it produces the desired data/output. This is in contrast to editing a line of code, invoking the code (i.e. by calling the surrounding function), and inspecting the output of the function.

Regarding producing documentation, since pynt mixes markdown with code and data, it can serve as a piece of documentation to hand off to someone so they can quickly get up to speed with how the code works.

## Prerequisites

- Emacs
- jupyter (python)
- EIN [[1]](http://millejoh.github.io/emacs-ipython-notebook/) and [[2]](https://github.com/millejoh/emacs-ipython-notebook)
- epc (python)

## Installation



## Using pynt

The first step is starting EIN just like you normally would. My workflow for that is the following.

1. Do `M-x pynt-mode RET` on a python file
2. Pop over to the jupyter notebook and cycle through the namespaces with the `<left>` and `<right>` arrow keys
3. Once you've decided on a namespace pop back over to the code and then hit `C-c C-e` or `M-x pynt-execute-current-namespace RET`
4. Optionally toggle `M-x pynt-scroll-mode RET` to make the generated notebook scroll with your point

## Inspirations and Related Projects

- [SLIME](https://common-lisp.net/project/slime/)
- [vim-slime](https://github.com/jpalardy/vim-slime)
- [EIN](http://millejoh.github.io/emacs-ipython-notebook/)
- [Bret Victor - Inventing on Principle (video)](https://vimeo.com/36579366)
    - [Tools to support live coding as in Bret Victor's “Inventing on Principle” talk](https://stackoverflow.com/questions/9448215/tools-to-support-live-coding-as-in-bret-victors-inventing-on-principle-talk)  (stack overflow)
- [Light Table - a new IDE concept](http://www.chris-granger.com/2012/04/12/light-table-a-new-ide-concept/)
    - [EmacsWiki: Light Table](https://www.emacswiki.org/emacs/LightTable)
    - [Video demonstration and commentary](https://www.youtube.com/watch?v=TgHvRcbYJ-8)
- [CppCon 2014: Mike Acton "Data-Oriented Design and C++"](https://www.youtube.com/watch?v=rX0ItVEVjHc)
- [GOTO 2016 • Pure Functional Programming in Excel • Felienne Hermans](https://www.youtube.com/watch?v=0yKf8TrLUOw)
- [Introduction to Investing and Finance - Lesson 1 by Martin Shkreli](https://www.youtube.com/watch?v=ARrNYyJEnFI&t=1379s)  (expert spreadsheet usage)
- [Bruce Hauman](http://rigsomelight.com/)
    - [Literate interactive coding: Devcards](https://www.youtube.com/watch?v=G7Z_g2fnEDg)
    - [Developing ClojureScript With Figwheel](https://www.youtube.com/watch?v=j-kj2qwJa_E)

## Screenshots

### Jupyter Notebook Web Browser Client

![Browser](/img/browser.png)

### Emacs IPython Notebook Client

![EIN](/img/ein.png)
