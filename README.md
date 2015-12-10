spenv
=====

[![Build Status](https://travis-ci.org/sckott/spenv.svg)](https://travis-ci.org/sckott/spenv)

`spenv` - add environmental data to spatial data

See the [Wiki](https://github.com/sckott/spenv/wiki) for some documentation.

Package API:

* `sp_mutate` - get env data for occ data input
* `sp_query` - query for env data
* `find_locs` - find locations/stations/etc. based on occ data input - internal fxn used in `sp_mutate`

## Install


```r
devtools::install_github("ropensci/spenv")
```


```r
library("spenv")
```

## Examples


```r
file <- system.file("examples", "obis_mola_mola.csv", package = "spenv")
dat <- read.csv(file)
head(dat)
```


```r
res <- sp_mutate(x = dat[1:10,], radius = 100)
res[[1]]
```

## Meta

* Please [report any issues or bugs](https://github.com/sckott/spenv/issues).
* License: MIT
