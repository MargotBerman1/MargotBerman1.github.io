---
permalink: /
title: "Illicit Financial Flows in the Carribean"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Modeling a country's vulnerability to de-risking
======
hopefully I am able to do that


I will code things
======

see example below

```

ar1_gen <- function( nobs, sd) {
  y <- rep(0,nobs)
  for(t in 2:nobs) {
    y[t] <- y[t-1] + rnorm(1, mean = 0, sd=sd)
  }
  return(y)
}


test_statistic <- rep(0,1000)
p_values <- rep(0,1000)
for(i in 1:1000) {
  x <- ar1_gen(nobs = 50, sd=1)
  y <- ar1_gen(nobs = 50, sd=1)
  test_statistic[i] <- summary(lm(y~x))$coefficients[1,3]
  p_values[i] <- summary(lm(y ~ x))$coefficients[2, 4]
}

```


how do i commit things to github?

```
git add .
git commit -m "commit details"
git push origin

```




