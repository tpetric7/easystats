# Reports download statistics for easystats packages

This function reports download statistics for `easystats` packages from
CRAN through the `cranlogs` package.

## Usage

``` r
easystats_downloads(from = "2019-02-26", sort_by = "total", length = 30)
```

## Arguments

- from:

  Starting date for the download statistics. Defaults to `"2019-02-26"`,
  which is when the first easystats package was released on CRAN.

- sort_by:

  Name of the column that should be used for sorting. Can be
  `"package"`, `"total"`, or `"monthly"`. Use `NULL` for no sorting.
  Defaults to `"total"` (total downloads).

- length:

  Numeric, maximum length of the returned string. If not `NULL`, will
  shorten the string to a maximum `length`, however, it will not
  truncate inside words. I.e. if the string length happens to be inside
  a word, this word is removed from the returned string, so the returned
  string has a *maximum* length of `length`, but might be shorter.

## Value

A data frame with three columns: package, total downloads, and average
monthly downloads.

## Examples

``` r
# \dontrun{
easystats_downloads()
#> Package     |      Total | Monthly
#> ----------------------------------
#> insight     | 10,207,050 | 120,083
#> datawizard  |  6,775,685 | 116,822
#> performance |  4,605,038 |  54,822
#> parameters  |  4,483,673 |  56,046
#> bayestestR  |  4,410,833 |  52,510
#> effectsize  |  3,331,788 |  43,270
#> correlation |  1,257,585 |  17,227
#> see         |  1,015,121 |  12,230
#> modelbased  |    736,004 |   9,813
#> report      |    374,154 |   6,236
#> easystats   |    165,605 |   3,764
#> Total       | 37,362,536 | 492,823
# }
```
