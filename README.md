# TRB_LaTeX_tex

A LaTeX template for Transportation Research Board Annual Meeting papers.

This TRB LaTeX template is a R Markdown template that enables users to write 
TRB papers using R, Sweave, and LaTeX.  A Lite (TeX-only) version of this template 
can be found https://github.com/chiehrosswang/TRB_LaTeX_tex.

More instruction and details about the project can be found inside the
``trb_template.rnw``. 

Perl is necessary for ``\totaltexcount`` to work and needs a Perl interpreter e.g. [ActivePerl](http://www.activestate.com/activeperl/downloads).

For R-Studio users using Sweave and .rnw ﬁles, you may enable shell escape command in 
the Global Options > Sweave settings

# Making Document
To make this document from source in a Unix-like OS, issue the following commands:

``R CMD SWEAVE 'trb_template.rnw

pdflatex --shell-escape trb_template.tex

bibtex trb_template

pdflatex --shell-escape trb_template.tex

pdflatex --shell-escape trb_template.tex``

The --shell-escape option is required to access the command line for the word count.
