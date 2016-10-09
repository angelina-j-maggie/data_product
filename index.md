---
title       : Building a data product
subtitle    : How likely are you to offend?
author      : angelina.j.maggie
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## How likely are you to offend?

In order to assess this question, the Proven Reoffending Statistics, which was released in July 2016 by the Ministry of Justice, GB. The data set used was the CSV format of data tools, found at this link:

https://www.gov.uk/government/statistics/proven-reoffending-statistics-october-2013-to-september-2014

The dataset contains a breakdown of the offending and reoffending data in the period October 2013 to September 2014 by the following characteristics:

1. Age
2. Area
3. Gender

--- .class #id 

## How likely are you to offend?

The dataset was cleaned to contain only the breakdown by area, age and gender.

Then the population of each area of England and Wales in 2014 was obtained from the Office for National Statistics (ONS) Annual Mid-year Population Estimates. These can be found at the following link:

http://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/bulletins/annualmidyearpopulationestimates/2015-06-25


<!-- html table generated in R 3.3.1 by xtable 1.8-2 package -->
<!-- Sun Oct  9 11:00:25 2016 -->
<table border=1>
<tr> <th>  </th> <th> Region </th> <th> Population Estimate </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> North East </td> <td> 8,100,00 </td> </tr>
  <tr> <td align="right"> 2 </td> <td> North West </td> <td> 7,800,000 </td> </tr>
  <tr> <td align="right"> 3 </td> <td> South East </td> <td> 18,700,000 </td> </tr>
  <tr> <td align="right"> 4 </td> <td> South West </td> <td> 14,500,000 </td> </tr>
  <tr> <td align="right"> 5 </td> <td> London </td> <td> 9,100,000 </td> </tr>
   </table>

--- .class #id 

## How likely are you to offend?

# The user can then input their Gender, Age and Area of choice.

Imagine you are a female from London, with the age range 18 to 20. You would input those details in the left hand panel and then press submit to get the likelihood of you offending.


![width](rshiny_tool.png)

In the background, the proportion of offenders in these sub-categories is calculated and the number of offenders in 1,000 is provided, after pressing "Submit".


--- .class #id 

## How likely are you to offend?

# Output of the product


The output given is the number of offenders in 1,000 individuals who all have the same age, gender and area as the submitted entries. Further, the risk of reoffence is provided too.

Two plots are given that show the breakdown offences committed by offence category in the age, gender and area categories and the number of previous offences commited by the same individuals.


<img src="assets/fig/unnamed-chunk-2-1.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" style="display: block; margin: auto;" />
