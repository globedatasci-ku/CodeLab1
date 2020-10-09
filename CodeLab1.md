<style>
.reveal h1, .reveal h2, .reveal h3 {
  word-wrap: normal;
  -webkit-hyphens: none;
  -moz-hyphens: none;
  hyphens: none;
}

iframe {
  position: absolute;
  top: 50%; 
  left: 50%;
  -webkit-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
  min-width: 100vw; 
  min-height: 100vh; 
  z-index: -1000; 
  overflow: hidden;
}

</style>

Code Lab 1 Intro
========================================================
author: Hannah L. Owens
date: 09 October, 2020
autosize: true
transition: linear
font-family: 'Futura'

Plan for today
========================================================
incremental: true

- Brief introduction to problem solving in R
- Introduction to tutorial interface
- Interactive problem-solving exercises!

Problem solving in R
========================================================
type: section

***
![GIS applications](https://img.etimg.com/thumb/msid-76642954,width-650,imgsize-330838,,resizemode-4,quality-100/although-a-separate-court-case-established-early-holmes-novels-are-in-the-public-domain-the-lawsuit-alleges-the-detective-only-developed-feelings-in-the-last-10-books-.jpg)

First, some words of encouragement
========================================================

## "I can break code all day regardless of the data source." -- Hannah Owens

## "Programming allows you to think about thinking, and while debugging you learn about learning." -- Nicholas Negroponte

## "The most effective debugging tool is still careful thought, coupled with judiciously placed print statements." -- Brian Kerninghan

Some tips on troubleshooting
========================================================
type: section

<div align="center">
<img src="https://testzius.files.wordpress.com/2015/09/bug-in-code.jpg" width=800 height=600>
</div>

Some tips on troubleshooting
========================================================
incremental: true

- What is the error
  - Pay attention to line marks
  - Read error messages
    - When error message makes no sense, Google it!
- Ask for help
  - People you know
  - StackOverflow, GitHub, Reddit, Twitter, etc.
- Walk away (but come back)

Some tips on troubleshooting: Print statements
========================================================
- Where is the error?
- Why is there an error?

Some tips on troubleshooting: Print statements
========================================================

```r
testFunction <- function(y){
  if (y %% 2==0){
    return("notOdd")
  } else return()
}

x <- c()
for(i in 1:3){
  print(i)
  print("executing function")
  newI <- testFunction(i)
  print(paste("newI: ", newI))
  print("appending new i")
  x <- c(x,newI)
  print(x)
}
```
***

```
[1] 1
[1] "executing function"
[1] "newI:  "
[1] "appending new i"
NULL
[1] 2
[1] "executing function"
[1] "newI:  notOdd"
[1] "appending new i"
[1] "notOdd"
[1] 3
[1] "executing function"
[1] "newI:  "
[1] "appending new i"
[1] "notOdd"
```

Introduction to tutorial interface
========================================================
type: section

Introduction to tutorial interface
========================================================
- You will get a link to an R tutorial.
- You will be split into breakout rooms.
- As a group, you will work to solve each problem.
- In between problems, we will regroup to discuss.

Introduction to tutorial interface
========================================================
- A tutorial is a special kind of interactive R interface, powered by Shiny.
- Shiny is a framework for building web applications using R code.
- The app is published on the shiny.io server
  - You don't even need to have a functioning version of R set up on your machine!

***
<img src="https://www.libraries.rutgers.edu/sites/default/files/styles/resize_to_300px_width/public/events/2019/09/shiny.png?itok=Nr_Xx5T6" width=500>

A brief tour of the interface
========================================================
Tutorial app location: https://hannah-owens.shinyapps.io/CodeLab_1/