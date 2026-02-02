Lab 03 - Nobel laureates
================
Saima Arina
01/31/2026

### Load packages and data

``` r
library(tidyverse) 
```

``` r
nobel <- read_csv("data/nobel.csv")
```

## Exercises

Here is a link to the [lab
instructions](https://datascience4psych.github.io/DataScience4Psych/lab03.html).

### Exercise 1

``` r
nrow(nobel)
```

    ## [1] 935

``` r
ncol(nobel)
```

    ## [1] 26

There are 935 observations and there are 26 variables. Each row
represents a nobel lauterate individual.

### Exercise 2

``` r
nobel_living <- nobel %>% 
  select(firstname, surname, died_date, country, gender) %>% 
  filter(is.na(died_date)) %>% 
  filter(!is.na(country))
```

``` r
nobel %>% 
  count(is.na(died_date))
```

    ## # A tibble: 2 × 2
    ##   `is.na(died_date)`     n
    ##   <lgl>              <int>
    ## 1 FALSE                627
    ## 2 TRUE                 308

``` r
nobel %>% 
  count(!is.na(country))
```

    ## # A tibble: 2 × 2
    ##   `!is.na(country)`     n
    ##   <lgl>             <int>
    ## 1 FALSE               254
    ## 2 TRUE                681

``` r
nobel %>% 
  count(gender)
```

    ## # A tibble: 3 × 2
    ##   gender     n
    ##   <chr>  <int>
    ## 1 female    52
    ## 2 male     856
    ## 3 org       27

### Exercise 3

Remove this text, and add your answer for Exercise 1 here. Add code
chunks as needed. Don’t forget to label your code chunk. Do not use
spaces in code chunk labels.

### Exercise 4

…

### Exercise 5

…

### Exercise 6

…
