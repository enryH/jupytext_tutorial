# Jupytext - sync notebooks as simpler text files

> Jupyter Notebooks in Jupyter Lab, VSCode, GitHub, Papermill and Jupytext - a good ensemble - a scientific use case

[![Start Tutorial](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/enryH/jupytext_tutorial/master?urlpath=lab/tree/tutorial)

Have a look at the [tutorial instructions](tutorial/README.md) (should be visible in jupyter lab)

## Outline

- [link to slides](https://docs.google.com/presentation/d/1bdL4F9JorxOK6vk9ZhNRqIzQiAoI5sdc1qoEGrdmqXo/edit?usp=sharing)


1. Link Jupyter Notebook with percentage script
2. Motivate different representations of files
    - Refactoring vs sharing outputs
    - Life exploration of object attributes (or methods) when working with data
    - different notebook view in VSCode
    - two views, two kernels, two states
3. Jupyter notebooks
    - JupyterLab and Jupyter ([jupyter-notebook-interface](https://docs.jupyter.org/en/latest/projects/architecture/content-architecture.html#the-jupyter-notebook-interface))
4. Run notebook in VSCode and JupyterLab
5. Use Papermill and paramterize tutorial script

## Setup

- uses jupyter-vscode-proxy, based on [vscode-binder](https://github.com/betatim/vscode-binder)

Start in repository folder: Explore [![Binder setup](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/betatim/vscode-binder/master?urlpath=lab)

## Topic

[`jupytext`](https://github.com/mwouts/jupytext) is a lightweight tool to keep scripts either as notebooks (`.ipynb`) or simpler text based file formats, such as markdown files (`.md`)  which can be easily rendered on GitHub or python files  (`.py`) which can be executed in VSCode’s interactive shell and are better for version control. Some tools still need `ipynb` to work, e.g. `[papermill](https://papermill.readthedocs.io/en/latest/)`. Therefore it is handy to keep different version of a script in sync. Otherwise one can also only use python files and render these as notebook in e.g. jupyter lab. Especially if the code is only kept for version control, but executed versions are keep in a project folder using a workflow environment (as `snakemake` or `nextflow`) this comes in handy. I’ll intend to give you an overview over my stack and practices working in life sciences. Hopefully you learn some interesting tools and more about the possibilities around jupyter, which can be compared to quarto or rmarkdown. 

Why do I use more than one file version for the same document? 

- jupyter kernels allow live exploration of attributes
- jupyter lab has a great scratch cell for exploration, while keeping the general structure of a notebook
- VSCode is great for applying changes in many places (”refactoring”)
- VSCode allows the search over many files

## Papermill

- needs `ipynb` → if you work from `*.py` files, you can use [jupytext cli](https://jupytext.readthedocs.io/en/latest/using-cli.html)
