# FLRW Metric: Derivation and Empirical Validation of the Cosmological Scale Factor

This repository contains the source code, computational routines, and manuscript files for the analytical derivation of the kinematics of the universe's expansion based on the Friedmann-Lemaître-Robertson-Walker (FLRW) metric. It also includes the empirical validation of the model using extragalactic redshift and distance data.

## Project Overview

By imposing space-time homogeneity and isotropy (the Cosmological Principle), this project defines the Cosmological Tensor as the covariant derivative of the Riemann tensor ($K^\alpha_{\beta\gamma\mu\nu} := R^\alpha_{\beta\gamma\mu;\nu}$) and sets it to zero ($K^\alpha_{\beta\gamma\mu\nu} = 0$). This fundamental constraint allows for the deduction of the system of exact differential equations governing the evolution of the scale factor $a(t)$. A predictive model correlating proper distance and redshift is then formulated and tested using a weighted nonlinear least squares (NLS) regression analysis.

### Key Features:
* **Tensor Calculus & General Relativity:** Derivation of the Riemann Tensor, Ricci Tensor, Einstein Tensor, and Cosmological Tensor based on the FLRW metric.
* **Empirical Validation:** Data extraction and processing from the NASA/IPAC Extragalactic Database (NED).
* **Statistical Modeling:** NLS regression to estimate the spatial curvature $k$ and the expansion parameter $X^2$, including 95% statistical confidence intervals.
* **Reproducible Research:** Fully integrated R Markdown environment for data processing, statistical fitting, and automated typesetting of the final scientific manuscript.

## Repository Structure

* `FLRW Metric.Rmd`: The core R Markdown file containing the theoretical derivations (LaTeX), data scraping/cleaning routines, statistical models, and plotting scripts.
* `FLRW-Metric.pdf`: The compiled, publication-ready scientific manuscript.
* `Literature.bib`: The BibTeX file containing all the theoretical, mathematical, and software references used in the manuscript.
* `.gitignore`: Git configuration file specifying intentionally untracked files.

## Prerequisites and Dependencies

To compile the `.Rmd` file and reproduce the results, you will need the following software and libraries:

* **R** (A Language and Environment for Statistical Computing)
* **LaTeX** distribution (e.g., TeX Live, MiKTeX, or TinyTeX) for rendering the PDF.

**Required R Packages:**
```r
install.packages(c("dplyr", "rvest", "lubridate", "ggplot2", "knitr", "rmarkdown"))
```

## How to Reproduce

1. Clone this repository to your local machine:
```bash
git clone https://github.com/LUCHER4321/flrw-metric.git
```
2. Open the project in RStudio (or your preferred R environment).
3. Ensure all required packages are installed.
4. Open `FLRW Metric.Rmd` and click **"Knit to PDF"** (or run `rmarkdown::render("FLRW Metric.Rmd")` in the console). This will execute all data fetching, statistical calculations, and generate a fresh PDF of the manuscript.

## Data Availability

The extragalactic distances and recession velocities were extracted from the **NASA/IPAC Extragalactic Database (NED)**, which is operated by the Jet Propulsion Laboratory, California Institute of Technology, under contract with the National Aeronautics and Space Administration (NASA).
