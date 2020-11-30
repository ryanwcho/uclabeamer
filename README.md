# UCLA Rmarkdown Beamer Template

<p float="center">
  <img src="https://user-images.githubusercontent.com/34947559/100639492-16baa980-32ea-11eb-8144-337fbecbfefb.png" width="400" />
  <img src="https://user-images.githubusercontent.com/34947559/100639502-18846d00-32ea-11eb-8a98-fcb94deac850.png" width="400" /> 
</p>

[Rmarkdown](https://rmarkdown.rstudio.com/) is a popular way for researchers to present their research in a number of different formats. One of the benefits for researchers is that Rmarkdown can help produce a wide array of documents, to include Beamer presentations.

This template was created by a need to have a simple and custom theme that I could use for presentations and the like. The template is based off the Madrid Beamer theme, and simply adds on a blue color scheme with a UCLA logo as the header and a transparent Bruin in the lower right corner. It's not much, but hopefully will save you some time. 

## Using the template

If you have any familiarity with Rmarkdown, the implementation should be fairly straightforward. However, a few things of note for this to work for you once downloaded.


### In the LaTex document

The LaTex document `beamer.tex` provides some additional information to help process the document. Nothing needs to be changed here except that you do need to specify your name and department. This is the way to produce the title page as shown above.

```latex
\author{First M. Last}
\institute{Department of X}
```

### In the Rmarkdown document

The results of the `template.Rmd` can be found in the `template.pdf` document to see how certain options and headers pan out. Most options are found in the YAML header:

```
title: Title
subtitle: Subtitle
output:
  beamer_presentation:
    keep_tex: true
    latex_engine: xelatex
    slide_level: 4 # Change this depending on which paragraphs you need
    include:
      in_header: "yourfilepath/beamer.tex"
  ```

The `title` and `subtitle` parts should be self explanatory. The only thing that you may wish to change is the `slide_level` which will provide different options on the levels of headers provided. Currently, the set up is:

```
# Navigation Bar Header (What's provided near the bubbles)
## Section Header (I typically keep this the same as the Level 1 header)
### Intermediate Title Page (I don't really use this option but it's provided for those who do)
#### Normal Slide
##### Text Box within the Page
```

I've also provided a number of different examples of types of slides you might want to incorporate in the document, such as pages with columns, or pages with emphasized bullet points. 

Using Rmarkdown, as many people know, is a huge result of trial and error. If you have any issues, I'm more than happy to assist!



***Disclaimer***: I do not own the rights to the images used in creation of this template. The use of such images are assumed to be used in accordance with UCLA Policy 110 as described [here](https://www.adminvc.ucla.edu/marks/request/name-seal-marks/campus-unit).
