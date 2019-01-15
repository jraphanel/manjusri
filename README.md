---
title: Thus Spake Manjusri
date: 2018-12-21
hero: oṃ arapacana dhīḥ
---

# Thus Spake Manjusri

This site is a collection of my personal notes on:

* High Performance Computing
* Machine Learning
* CyberInfrastructure

It is powered by the excellent static site generator [MkDocs](http://mkdocs.org) and the beautiful [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

## Conda Environment

Anaconda is my preferred Python distribution. However, *MkDocs* is not available as a [conda package](https://conda.io/docs/user-guide/tasks/manage-pkgs.html) from the default channels.

First create a new *conda* environment named `manjusri`:

```console
$ conda create -n manjusri pip
```

Create the root folder for the MkDocs project:

```console
$ mkdir ~/manjusri
$ cd ~/manjusri
```

Create a requirement file (`requirements.txt`) containing a list of packages to be installed using [pip](https://pip.pypa.io/en/stable/user_guide/):

```txt
mkdocs>=1.0
mkdocs-material>=3.0
Pygments>=2.2
pymdown-extensions>=5.0
htmlmin
```

Activate the `manjusri` environment:

```console
$ source activate manjusri
```

Install the required packages (and its dependencies):

```console
$pip install -r requirements.txt
```

## MkDocs Command

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

After running `mkdocs build`, a static web site will be generated in the subfolder `site`. We can then deploy the site to a web server, or serve it locally with:

```console
$ python -m http.server
```
