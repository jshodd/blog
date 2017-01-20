+++
# Date this page was created.
date = "2016-12-16"

# Project title.
title = "Clojure Webapp"

# Project summary to display on homepage.
summary = "A simple recipe web application built using Clojure."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "clojure.png"

# Optional image to display on project detail page (relative to `static/img/` folder).
image = "clojure-webapp-new.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["course-work"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

+++

[See The Code Here!](https://www.github.com/jshodd/Clojure_Webapp)

This project was an assignemnt in my Language Design class. In this class we learned three different programming languages from three different programing paradigms: functional, object oriented, and logic based. Clojure is a purely functional language, so the structure is much different from what I was used to at the time. for example, a simple function to count the occurences of an element 'x' in a list would look like this:

```
 (defn count-occurrences
  [x lst]
  (cond
    (empty? lst) 0
    (list? (first lst)) (+ (count-occurrences x (first lst)) (count-occurrences x (rest lst)))
    (= (first lst) x) (+ 1 (count-occurrences x (rest lst)))
    :else (recur x (rest lst))
    )
  )
```

As a way to tie together the various aspecs of the language that we were learning, we were tasked with setting up a simple web application using Clojure. for this project we used a few tools called Ring, Compojure, and Hiccup. This was my first experience with web related work and taught me the fundementals of setting up url routes, handlers, and creating views. While my project was quite simple in retrospect, it gave me an opportunity to learn some more intimate parts of the language.
