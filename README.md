# Power-Analysis
Script for power analysis in R, ranging from Chi-Square to multivariate regression

#Be sure to have the package "pwr" installed prior to use


#Installation
install.packages("pwr")

#Loading "pwr"
library("pwr")

#For each of these, exclude the part of the code you want to know more about. For instance, if you are interested in knowing required sample needed for a paired t-test with a moderate effect size, do not include "n=" in the code. If you are more interested in learning about the effect size that a certain sample gives you, exclude the effect size variable (in the case of a t-test, this would be "d"). Additionally, "sig.level" is normally set to ".05" and "power" is set to ".80".


#Chi-Square
pwr.chisq.test(w =, N = , df = , sig.level =, power = )
##w=effect size (Small=.1, Moderate=.3, Large=.5)


#Correlations
pwr.r.test(n = , r = , sig.level = , power = )
##r=effect size (Small=.1, Moderate=.3, Large=.5)


#T-Tests
pwr.t.test(n = , d = , sig.level = , power = , type = c("two.sample", "one.sample", "paired"))
##d=effect size (Small=.2, Moderate=.5, Large=.8)


#T-Test: Groups with different sample sizes
pwr.t2n.test(n1 = , n2= , d = , sig.level =, power = )
##d=effect size (Small=.2, Moderate=.5, Large=.8)


#ANOVA
pwr.anova.test(k = , n = , f = , sig.level = , power = )
##k=number of groups,f=effect size (Small=.1, Moderate=.25, Large=.4)


#Linear Regression
pwr.f2.test(u =, v = , f2 = , sig.level = , power = )
##f2=effect size (Small=.02, Moderate=.15, Large=.3)
##u=Numerator Degrees of Freedom, v=Denominator Degrees of Freedom

