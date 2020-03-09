Untitled
================

library(tidyverse) read\_csv("data/data.csv")

my\_data &lt;- read\_csv("data/data.csv")

mean(my\_data*f*0)*m**e**a**n*(*m**y*<sub>*d*</sub>*a**t**a*durationV) mean(my\_data$int)

split data into different columns to get means based on lex stress
==================================================================

separate(data = my\_data, col = info, into = c("word", "stress"), sep = "\_")

make it an object
=================

my\_new\_data &lt;- separate(data = my\_data, col = info, into = c("word", "stress"), sep = "\_")

calculate means for each variable
=================================

for vowel duration
==================

my\_new\_data %&gt;% group\_by(stress) %&gt;% summarize(mean\_durationV = mean(durationV))

for f0
======

meanf0 &lt;- my\_new\_data %&gt;% group\_by(stress) %&gt;% summarize(mean\_f0 = mean(f0))

for stress
==========

meanint &lt;- my\_new\_data %&gt;% group\_by(stress) %&gt;% summarize(mean\_int = mean(int))

install.packages("ggplot2")

library(ggplot2)

qplot(my\_new\_data$, geom="histogram")

ggplot(data=my\_new\_data, aes(durationV$int)) + geom\_histogram()
