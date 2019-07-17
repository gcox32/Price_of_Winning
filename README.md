<img src="assets/brand logo.png" width="100" height="100"></a>

# The Price of Winning: The True Cost of Your Bad Football Team
Repo for R Project on Money and College Football

## Table of Contents

- [The Problem](#theproblem)
- [The Data](#thedata)
- <a href="https://github.com/gcox32/Price_of_Winning/blob/master/Features.txt">The Features</a>
- [The Libraries](#the-r-libraries)
- [Acknowledgements](#acknowledgements)

## The Problem

    There is and has been across the last decade an arms race in the world of college football for the biggest and the best team/coach/stadium. And why shouldn’t there be? The allure of national television exposure or of the supposed millions in revenue ought to be enough to sway any small university to fund a team. However, revenue data at division I programs show us that only the rich are getting richer, and the vast majority of programs are actually bleeding money. To make this worse, these latter schools are funding the difference by subsidizing their football programs via student fees. It follows (and the numbers show) that schools that are receiving the least revenue from things like ticket sales (i.e. schools where the students seemingly care the least) are subsidizing their programs through the most substantial student fees.

    Possible problems:

        - to what degree is this an issue?
        - How many schools are both a) losing money through their football program and b) subsidizing their program through student fees?
        - What do student fees (as a portion of student tuition) look like across schools?
        - how does win-loss record predict:
            - revenue of the football program
            - cost of student tuition
            - percentage of program revenue subsidized by student fees
        - how does percentage subsidized predict tuition cost
        - how does percentage subsidized predict revenue of the football program
            - percentage of tuition towards student fees
        - can win-loss record predict the viability (profitability) of a program?

## The Data

The dataset with win-loss records is pulled from 4 different year specific tables via <a href="teamrankings.com">teamrankings.com</a> and the revenue and subsidy dataset via <a href="http://projects.huffingtonpost.com/projects/ncaa/reporters-note">Huffington Post</a>. The former set holds 5 tables (1 per year) and has roughly 130 records each. The latter dataset holds 1,015 records with 49 variables each. Both sets are in “.xlsx” formats.

## The R Libraries

The following libraries were used to wrangle the data, plot the data, and then ultimately use machine learning strategies to predict:

```r
library(dplyr)
library(tidyr)
library(ggplot2)
library(scales)
library(caTools)
library(randomForest)

```

## Acknowledgements

This project would not have been possible without the legwork of those at Huffington Post who first accrued all of this data through the deep examination of all of these NCAA Revenue/Expense forms. The original article that inspired this project can be found <a href="https://projects.huffingtonpost.com/projects/ncaa/sports-at-any-cost" target="_blank">**here.**</a>

I also owe a thanks to the team at <a href="www.teamrankings.com" target="_blank">**teamrankings.com**</a> as this is where I was able to grab all of these universities' win-loss information.