
--- 
title: "R for Data Analysis and Visualization"
subtitle: |
  | ECON 396 (Fall 2017)
  | TR 10:30-11:45, DURP Computer Lab (first floor Saunders)
author: "Jonathan Page"
date: "2017-11-12"
site: bookdown::bookdown_site
output: 
  bookdown::gitbook:
    config:
      toc:
        collapse: section
    highlight: kate
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
github-repo: jonpage/r-course
description: "This is a course on using R focused on data analysis and visualization through case studies."
---

# Syllabus {-}

## Office Hours {-}
Monday 2-3 PM and Tuesday 3-4 PM, or by appointment, Saunders 509, jrpage at hawaii dot edu.

## Student Learning Objectives {-}

1. To be familiar with standard techniques for visualizing data, including heat maps, contour plots, etc.
2. To be able to transform raw data into formats suitable for analysis
3. To be able to perform basic exploratory analysis
4. To be able to create data visualizations in R

There is no prerequisite for this course.

## Resources {-}

### Required {-}

Introductory Statistics with Randomization and Simulation: Available as a free PDF (https://www.openintro.org/stat/textbook.php?stat_book=isrs) or for $8.49 on Amazon.

### Recommended: {-}

[R Graphics Cookbook](https://www.cookbook-r.com/Graphs)

[RStudio Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)

## Course Requirements {-}

Grades for this course will be based on weekly assignments (30%), project assignments (30%), the project proposal (5%), the final project deliverable (20%), and final project presentation participation (15%).

### Weekly assignments (30%) {-}

Weekly assignments are short R excercises. Each exercise should take no longer than 15 minutes. You will typically be given time to complete the exercise in class the day the assignment is given. The assignment will be in the form of R Markdown file (*.Rmd). You will submit the completed assignments via [classroom.google.com](https//classroom.google.com) by the following class period. 

## Individual Project {-}

### Project assignments (30%) {-}

Each week, leading up to the project proposal, you will be given an assignment that is designed to provide you with an organized workflow for approaching new data science projects. Project assignments are submitted via [classroom.google.com](https//classroom.google.com), with the exception of the two presentations

### Project proposal presentation (5%) {-}

This presentation should be less than 2 minutes. You simply need to communicate the core question your project seeks to answer and the dataset(s) you will be using to answer this question.

### Final project (20%) {-}

The final project will be an R Markdown document which communicates your project question, the data you used, and your results. You will need to deliver both your R Markdown file and any necessary data for running the file.

### Final project presentation participation (15%) {-}

Your final project participation grade is based on a combination of your own presentation and the feedback you provide to your classmates.

## Schedule {-}

The following schedule is tentative and subject to change. Typically, the Tuesday class will consist of the week's
R lecture. Depending on how quickly we get through the material, you will have time to work on your assignment that
will be due before the following class period. On Thursdays, we will discuss a relevant topic, but you should have
time to work on your project assignment for the week. That assignment will generally be due before the following class
period, except for the last several weeks when you are completing your final project.

### Week 1 {-}

* **R** [Intro to R and RStudio; Histograms, scatterplots, summary statistics](#intro)
    * **Data** R Sample Datasets
* **Topic** [Data sources overview](#data-sources)
* **Project Assignment** Indentify interesting datasets (include links to datasets) and questions

### Week 2 {-}

* **R** [read_csv, dplyr basics, heatmaps, hexbins](#read-data)
    * **Data** ACS PUMS *[CSV]*
* **Topic** [Anscombe's Quartet](#anscombe)
* **Project Assignment** Choose question and dataset (with link to your source) for your project

### Week 3 {-}

* **R** [ggplot facets, bubble plots, transparency](#facets-and-bubbles)
    * **Data** Hawaii Tourism Authority *[Excel]*
* **Topic** [Probability](#probability)
* **Project Assignment** Write description of your question

### Week 4 {-}

* **R** [geom_smooth, abline, vline, hline](#lines)
    * **Data** State of Hawaii Department of Business, Economic Development (DBEDT) *[Excel]*
* **Topic** [Distributions](#distributions)
* **Project Assignment** Write description of your dataset(s)

### Week 5 {-}

* **R** [ggplot2 Extensions and Scatterplot Matrices (GGally)](#ggplot-exts)
    * **Data** ACS Immigration *[CSV]*
* **Topic** [JunkCharts Trifecta Checkup](#trifecta)
* **Project Assignment** Create 2 descriptive plots of your datasets(s)

### Week 6 {-}

* **R** [Boxplots, violin plots](#boxplots-and-violins)
    * **Data** SSA *[Excel]*
* **Topic** [Intro to Inference](#inference)
* **Project Assignment** Write a description of the data cleaning required for your project

### Week 7 {-}

* **R** [Spatial Visualizations with geom_spoke, gganimate, and GGally::glyphs](#geom_spoke)
    * **Data** NOAA Wind *[netCDF]*
* **Topic** [Confidence Interval](#confidence-intervals)
* **Project Assignment** Write a description of your planned approach

### Week 8 {-}

* **R** [geom_area, geom_ribbon](#area-and-ribbons)
    * **Data** BLS American Time Use Survey (ATUS) *[TSV]*
* **Topic** Project Proposal Description
* **Project Assignment** Work on project proposal presentation

### Week 9 {-}

* **R** [jitter, rug, aesthetics](#jitter-rug)
    * **Data** PSID *[SPS, TXT (Fixed-Width)]*
* **Topic** Present project proposal (<2 Minutes)

### Week 10 {-}

* **R** [Themes, Labels, and Colors](#themes-labels-colors)
    * **Data** Zillow Age of Real Estate Inventory Data *[CSV]*
* **Topic** [Inference for Numerical Data](#inference-numerical)
* **Project Assignment** Work on final project

### Week 11 {-}

* **R** [Polar Coordinates](#polar)
    * **Data** University of Michigan - Survey of Consumers *[CSV]*
* **Topic** [Inference for Categorical Data](#inference-categorical)
* **Project Assignment** Work on final project (cont.)

### Week 12 {-}

* **R** [Text Analysis (Natural Language Processing)](#nlp)
    * **Data** Twitter *[twitteR API]*
* **Topic** [Linear Regression](#linear-regression)
* **Project Assignment** Work on final project (cont.)

### Week 13 {-}

* **R** [networks, geomnet extension](#networks)
    * **Data** UN Comtrade *[CSV]*
<!-- -->
* **Topic** [Multiple Regression](#multiple-regression)
* **Project Assignment** Work on final project (cont.)

### Week 14 {-}

* **R** [Log Scales](#log)
    * **Data** IRS Statistics of Income *[CSV]*
* **Topic** [Putting your work online]()
* **Project Assignment** Work on final project (cont.)

### Week 15 {-}

* **R** [Cross-Section Modeling](#cross-section)
    * **Data** NSF National Survey of College Graduates *[DAT (Fixed-Width)]*
* **R** [Time-Series Modeling](#time-series)

### Week 16 {-}

* Final Project presentations

## Other Resources {-}

There are many useful resources you should be aware of while going through this course.
I will attempt to keep this list updated as I become aware of more useful links:

[RStudio's List of Useful R Packages](https://github.com/rstudio/RStartHere)

[Visual Tutorial on Histograms](http://tinlizzie.org/histograms/)

### Statistics {-}

[Variance Explained](http://varianceexplained.org/RData/resources/)

[R for Data Science - Grolemund and Wickham](http://r4ds.had.co.nz/)

### Visualization {-}

[FlowingData](http://flowingdata.com/)

[Junk Charts](http://junkcharts.typepad.com/)

[Catalog of Visualization Types by Ferdio](http://datavizproject.com/)

### Courses {-}

[Gary King - Quantitative Research Methodology](http://projects.iq.harvard.edu/gov2001/)

[John Stasko - Information Visualization](http://www.cc.gatech.edu/~stasko/7450/)

[Jenny Bryan - Data wrangling, exploration, and analysis with R](http://stat545.com/)

[HarvardX Biomedical Data Science Open Online Training](https://rafalab.github.io/pages/harvardx.html)

### Books {-}

[Econometrics in R](https://cran.r-project.org/doc/contrib/Farnsworth-EconometricsInR.pdf)

[Using R for Data Analysis and Graphics](ftp://cran.r-project.org/pub/R/doc/contrib/usingR.pdf)

### Papers {-}

[Embedded Plots](http://vita.had.co.nz/papers/embedded-plots.pdf)


# Weekly Assignments {-}

## Creating the R Markdown files {-}

Weekly assignments are R Markdown files. To begin each assignment, create a new 
R Markdown file. By either

* Use the `File` menu, under the `New File` selection, click on `R Markdown...`, or
* Click on the new file button, then click on `R Markdown...`

In the dialog box, set the title to match the heading for the assignment. For example,

"Assignment 1.3"

Remember to use your name in the space for an author. When saving set the filename to the 
assignment followed by your first and last name, using dashes as separators. For example, if your 
name is John Snow, you would save Assignment 1.3 as `assignment-1-3-John-Snow`

## Submitting your assignment {-}

After you have completed the assignment and before the start of the next class period,
submit your R Markdown file on [classroom.google.com](https//classroom.google.com).


# Individual Project {-}

## Project assignments {-}

Each week, leading up to the project proposal, you will be given an assignment that is designed to provide you with an organized workflow for approaching new data science projects. Project assignments are submitted via [classroom.google.com](https//classroom.google.com), with the exception of the two presentations

## Project proposal presentation {-}

This presentation should be less than 2 minutes. You simply need to communicate the core question your project seeks to answer and the dataset(s) you will be using to answer this question.

## Final project RMarkdown {-}

The final project will be an R Markdown document which communicates your project question, the data you used, and your results. 

## Final project presentation participation {-}

Your final project participation grade is based on a combination of your own presentation and the feedback you provide to your classmates.

# Final Project Rubric {-}

The final project deliverable is worth 20% of your final grade. The following is a break down of
how your final project will be graded.

## Section: Introduction (10%) {-}

Your introduction should clearly state the research question(s) addressed by your 
project. The goal for this section is to make your reader interested in the topic
of your project.

## Section: Data (10%) {-}

The data section should clearly indicate where/how to access the data you used in
your project so that any reader could replicate your analysis. 

## Section: Analysis and Results (30%) {-}

This section should present the main figures/tables that answer your research question.

## Section: Conclusion (10%) {-}

The conclusion should provide a summary of your findings and a discussion of the next
steps that you (or someone else interest in your topic) could take to explore your
question further.

## General: Organization (10%) {-}

You should use headings (begin a line with `#` in R Markdown) to indicate separate sections.
The narrative of your project should be easy to follow.

## General: Grammar (10%) {-}

Your project should be free from spelling and grammatical mistakes. Place your text in Word if 
you need assistance, or have someone else proofread your project.

## General: Code (20%) {-}

All of your R chunks should be well organized and easy to follow. The key here is that all your
code should work. With the data you described in your data section, I should be able to run your
R Markdown without getting any errors.
