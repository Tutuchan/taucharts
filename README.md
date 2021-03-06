<!-- README.md is generated from README.Rmd. Please edit that file -->

taucharts is an R htmlwidget interface to the TauCharts javascript
library

Take a look at the [TODO
list](https://github.com/hrbrmstr/taucharts/issues/1) and chip in\!

Right now, you can make & customize (including manual color scales &
ordered factors + legends + tooltips + trendlines):

  - scatterplots
  - scatterplot matrices
  - line charts
  - bar charts (veritical, horizontal & stacked)

Composite plots are on the road map for support but not in the R package
yet.

Have a look [on RPubs](http://rpubs.com/hrbrmstr/taucharts) to see what
`taucharts` can do\!

The following functions are implemented:

  - `tauchart`: Create a new TauChart
  - `tau_line`: Create a TauCharts line chart
  - `tau_point`: Create a TauCharts scatterplot
  - `tau_bar`: Create a TauCharts bar chart (horizontal or vertical)
  - `tau_stacked_bar`: Create a TauCharts stacked bar chart (veritcal
    only)
  - `tau_guide_gridlines`: Control showing of axis gridlines
  - `tau_guide_padding`: Set overall chart padding
  - `tau_guide_x`: Control x-axis padding, label, scale & tick format
  - `tau_guide_y`: Control y-axis padding, label, scale & tick format
  - `tau_legend`: Add a TauCharts legend
  - `tau_tooltip`: Add a TauCharts tooltip
  - `tau_trendline`: Add a TauCharts trendline
  - `run_tau_app`: Run a built-in example Shiny app
  - `tau_tasks`: Add post-render JavaScript tasks to taucharts
  - `tau_add_css_rule`: Add a CSS rule to the rendered htmlwidget
  - `tau_set_font`: Set `font-family` for the chart
  - `as_tauchart`: Turn a simple (single-geom) ggplot plot into an
    tauchart object
  - `tau_title`: Add a title to the tauchart plot

with many color palette options:

  - `tau_color_manual`: Specify the colors used in the charts
  - `tau_color_brewer`: Use the ColorBrewer palette in the charts
  - `tau_color_economist`: Use the “Economist” palette used in the
    charts
  - `tau_color_few`: Use the “Few” palette used in the charts
  - `tau_color_highcharts`: Use the HighchartsJS palette used in the
    charts
  - `tau_color_manual`: Specify the colors used in the charts
  - `tau_color_tableau`: Use the Tableau palette in the charts
  - `tau_color_wsj`: Use the “Wall Street Journal” palette used in the
    charts

The following datasets are included:

  - `cars_data`: statistics on cars released from 1997 through 2013 (a
    data frame with 135 rows and 7 variables)

### News

  - Version 0.4.5 released : Shiny click events, color themes for
    faceted charts, updated TauCharts JS lib
  - Version 0.4.4.9000 released : `tau_title`
  - Version 0.4.3.9000 released : minor issue with guides
  - Version 0.4.2.9000 released : pre-CRAN flight check
  - Version 0.4.0.9000 released : added `as_tauchart` & updated
    TauCharts JS lib
  - Version 0.3.4.9000 released : added warning for global targeted CSS
    rules and font ref fix thx to @jlewis91
  - Version 0.3.3.9001 released : fix for custom colors and `tau_line`
  - Version 0.3.3 released : custom font for chart (`?tau_set_font`)
  - Version 0.3.2 released : custom colors working in legend &
    trendlines
  - Version 0.3.1 released : removed R 3.2.0 dependency (removed the
    dependent code)
  - Version 0.3.0 released : color palettes galore\!
  - Version 0.3.0.9000 released : `?tau_add_css_rule` (add CSS rules to
    a chart)
  - Version 0.2.6.9000 released : `?tau_tasks` (add JavaScript to a
    chart)
  - Version 0.2.5.9000 released : list & run example Shiny apps - see
    `?run_tau_app` for more info
  - Version 0.2.5.9000 released : stacked bar charts
  - Version 0.1.0 released : trendline, tooltips & dev fork (prod is
    pretty much stable & functional)
  - Version 0.0.1.9003 released : facet-based ordering + legends
  - Version 0.0.1.9000 released : auto-detects column classes, can add
    manual colors & faceted plots are now working (see the Rpub for an
    example)
  - Version 0.0.0.9000 released

### Installation

``` r
devtools::install_github("hrbrmstr/taucharts")
```

### Usage

``` r
library(taucharts)

# current verison
packageVersion("taucharts")
#> [1] '0.4.5'
```

### Test Results

``` r
library(testthat)
date()
#> [1] "Fri May 11 00:02:12 2018"

test_dir("tests/testthat", reporter = SummaryReporter)
#> basic functionality: S
#> 
#> ══ Skipped ════════════════════════════════════════════════════════════════════════════
#> 1. we can do something (@test-taucharts.R#2) - Empty test
#> 
#> ══ DONE ═══════════════════════════════════════════════════════════════════════════════
```

### Code of Conduct

Please note that this project is released with a [Contributor Code of
Conduct](CONDUCT.md). By participating in this project you agree to
abide by its terms.
