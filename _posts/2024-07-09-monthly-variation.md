---
title: "Small thoughts on dealing with monthly consumption data"
date: 2024-07-09
categories:
  - monthly variation
tags:
  - Monthly consumption
  - Data analysis 
---

When working with monthly electricity and natural gas consumption data, I've encountered several problems in data cleaning and analysis. The most significant (and nightmarish) one is... how to deal with monthly variation! I wandered in endless lines of R/Stata codes for a few weeks, in particular, when I tried event studies (dynamic TWFE DiD in Roth et al. (2023)). Here is the list of methods I've been trying so far; some worked, some didn't help, but still can be one way to begin exploring which one is 'the one.' 

- Different time indicators: i.month i.year or i.month#i.year
- Add control variables, such as monthly weather
- Look into differences between same month / different years
- Add the same month/previous year value as in Ferraro et al. (2011)
- Matching/Synthetic DiD 
  
Ferraro, P. J., Miranda, J. J., & Price, M. K. (2011). The persistence of treatment effects with norm-based policy instruments: evidence from a randomized environmental policy experiment. American Economic Review, 101(3), 318-322.
Roth, J., Sant’Anna, P. H., Bilinski, A., & Poe, J. (2023). What’s trending in difference-in-differences? A synthesis of the recent econometrics literature. Journal of Econometrics, 235(2), 2218-2244.
