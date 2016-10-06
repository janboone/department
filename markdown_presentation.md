% Introduction Markdown
% Jan Boone 
% Dept. of Economics, Tilburg University


Introduction
================

this lecture
------------

* in this part, we look at

    * markdown
    * [pandoc](http://pandoc.org/demos.html)
    * [atom](https://atom.io/)


Latex
=====

latex vs markdown
-----------------

* Latex is great!
* markdown does not compete with latex when writing a paper or PhD
  thesis
* however,

    * when writing a short note (say, assignment or referee report), latex is a bit heavy handed
    * latex is geared towards pdf; markdown is a lot more flexible,
      e.g. export to html
    * markdown to write your first notes (e.g. on a paper), then you
      convert to latex
	* creating presentations in latex is ... horrendous (and we don't
      want to talk about Office at all)
    * [jupyter notebooks](http://jupyter.org/) allow you to explain
      your code with markdown, results in something like [this](http://janboone.github.io/Deductible_Health_Insurance/)

Installation
============

what you need
-------------

* markdown: nothing
* pandoc: go to [pandoc website](http://pandoc.org/installing.html)
* an editor, e.g. [atom](https://atom.io/)

    * you can use editors like atom and emacs also for latex and lots
      of other things
    * please don't use Scientific Workplace (or any other 'wysiwyg'
      editor); it is easy at the start, but you will regret such a
      choice for the rest of your life ...


markdown
========

simple!
-------

* markdown allows you to create structure in a simple way
* much simpler than latex and more readable in source file
* especially when making presentations this is very useful

-------


* examples are:

```

    this is a heading
    =================

    subheading
    ----------

    or when doing a presentation:

    new slide
    ---------

    * first bullet
    * second bullet

    [link text](actual link, e.g. http://www.etc)

    ![Alt text for image](/path/to/img.jpg "Optional title")

```

* look on the web for other syntax like footnotes etc.
* google for "markdown tutorial" to find more details

-------

* math you type as in latex

```
* $x^2$, $\beta$, $\sqrt{9}$, $\frac{1}{2}$, $\bar x$

```

* This yields:

* $x^2, \beta, \sqrt{9}, \frac{1}{2}, \bar x$



pandoc
------

* this is where the magic happens
* you need to be able to work with shell/terminal/command prompt
  (which is useful for latex as well)
* with pandoc you can convert markdown files into many other file
  formats
* [pandoc website](http://pandoc.org/demos.html) contains examples of
  how to convert from one file format into another
* these commands can be quite elaborate

--------

* the command to turn the markdown version of this presentation into
  an html file is given by


```
pandoc -s --mathjax --slide-level 2 --toc --toc-depth=1 -t revealjs markdown_presentation.md -V theme=solarized -o markdown_presentation.html

```

* if you are really addicted to latex beamer, then do:

```

pandoc --slide-level 2 --toc --toc-depth=1 -t beamer markdown_presentation.md -V theme:Montpellier -o markdown_presentation.pdf

```

------


* have fun using pandoc!


<!--

How to turn this markdown file into a presentation:

pandoc -s --mathjax --slide-level 2 --toc --toc-depth=1 -t revealjs markdown_presentation.md -V theme=solarized -o markdown_presentation.html

pandoc --slide-level 2 --toc --toc-depth=1 -t beamer markdown_presentation.md -V theme:Montpellier -o markdown_presentation.pdf




new slide:

------------


-->
