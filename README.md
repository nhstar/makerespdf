# makerespdf
Turns a markdown version of a resume into a reasonable PDF file.

This requires Pandoc and Weasyprint

I've only done on Debian, but it should work on any system that supports bash/pandoc/weasyprint.

## Usage:
```
makeres -c ./style.css -o resume.pdf -k -d resume-sample.md
```
-c  declare location of style-sheet for intermediate processing\
*Default location for the style.css files is $HOME/.config/makeres/style.css*

-o  Name of the output file.  Defaults to name of input, changing extension to pdf

-k  Keep the intermediate HTML file produced by pandoc and used by weasyprint.  Useful for debugging output issues. 

-d  debug.  Some extra troubleshooting messaging.

***Docx version coming soon.***

## Author's note
I put the following in the top of my markdown to generate a title.

```
---
title: "John Smith"
---
```

This allows me to have an appropriate title on the output pdf file instead of just repeating the name of the file.  I then use the css to hide it so that it will format my name without duplicating the title.  It was quick and dirty, but does the trick.
