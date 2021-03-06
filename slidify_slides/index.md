---
title       : Web A/B Testing Simple Sample Size Calculator
subtitle    : Coursera Developing Data Products Peer Assignment
author      : hajozaki
job         : Coursera Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Overview
* Objective
    * Provide GUI of `power.prop.test` in R as simple sample size calculator for non-tech digital marketer who has responsible Web A/B Testing exmeriments
* Business Notice
    * Digital Marketer use MDE(delta) either absolute or relative depend on  company or situation
    * They must be able to choose MDE type on App
* Technical Notice
    * It use core feature of Shiny: `reactivity` for choosing MDE type 

GO to [My Shiny App for PA](https://hajozaki.shinyapps.io/csr_ddp_pa)  
GO to [My Github Repo for PA](https://github.com/hajozaki/csr_devdataprod_pa)  


--- .class #id 

## Problem - If you should support Digital Maketer
* They often do not know the statistics
* They often can not use any statistics software
* They often hate typing on CUI/CLI

*IF They have strong skill for debate and politics... :,(*


--- .class #id 

## Solution - Shiniy GUI App
* Easy to use for Digital Maketer - input only three items
* Easy to suport for us - same as `power.prop.test` in R
* It use core feature of Shiny: `reactivity` for choosing MDE type(`input$mde_type`)

<div style='text-align: center;'>
    <img height='375' width='606'
        src='./assets/img/screenshot01.png' alt='Annotated ScreenShot'/>
</div>

[Web A/B Testing Simple Sample Size Calculator on shiniyapps.io](https://hajozaki.shinyapps.io/csr_ddp_pa)


--- .class #id 

## Sample Size calculation in R
* Previous Slide's Screen Shot(Default Parameters) same as below the code in R

```r
base_cvr <- .06; var_cvr <- base_cvr + .01 ;sig_level <- .05; pwr_level <- .8
ceiling(power.prop.test(
    p1 = base_cvr, p2 = var_cvr, sig.level = sig_level, power = pwr_level)$n)
```

```
## [1] 9540
```
</br>
### Thank you for your evaluation!
I deploied `showcase` mode and MIT License. Feel free try to examine, use, and customize it for your user.

* [Github repo](https://github.com/hajozaki/csr_devdataprod_pa)

Any Quiestion? Please mension at [Twitter](https://twitter.com/hajozaki).

