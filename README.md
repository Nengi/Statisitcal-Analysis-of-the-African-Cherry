# Statisitcal-Analysis-of-the-African-Cherry
This primary aim is to determine if physical characteristics of fruits differ by location by utilizing statistical data analysis. There are about 236 observations from 6 different locations. 

## Technology Used
* R

## Example Code
```
ggplot(data=ft,aes(x=fwgt))+geom_histogram(bins=20)+ ggtitle("Histogram of Fruit Weight") 
ggplot(data=ft,aes(x=fwgt))+geom_histogram(bins=15)+facet_wrap(~location,ncol=3) +ggtitle("Histogram of Fruit Weight By Location") 
ggplot(data=ft,aes(x=fwgt))+geom_freqpoly(bins=15)+facet_wrap(~location,ncol=3) +ggtitle("Histogram of Fruit Weight By Location")
ggplot(data=ft,aes(x=location,y=fwgt))+geom_boxplot()+ ggtitle("Boxplot of Fruit Weight") 
ggplot(data=ft,aes(sample=fwgt)) + geom_qq(distribution = stats::qnorm)+ stat_qq_line() + facet_wrap(~location)+ facet_wrap(~location)+ggtitle("QQPlot For Fruit Weight By Location")

scatterplotMatrix(ft[-c(1,5,6)],groups=ft$location, regLine = FALSE,smooth = FALSE)
title(main="Scatterplot Matrix of Fruit Attributes, With Location Seperation By Color")

nonpartest(fdiam|fwgt|flgt|seedno~location,data=ft4)
```


# Project Status
Incomplete. Tests for normality indicate that MANOVA will not be a good fit for analysis. I have utilized the multivirate Non-Parametric test available in R. To continue the following will be considered:
* Other statistical distributions i.e Triangle distribtution
* Bayesian Inference
* Cluster Analysis
