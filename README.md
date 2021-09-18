# Single cell RNA-seq analysis workshop

## Overview

This workshop is a shorten version of SingleCellWorkshop from Yunshun Chen, and more details can be found [here](https://yunshun.github.io/SingleCellWorkshop/articles/SingleCellWorkshop.html).

In this workshop, you will learn how to analyse single-cell RNA-seq count data using Seurat and ternary plot. This workshop uses one epithelium sample of human normal mammary gland, which can be obtained from the 10X Genomics dataset (GSE161529) of [Pal et al. 2021. EMBO J.](https://doi.org/10.15252/embj.2020107333).

## Pre-requisites

The course is aimed at PhD students, Master's students, and third & fourth year undergraduate students.
Some basic R knowledge is assumed - this is not an introduction to R course.
If you are not familiar with the R statistical programming language it is compulsory that you work through an introductory R course before you attend this workshop

## _R_ packages used

The following R packages will be used:

* Seurat
* edgeR
* vcd
* scales
* pheatmap


## Time outline

| Activity                         | Time |
|----------------------------------|------|
| Introduction & setup             | 10m  |
| Part 1. Standard analysis        | 35m  |
| Part 2. Ternary plot analysis    |  5m  |
| Q & A                            | 10m  |


## Workshop goals and objectives

### Learning goals

 - Learn the standard scRNA-seq analysis pipeline.
 - Learn the ternary plot analysis for scRNA-seq data

### Learning objectives

 - Perform standard analysis of a single 10X scRNA-seq sample.
 - Perform ternary plot analysis of a single 10X scRNA-seq sample

## Workshop package installation

### Guide
This is necessary in order to reproduce the code shown in the workshop.
The workshop is designed for R `4.1` and can be installed using one of the two ways below.

### Via Docker image

If you're familiar with [Docker](https://docs.docker.com/get-docker/) you could use the Docker image which has all the software pre-configured to the correct versions.

```sh
docker run -e PASSWORD=abc -p 8787:8787 jinmingcheng/scrnaseqworkshop
```

Once running, navigate to <http://localhost:8787/> and then login with
`Username:rstudio` and `Password:abc`.

You should see the Rmarkdown file with all the workshop code which you can run.


### Via GitHub

Alternatively, you could install the workshop using the commands below in R `4.1`.

```
install.packages('remotes')

# Install workshop package
remotes::install_github("jinming-cheng/scRNAseqWorkshop", build_vignettes = TRUE)

# To view vignettes
library(scRNAseqWorkshop)
browseVignettes("scRNAseqWorkshop")
```
