---
title: An Example R Markdown Document
subtitle:  (A Subtitle Would Go Here if This Were a Class)
author: Steven V. Miller
date: 
fontsize: 10pt
output:
  beamer_presentation:
#    keep_tex: true
#    toc: true
    slide_level: 3
    includes:
      in_header: ~/Dropbox/teaching/clemson-beamer-header-simple.txt
      after_body: ~/Dropbox/teaching/table-of-contents.txt
---

# Pop Songs and Political Science
## Morning Train

### Sheena Easton and Game Theory

Sheena Easton describes the following scenario for her baby:

1. Takes the morning train
2. Works from nine 'til five
3. Takes another train home again
4. Finds Sheena Easton waiting for him

\bigskip Sheena Easton and her baby are playing a \textcolor{clemsonorange}{zero-sum (total conflict) game}.

- Akin to Holmes-Moriarty game (see: von Neumann and Morgenstern)
- Solution: \textcolor{clemsonorange}{mixed strategy}


## Never Gonna Give You Up

### Rick Astley's Re-election Platform

Rick Astley's campaign promises:

- Never gonna give you up
- Never gonna let you down
- Never gonna run around and desert you
- Never gonna make you cry
- Never gonna say goodbye
- Never gonna tell a lie and hurt you.


\bigskip Whereas these pledges conform to the preferences of the \textcolor{clemsonorange}{median voter}, we expect Congressman Astley to secure re-election.

## Caribbean Queen
### Caribbean Queen and Operation Urgent Fury

In 1984, Billy Ocean released ``Caribbean Queen''.

- Emphasized sharing the same dream
- Hearts beating as one

\bigskip ``Caribbean Queen'' is about the poor execution of Operation Urgent Fury.

- Echoed JCS chairman David Jones' frustrations with military establishment.

\bigskip Billy Ocean is advancing calls for what became the Goldwater-Nichols Act.

- Wanted to take advantage of \textcolor{clemsonorange}{economies of scale}, resolve \textcolor{clemsonorange}{coordination problems} in U.S. military.

## Good Day
### The Good Day Hypothesis

We know the following about Ice Cube's day.

1. The Lakers beat the Supersonics.
2. No helicopter looked for a murder.
3. Consumed Fatburger at 2 a.m.
4. Goodyear blimp: "Ice Cube's a pimp."

\bigskip This leads to two different hypotheses:

- $H_0$: Ice Cube's day is statistically indistinguishable from a typical day.
- $H_1$: Ice Cube is having a good (i.e. greater than average) day.

\bigskip These hypotheses are tested using archival data of Ice Cube's life.



# Rendering This Document
### The Problem of Rendering in Markdown

One big disadvantage to Markdown: compiling.

\bigskip Here's what it would look like from Terminal \medskip


![Markdown Call](markdown-call.png)

\bigskip Nobody got time for that.

### One Alternative: Rstudio

\begin{center}
  \includegraphics[width=1.00\textwidth]{knit-rstudio.png}
\end{center}



### Another Alternative: Rscript

Another option: noninteractive \texttt{Rscript}

- I prefer this option since I tend to not like GUIs.
- Assumes you're on a Linux/Mac system.

Save this to a .R script (call it whatever you like)

- Note that the "s" in "utils" package is cut off in verbatim environment below.


```
#! /usr/bin/Rscript --vanilla --default-packages=base,stats,utils
library(knitr)
library(rmarkdown)
file <- list.files(pattern='.Rmd')
rmarkdown::render(file)
```



Make it executable. Double click or run in Terminal.

- Keep a copy in each directory, but keep only one .Rmd per directory.


# Conclusion
### Conclusion

Beamer markup is messy. Markdown is much more elegant.

- Incorporating R with Markdown makes Markdown that much better.
- Rendering Markdown $\rightarrow$ Beamer requires minimal Rscript example.
 - I provide such a script to accompany this presentation.

# (WIP) Editorial - Jekyll Theme

A Jekyll version of the "Editorial" theme by [HTML5 UP](https://html5up.net/).

![Editorial Theme](assets/images/screenshot.jpg "Editorial Theme")

# How to Use

For those unfamiliar with how Jekyll works, check out [https://jekyllrb.com/](https://jekyllrb.com/) for all the details,
or read up on just the basics of [front matter](https://jekyllrb.com/docs/frontmatter/), [writing posts](https://jekyllrb.com/docs/posts/),
and [creating pages](https://jekyllrb.com/docs/pages/).

- **GitLab**: Simply fork this repository and start editing the `_config.yml` file!
- **GitHub**: Fork this reposity and create a branch named `gh-pages`, then start editing the `_config.yml` file! The `.gitlab-ci.yml` file is only needed for GitLab Pages, so feel free to delete this if you are using GitHub instead.

# Added Features

* Add your **social profiles** easily in `_config.yml`.

# Configuration

You can use the following custom parameters in `_config.yml`.

## Site
- `subtitle` sets the text for the lighter colored text next to your site's title.

## Social
- `500px_url`
- `facebook_url`
- `github_url`
- `gitlab_url`
- `googleplus_url`
- `instagram_url`
- `linkedin_url`
- `pinterest_url`
- `slack_url`
- `twitter_url`

# Credits

Original README from HTML5 UP:

```
Editorial by HTML5 UP
html5up.net | @ajlkn
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)


Say hello to Editorial, a blog/magazine-ish template built around a toggleable "locking"
sidebar (scroll down to see what I mean) and an accordion-style menu. Not the usual landing
page/portfolio affair you'd expect to see at HTML5 UP, but I figured for my 41st (!!!)
template I'd change it up a little. Enjoy :)

Demo images* courtesy of Unsplash, a radtastic collection of CC0 (public domain) images
you can use for pretty much whatever.

(* = not included)

AJ
aj@lkn.io | @ajlkn


Credits:

	Demo Images:
		Unsplash (unsplash.com)

	Icons:
		Font Awesome (fortawesome.github.com/Font-Awesome)

	Other:
		jQuery (jquery.com)
		html5shiv.js (@afarkas @jdalton @jon_neal @rem)
		Misc. Sass functions (@HugoGiraudel)
		Respond.js (j.mp/respondjs)
		Skel (skel.io)
```

Repository [Jekyll logo](https://github.com/jekyll/brand) icon licensed under a [Creative Commons Attribution 4.0 International License](http://choosealicense.com/licenses/cc-by-4.0/).
