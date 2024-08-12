
<!-- README.md is generated from README.Rmd. Please edit that file -->

# delaunator1

<!-- badges: start -->
<!-- badges: end -->

The goal of delaunator1 is to …

## Installation

You can install the development version of delaunator1 like so:

``` r
# FILL THIS IN! HOW CAN PEOPLE INSTALL YOUR DEV PACKAGE?
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(delaunator1)
delaunator1:::delaunator1(matrix(rnorm(6), ncol = 2))
#> [1] 1 0 2
```

If you are following along this is unstable and will change, but here’s
how the elements are oriented (for now).

``` r
xy <- matrix(rnorm(1024), ncol = 2)
#xy <- do.call(cbind, maps::map(plot = TRUE)[1:2])
## transpose in, for now
i <- delaunator1:::delaunator1(t(xy)) + 1
plot(xy, asp = 1)
polygon(xy[t(cbind(matrix(i, ncol = 3, byrow = TRUE), NA)), ])
```

<img src="man/figures/README-orientation-1.png" width="100%" />