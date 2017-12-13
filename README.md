## Ocean Health Index Toolbox Training materials

These materials are available as a book at http://ohi-science.org/toolbox-training. 

Please clone or download https://github.com/OHI-Science/toolbox-demo to accompany this training.

To render this book: `bookdown::render_book("index.Rmd", "bookdown::gitbook")`

Many thanks to the creators of `bookdown`: 

- Yihui Xie (2016). bookdown: Authoring Books and Technical Documents with R Markdown. R package version 0.3.9.
- Yihui Xie (2016). bookdown: Authoring Books and Technical Documents with R Markdown. Chapman and Hall/CRC. ISBN 978-1138700109

## Publishing with the `/docs` folder

Here is how to publish this book using the docs/ folder instead of the current [_deploy.r](https://github.com/OHI-Science/toolbox-training/blob/f4f017ff8d2099aa9f0dda03223b945477a778bd/_deploy.r).  

**In RStudio**:  

1. in the root directory of your book, create a folder called `docs` (all lowercase)
1. in `_bookdown.yml`, add a line that says `output_dir: "docs"`
1. check your `.Rproj` file (may have to open a separate text editor for this. Make sure that lines ~12 on say: 

    ```
    RnwWeave: knitr
    LaTeX: pdfLaTeX

    AutoAppendNewline: Yes
    StripTrailingWhitespace: Yes

    BuildType: Website
    ```
1. Quit RStudio. When you reopen, your "Build" tab in the top right pane should have a button that says "Build Book"
1. Build your book by clicking the button or in the console: `rmarkdown::render_site(encoding = 'UTF-8')`
1. Delete the `_book` folder if it exists
1. Commit and push

**On GitHub.com**

1. Go to your repo > Settings
1. Scroll down to GitHub Pages
1. Change "Source" to "master branch /docs folder", click "save"


