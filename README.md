# covid-edu

This project uses [{drake}](https://github.com/ropensci/drake) to facilitate the reproducibility of the analysis.

To run the web-scraper, run either:

- the contents of [`R/make.R`](R/make.R)
- or `drake::r_make()`

All of the required packages are listed in [`R/packages.R`](R/packages.R).

There are two key parameters to set/modify in [`R/plan.R`](R/plan.R):

- `my_date` (defaults to today's date, but can be changed for use in certain cases, e.g. if the scraper fails and you want to maintain the same file structure (which includes the date))
- `search_term` a character vector with one or more search terms; used as a regular expression, so e.g. wildcards are supported