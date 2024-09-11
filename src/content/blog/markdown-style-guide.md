---
title: '1_making_a_blog'
description: 'A blog post about starting a blog!'
pubDate: 'September 9, 2024'
heroImage: '/pexels-ketut-subiyanto-4126694.jpg'
heroAlt: 'exhausted woman with head on laptop keyboard'
heroCredit: 'Photo by Ketut Subiyanto: https://www.pexels.com/photo/exhausted-woman-with-head-on-keyboard-4126694/'
---

> A blog post about starting a blog!

With so many tools and options out there, starting a blog felt daunting — I often find myself with ‘_analysis paralysis_’ when it comes to starting out new projects out of the personal expectation that it has to be perfect. To get over this hurdle, I listed key objectives I had in mind when it came to what I wanted from building a blog. I wanted the ability to quickly spit out blog posts, have the flexibility to design the front-end (what the users see), and familiarize myself with modern development practices such as CI/CD (continuous integration/deployment).  I consulted with good ‘ol chatGPT, Stack Overflow and Reddit to see some suggestions on what people have been using. 

Based on my objectives, I decided to go with a static site generator which creates a front-end for me over a ‘head-full’ CMS like Wordpress or even a front-end + CMS combination. I’ll be the only one posting so I don’t think a CMS is necessary.  

###### Before going further I’d like to clarify what these letters mean in simple terms...

**CMS** - _content management system_, it's a software platform that allows users to create, manage, and publish digital content on a website without needing too much tehcnical knowledge. It can either be...
1. a headless CMS - which provides an API/back-end for content delivery to verious front-end technologies. Examples are Sanity, Contentful. 
2. a traditional CMS - integrates both content management and presentation layers. Essentially controls the front-end and back-end of the website (like Wordpress)

"But what the heck are front-end, back-end, and API?"

**Front-end** refers to the part of the website that users can see and interact with, it involves, structure, design, and functionality! Some of the languages and technologies for front-end are: HTML (_HyperText Markup Language_), CSS (_Cascading Style Sheets_), JS (_JavaScript_), and the rabbit hole can go even deeper with frameworks and libraries (pre-made code by really smart people so that we don't have to program commonly used coding patterns all over again) like the React, Angular, Vue, etc.

**Back-end** is the part of the website that users don't see -- it's the 'server side' of a website or application that manages and stores data and logic. So when you think about it, a headless CMS is just pre-made code that provides the 'back-end' of our website. 

An **API** stands for _Application Programming Interface_ and it's essentially code that allows the front-end to interact with the backend to get data or enable some kind of functionality. 
<br/>

Okay, now that we sort of know what we want to build our blog with, which technologies do we go with? With our current net worth of -$2.00, we can’t exactly afford those fancy paid tools so we add another criteria to our search, it has to be free! It also has to be somewhat approachable as a novice web developer — at this point of writing I have some experience in front-end projects involving Javascript and React, alongside some Java API programming. 

~For now, I’ve chosen Gatsby — a React-based framework which will give us the foundation for our front-end portion of the website. It will generate code for me which is what the users see. 
To set it up, simply follow the instructions on here, it involves installing some applications:
https://www.gatsbyjs.com/docs/tutorial/getting-started/part-0/
Setting up the environment (fiddling with different versions of Node, Gatsby, react-dom, react took some time) can be a headache but after several hours later,~ 
I have a website I can view by entering this on my browser: http://localhost:8000 
This initial website won’t be viewable on other people’s computers as the code is only stored in my computer…

I initially set out to use Gatsby as my static site generator of choice and went down the rabbit hole of setting up React components, installing Gatsby specific plugins, creating queries via GraphQL and rendering pages based on the queries. Unfortunately I hit a dead-end when I found out Gatsby as a framework has been deprecated for quite some time now (no support for it). See: https://github.com/gatsbyjs/gatsby/issues/38696. So I scrapped it, although I feel like I learned quite a bit about the workflow with regards to dynamic page routing and creating GraphQL queries — so this wasn’t a total waste of time 🥹. 

Anyways, I now turn to another more modern static site generator (Astro!) for the front-end. 

I’ll be going with Astro (a static site generator) to generate the HTML/CSS/JS/configuration files --> deploy and host this site using CloudFlare Pages (so that everyone can see my website, not just me). 

After pushing all files and changes onto a Github repository (a place online to store code), the process for deployment was quite simple. I just had to get the link to my repository and provide it to Cloudflare. I adjust the settings to classify it as an Astro project and <b style="font-size:50px">BOOM!</b> We now have the link to our fully deployed and viewable <a style="text-decoration:none" href="https://goldfishprogramming.pages.dev">blog</a>!

That's all for my first post, thanks for reading! I have some plans to add more features to this blog such as a reader counter and an email newsletter setup that provides subscribers with a notification. See you next time! 😃


<!-- 
## Images

### Syntax

```markdown
![Alt text](./full/or/relative/path/of/image)
```

### Output

![blog placeholder](/blog-placeholder-about.jpg)

## Blockquotes

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

### Blockquote without attribution

#### Syntax

```markdown
> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Note** that you can use _Markdown syntax_ within a blockquote.
```

#### Output

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Note** that you can use _Markdown syntax_ within a blockquote.

### Blockquote with attribution

#### Syntax

```markdown
> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>
```

#### Output

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## Tables

### Syntax

```markdown
| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |
```

### Output

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

## Code Blocks

### Syntax

we can use 3 backticks ``` in new line and write snippet and close with 3 backticks on new line and to highlight language specific syntax, write one word of language name after first 3 backticks, for eg. html, javascript, css, markdown, typescript, txt, bash

````markdown
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```
````

### Output

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

## List Types

### Ordered List

#### Syntax

```markdown
1. First item
2. Second item
3. Third item
```

#### Output

1. First item
2. Second item
3. Third item

### Unordered List

#### Syntax

```markdown
- List item
- Another item
- And another item
```

#### Output

- List item
- Another item
- And another item

### Nested list

#### Syntax

```markdown
- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese
```

#### Output

- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese

## Other Elements — abbr, sub, sup, kbd, mark

### Syntax

```markdown
<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
```

### Output

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Press <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> to end the session.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
-->