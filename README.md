# What is LaTeX?

LaTeX is a document preparation system. When writing, the writer uses plain text as opposed to formatted text, as in WYSIWYG word processors like Microsoft Word or LibreOffice Writer. The writer uses markup tagging conventions to define the general structure of a document (such as article, book, and letter), to stylize text throughout a document (such as bold and italic), and to add citations and cross-references. A TeX distribution such as TeX Live or MikTeX is used to produce an output file (such as PDF or DVI) suitable for printing or digital distribution.

> [wikipedia.org/wiki/LaTeX](https://en.wikipedia.org/wiki/LaTeX)

![logo](https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/LaTeX_logo.svg/100px-LaTeX_logo.svg.png)

# How to use this image

## Run a single TexLive script

To compile your LaTeX work use Docker image directly:

```bash
$ docker run -it --rm --name latexmk --net=none -v "$PWD":/data sigan/latex latexmk -pdf -pdflatex="pdflatex %O %S" your_super_latex_file
```

You can use any other latex commands if you know how.

Also, you can copy scripts from `bin/` folder to you `/usr/local/bin` on the system. So, for example, jupyter-notebook will work.

### Notes

The image assumes that your latex files, styles, and extra files are located in some directory and you run script described above from this location.

# For users

This repo is fork of [sigan/latex](https://github.com/senior-sigan/docker-latex). Repo dyakov/latex adds only new verion of Ubuntu and enables installation of new packages in [install.sh](https://github.com/senior-sigan/docker-latex/blob/master/src/install.sh) using `tlmgr`. All issues you can leave in [source repo](https://github.com/senior-sigan/docker-latex/issues).
