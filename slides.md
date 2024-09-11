---
theme: light-icons
image: ./images/intro.jpg
title: Web development - Introduction | Part 2
transition: slide-left
mdc: true
layout: intro
download: true
favicon: "https://scratchmy.dev/favicon.ico"
---

<div class="mb-4 absolute top-20 left-12">
  <span class="text-6xl text-teal-400 font-500" >
    Web development<light-icon icon="code"/>
  </span>
  <div class="text-4xl text-white text-opacity-60 font-300 uppercase" >
    Introduction – Part 2
  </div>
</div>

<div class="mb-4 absolute bottom-4 right-12">
  <div class="flex gap-x-4 items-center">
    <div class="rounded-full p-0.5 shadow-lg shadow-zinc-800/5 ring-1 backdrop-blur bg-white ring-white/10">
      <img src="/images/profile.webp" sizes="4rem" class="rounded-full object-cover h-16 w-16" alt="Profile picture" width="400" height="400" loading="lazy" decoding="async">
    </div>
    <div class="flex flex-col">
      <p class="!my-1 text-xl">Sébastien VIALLEMONTEIL</p>
      <p class="!my-1">Full stack web developer</p>
      <a href="mailto:sebastien.viallemonteil@institut-agro.fr"><light-icon icon="mail" class="inline-block mb-0.5"/> sebastien.viallemonteil@institut-agro.fr</a>
    </div>
  </div>
</div>

---
layout: image-right
image: ./images/gifs/rolling-eyes.webp
equal: true
---

# First, a bit of history

Yes again… But this is the last time, I promise.

---
layout: dynamic-image
image: ./images/crooked.jpg
equal: false
left: false
---

# Why CSS came to be

<v-clicks>

- **CSS** was born in 1996, a few years after HTML
- Like life, web pages without style feel a bit plain
- Add colors, backgrounds, fonts, etc.
- Position your block the way you want them to be

</v-clicks>

---
layout: dynamic-image
image: ./images/css-versions.jpg
equal: false
left: false
---

# CSS versions

<v-clicks>

- **CSS 1**: finalised in 1996, it helps developers to better style their web pages (colors, spacing, fonts, etc.)
- **CSS 2**: available in 1998 and CSS 2.1 in 2001. Better elements positioning, floating, box models
- **CSS 3**: current version, still in constant evolution, new features added regularly. Introduced layouts, animations, shadows, gradients, rounded borders, etc

</v-clicks>

---
layout: dynamic-image
image: ./images/mix-css-html.jpg
equal: false
---

# Adding CSS to HTML (1/4)
There are 3 ways to add CSS to your HTML files
### External CSS file(s) (recommanded)
```html {6}{lines:true}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link type="text/css" rel="stylesheet" href="style.css">
  </head>
  <body>
    <!-- … -->
  </body>
</html>
```

---
layout: dynamic-image
image: ./images/mix-css-html.jpg
equal: false
---

# Adding CSS to HTML (2/4)
There are 3 ways to add CSS to your HTML files
### The `style` tag

<Transform scale="0.85">

```html {6-10}{lines:true}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style type="text/css">
      div {
        background-color: #000000;
      }
    </style>
  </head>
  <body>
    <div>That’s a good looking division!</div>
  </body>
</html>
```

</Transform>

<ComplementaryMessage class="!-mt-5">This way can be a good addition to external CSS files if you have a few lines of CSS specifc to this HTML file.</ComplementaryMessage>
<ComplementaryMessage type="alert" bordered>If you realise you’re duplicating this code, move it to an external CSS file.</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/mix-css-html.jpg
equal: false
---

# Adding CSS to HTML (3/4)
There are 3 ways to add CSS to your HTML files
### The `style` attribute
```html {8-10}{lines:true}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Document</title>
  </head>
  <body>
    <div style="background: #000000;">
      My not so good looking division!
    </div>
  </body>
</html>
```

<ComplementaryMessage type="danger" bordered>Avoid at all costs! Very hard to maintain on multiple HTML files and difficult to read.</ComplementaryMessage>

---
layout: center-image
---

<h1 class="text-4xl text-teal-600 mb-4">Adding CSS to HTML (4/4)</h1>
<p class="opacity-50 mb-4 -mt-2 text-[1.1rem]">To sum up</p>

<div v-click class="text-left p-2 flex items-center gap-x-4 rounded-md border-1 border-teal-600">
  <img src="/images/no.png" alt="No meme" class="w-40 rounded-md border border-gray-300 dark:border-white" />

```html {*}{lines:true}
<div style="background: #000000;">
  My not so good looking division!
</div>
```

</div>

<div v-click class="text-left mt-2 p-2 flex items-center gap-x-4 rounded-md border-1 border-teal-600">
  <img src="/images/yes.png" alt="Yes meme" class="w-40 rounded-md border border-gray-300 dark:border-white" />
  <div>
<div class="flex items-center gap-x-2">

```html {4,7}{lines:true}
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <link type="text/css" rel="stylesheet" href="style.css">
</head>
<body>
  <div>My good looking division!</div>
</body>
```

<div class="flex flex-col items-center gap-y-1 border p-2 rounded-md">
  <tabler-file-type-html class="text-xl opacity-75" />
  <em>index.html</em>
</div>
</div>
<div class="flex items-center gap-x-4">

```css {*}{lines:true}
div {
  background: #000000;
}
```

<div class="flex flex-col items-center gap-y-1 border p-2 rounded-md">
  <tabler-file-type-css class="text-xl opacity-75" />
  <em>style.css</em>
</div>
</div>
</div>
</div>

---
layout: dynamic-image
image: ./images/select.jpg
equal: false
left: false
---

# Setting CSS rules

```css{*}{lines:true}
body {
 backgrond-color: #000000;
}
div {
 color: #FFFFFF;
 text-align: center;
}
```

<div class="absolute h-3 w-7 top-36 left-26" v-mark.box.blue="2"></div>
<div class="absolute h-3 w-5 top-49 left-26" v-mark.box.blue="2"></div>

<div v-click>
  <p><span v-mark.undeline.blue="2" class="font-bold">Selectors</span> will determine which HTML tags will be affected by the associated CSS rules.</p>
  <p><span v-mark.undeline.red="3" class="font-bold">Rules</span> will change the aspect of the affected HTML tags. They are composed of a <strong>name</strong> and a <strong>value</strong> separated by a colon.</p>
</div>

<div class="absolute h-3 w-41 top-40 left-28" v-mark.box.red="3"></div>
<div class="absolute h-8 w-31 top-54 left-28" v-mark.box.red="3"></div>

<div v-click="4">
  <ComplementaryMessage type="alert" bordered>Don’t forget the semi-colon at the end of each rule line.</ComplementaryMessage>
</div>

---
layout: center-image
---

<h1 class="text-4xl text-teal-600 mb-2">Hierarchy for selectors</h1>

<p class="text-left mt-1 text-sm opacity-75">Multiple selectors to affect the same rules</p>
<div class="flex items-center text-left gap-x-4">

```css{*}{lines:true}
div, p {
  font-size: 1.2em;
}
```

<light-icon icon="arrows-horizontal" size="24px"></light-icon>

```html{*}{lines:true}
<div>My division will be affected</div>
<p>So will this paragraph</p>
```

</div>

<v-click>
<p class="text-left mt-1 text-sm opacity-75">Descendents</p>
<div class="flex items-center text-left gap-x-4">

```css{*}{lines:true}
div p {
  font-size: 1.2em;
}
```

<light-icon icon="arrows-horizontal" size="24px"></light-icon>

```html{*}{lines:true}
<div>
  <p>This paragraph will be bigger in size</p>
</div>
<p>This paragraph is not a descendant of a div and will not be affected</p>
```

</div>
</v-click>

<v-click>
<p class="text-left mt-1 text-sm opacity-75"><strong>Direct</strong> descendents</p>
<div class="flex items-center text-left gap-x-4">

```css{*}{lines:true}
div > p {
  font-size: 1.2em;
}
```

<light-icon icon="arrows-horizontal" size="24px"></light-icon>

```html{*}{lines:true}
<div>
  <p>This paragraph will be bigger in size</p>
  <section>
    <p>This paragraph is not a direct descendant of a div and will not be affected</p>
  </section>
</div>
```

</div>
</v-click>
<v-click>
<p class="text-left mt-1 text-sm opacity-75">Next sibling</p>
<div class="flex items-center text-left gap-x-4">

```css{*}{lines:true}
div + p {
  font-size: 1.2em;
}
```

<light-icon icon="arrows-horizontal" size="24px"></light-icon>

```html{*}{lines:true}
<div>
  <p>This paragraph is not after a div and will not be affected</p>
</div>
<p>This paragraph will be bigger in size</p>
```

</div>
</v-click>

---
layout: dynamic-image
image: ./images/background.jpg
equal: false
left: false
---

# Setting a background to an element (1/2)
When it comes to backgrounds, you have many options to chose from: single color, an image (animated or not), a video or a gradient. Let’s focus on the basics.

<div v-click>
Setting a background color

```css{*}{lines:true}
body {
  background-color: red;
  /* You can chose from named colors or rgb|rgba|hexa|hsl syntaxes */
}
```

</div>

---
layout: dynamic-image
image: ./images/background.jpg
equal: false
left: false
---

# Setting a background to an element (2/2)
When it comes to backgrounds, you have many options to chose from: single color, an image (animated or not), a video or a gradient. Let’s focus on the basics.

<div v-click>
Setting an image with some options

```css{*}{lines:true}
body {
  /* Path of the image */
  background-image: url('images/my-image.jpg');
  /* Position the image in the container */
  background-position: top center;
  /* Should the image cover all the container’s background ? */
  background-size: 50%;
  /* Should the image repeat itself ? */
  background-repeat: none;
  /* Should the image be fixed when the user scrolls up and down ? */
  background-attachment: fixed;
}
```

More on the [background](https://developer.mozilla.org/en-US/docs/Web/CSS/background) rules.

</div>

---
layout: dynamic-image
image: ./images/text.jpg
equal: false
---

# Personalize texts (1/2)
CSS gives almost infinite possibilities to create a specific and unique look for your texts, you can spend hours (please, don’t) playing with options.

<div v-click>

```css{*}{lines:true}
p {
  /* Setting a color (same usual options) */
  color: #FF0000;
  /* Text alignment */
  text-align: justify;
  /* Text decoration */
  text-decoration: underline;
  /* Text indention */
  text-indent: 10px;
  /* Text transformation (upper|lower case or capitalized) */
  text-transform: uppercase;
  /* Text shadow to make your text blush */
  text-shadow: 2px 5px 10px #AA0000;
}
```

</div>

<img v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: -250, y: -272}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/typing.webp" alt="Cat typing GIF" />

---
layout: dynamic-image
image: ./images/text.jpg
equal: false
---

# Personalize texts (2/2)
Spacing your texts and let them breath.

<div v-click>

```css{*}{lines:true}
p {
  /* Height for each line of text (px, em, rem, etc.) */
  line-height: 1.5rem;
  /* Spacing each letter */
  letter-spacing: 10px;
  /* Spacing each word */
  word-spacing: 5px;
  /* Decide if the browser should break lines using white spaces */
  white-space: nowrap;
  /* Allow the browser to break words when doing a line break */
  word-wrap: break-word;
}
```

More on [text](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align) rules.

</div>

<img v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: -380, y: -287}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/typing2.webp" alt="Dog typing GIF" />

---
layout: dynamic-image
image: ./images/fonts.jpg
equal: false
left: false
---

# Fonts
Dress your texts with their best font.

<div v-click>

```css{*}{lines:true}
p {
  /* 
    Pick a font you like that is also readable.
    We need to set fallback fonts in case the main font
    is not available on the user’s computer
  */
  font-family: Helvetica, Arial, sans-serif;
  /* Change the default font size (px, em, rem, etc.) */
  font-size: 1.5rem;
  /* Give a bit of style */
  font-style: italic;
  /* Change the font’s weight */
  font-weight: 600;
}
```

More on [font](https://developer.mozilla.org/en-US/docs/Web/CSS/font) rules.
</div>

---
layout: dynamic-image
image: ./images/squeeze.jpg
equal: false
---

# Concatenation
Shorter does not always rhymes with readable. Use with caution.

<div v-click>

```css{*}{lines:true}
body {
  /* Change muliple font options at once */
  font: italic 1.2rem Helvetica, sans-serif;

  /* Same for background */
  background: left 5% / 15% 60% repeat-x url("./images/star.png");
}
```

</div>

---
layout: dynamic-image
image: ./images/hot-balloon.jpg
equal: false
left: false
---

# Styling your lists
Yes, you can change these basic bullet points or numbers!

<div v-click>

```css{*}{lines:true}
ul {
  list-style-type: decimal;
  list-style-position: inside;
}

ol {
  list-style-type: disc;
  /* 
    Other possible values: circle, square, lower-alpha, upper-alpha, etc.
    Or even emojis
  */
}

ul:last-child {
  list-style-image: url('./images/my-own-marker.svg');
}
```

</div>

<ComplementaryMessage>Yes, I just switched the default values for each type of list.<br>What a rebellious (and useless) thing to do!</ComplementaryMessage>

<v-click>

More on [lists](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style) rules.

</v-click>

<img v-motion v-click="4" :initial="{x: 999, y: -999}" :enter="{x: 560, y: -350}" class="absolute rounded-md border-2 border-teal-600 w-74" src="/images/gifs/bruce.webp" alt="Bruce file cabinet GIF" />

---
layout: dynamic-image
image: ./images/frame.jpg
equal: false
---

# Turn the tables
Merge table borders, space these borders, lay out the cells.

<div v-click="1">

```css {all|all|1-5|7-10}{lines:true}
table {
  border-collapse: collapse; /* "separate" by default */
  table-layout: fixed;
  caption-side: bottom;
}

.other-table {
  empty-cells: hide;
  border-spacing: 10px;
}
```

</div>

<div v-motion v-click="[2,3]" :initial="{x: 999, y: -999}" :enter="{x: -350, y: -250}" :leave="{x: 999, y: -999}" class="absolute p-4 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600 max-w-1/3">
  <table class="border border-gray-800 table-fixed caption-bottom">
    <caption>My caption</caption>
    <tr>
      <th class="border border-gray-800 p-1 !font-bold">Title 1</th>
      <th class="border border-gray-800 p-1 !font-bold">Title 2</th>
      <th class="border border-gray-800 p-1 !font-bold">Title 3</th>
    </tr>
    <tr>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
    </tr>
    <tr>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1"></th>
      <th class="border border-gray-800 p-1">Text</th>
    </tr>
    <tr>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
    </tr>
  </table>
</div>

<div v-motion v-click="3" :initial="{x: 999, y: -999}" :enter="{x: -325, y: -275}" class="absolute p-4 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <table class="border-separate border-spacing-sm [empty-cells:hide]">
    <caption>My caption</caption>
    <tr>
      <th class="border border-gray-800 p-1 !font-bold">Title 1</th>
      <th class="border border-gray-800 p-1 !font-bold">Title 2</th>
      <th class="border border-gray-800 p-1 !font-bold">Title 3</th>
    </tr>
    <tr>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
    </tr>
    <tr>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1"></th>
      <th class="border border-gray-800 p-1">Text</th>
    </tr>
    <tr>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
      <th class="border border-gray-800 p-1">Text</th>
    </tr>
  </table>
</div>

---
layout: dynamic-image
image: ./images/class.jpg
equal: false
left: false
---

# Use your ids with class…

<v-clicks>

- Ids and classes are two fundamentals of CSS that will allow you the target one or more HMTL tags.
- Ids are **unique** in a page. There can’t be two of the same, never forget that ~~young padawan~~.
- Classes on the other hand, are very *handy* to target multiple HTML elements, no matter their type (ie. *div*, *a*, *img*, etc.).

</v-clicks>

---
layout: dynamic-image
image: ./images/class.jpg
equal: false
left: false
---

# Use your ids with class…

```html {*}{lines:true}
<div id="my_container">
  <p>That’s some good ID you got there my good sir!</p>
  <span class="error">Whoopsy daisy !</span>
  <p>Your lack of ID is appalling…</p>
  <em class="error">That’s a classic!</em>
</div>
```

```css {*}{lines:true}
#my_container {
  width: 80%;
  background: #000000;
}
.error {
  color: #FF0000;
}
```

<div class="absolute h-6 w-28 top-43 left-34" v-mark.circle.red="1"></div>
<div class="absolute h-4 w-24 top-76 left-24" v-mark.circle.red="1"></div>

<div class="absolute h-6 w-22 top-52 left-39" v-mark.circle.blue="2"></div>
<div class="absolute h-6 w-22 top-61 left-36" v-mark.circle.blue="2"></div>
<div class="absolute h-4 w-14 top-94 left-24" v-mark.circle.blue="2"></div>

<div v-motion v-click="3" :initial="{x: 999, y: -999}" :enter="{x: 550, y: -235}" class="absolute w-1/3 flex items-center p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <style>
    #my_container {
      width: 80%;
      background: #000000;
      color: white;
    }
    .error {
      color: #FF0000;
    }
  </style>
  <div id="my_container">
    <p>That’s some good ID you got there my good sir!</p>
    <span class="error">Whoopsy daisy !</span>
    <p>Your lack of ID is appalling…</p>
    <em class="error">That’s a classic!</em>
  </div>
</div>

---
layout: dynamic-image
image: ./images/class.jpg
equal: false
left: false
---

# What’s your id doing in my class?
Or is it the other way around?

Like any other CSS selector, you can use hierarchy to select specific nested tags, or other.

```css {*}{lines:true}
#container .error {
  color: #FF0000;
  font-weight: bold;
}
```
<v-click>

Can you guess which element(s) will be targeted by this selector?

</v-click>

<ComplementaryMessage bordered>

Hint: if there is one or more HTML element with the **class** `error` located outside the element with the **id** `container`, they won’t be affected by these CSS rules.

</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/jack.jpg
equal: false
---

# Hierarchy you said?

```css {*}{lines:true}
/* Inputs with 'type' attribute set to 'button' */
input[type="button"] {
  color: #FFFFFF;
}
/* Spans with 'class' attribute including the word 'button' */
span[class*="button"] {
  color: #FFFFFF;
}
/* Images with 'title' attribute starting with 'My' */
img[title^="My"] { 
  border-color: #FFFFFF;
}
/* Links with 'href' attribute ending with '.html' */
a[href$=".html"] {
  text-decoration: none;
}
```

<ComplementaryMessage>Sometimes, you don’t need any id or class to get things done 🤷‍♂️</ComplementaryMessage>

<img v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: -250, y: -315}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/wdym.webp" alt="WDYM GIF" />

---
layout: intro
image: ./images/quiz.jpg
---

<h1 class="absolute left-12 bottom-12">Quiz time</h1>
<p class="opacity-80 absolute left-12 bottom-6">Yep, same GIF, I’m that lazy!</p>

<img src="/images/gifs/mouahahah.webp" class="absolute right-12 top-[30%] border-2 border-white rounded-md" alt="Mouahaha Gif" />

---
layout: dynamic-image
image: ./images/question.jpg
equal: false
---

# Start your engine
Ready, set, GO!

<v-clicks>

- Create a brand new block
- Add a very important heading
- Within this block, a new section appears out of thin air 💨
- To fill that section add an image with a description underneath, like a paragraph, you know
- Lastly after that section there is an article with a few **important** words in it

</v-clicks>

---
layout: dynamic-image
image: ./images/question.jpg
equal: false
---

# Start your engine
You thought that was it right?

<v-clicks>

- The heading should be centered and blue
- Set a green background to that section of yours with a white text so it pops
- 12px of size should be enough for the article’s text
- Finally, the important words should be red and in italic

</v-clicks>

---
layout: dynamic-image
image: ./images/time.jpg
equal: false
left: false
---

# Time’s up!
Who wants to write some code?

<div v-click="1">

```html {*|all|1,12|2|3,6|4-5|7-11}{lines:true}
<div>
  <h1>My important heading</h1>
  <section>
    <img src="img/my_picture.jpg" alt="Easy right?" />
    <p>I don’t know what I’m doing here.</p>
  </section>
  <article>
    These are <strong>very</strong>, but like,
    <strong>very</strong>, for real,
    important <strong>words</strong>!
  </article>
</div>
```

</div>

---
layout: dynamic-image
image: ./images/time.jpg
equal: false
left: false
---

# Time’s up!
Who wants to write some code?

<div v-click>

```css {*}{lines:true}
h1 {
  text-align: center;
  color: blue;
}

section {
  background: green;
  color: white;
}

article {
  font-size: 12px;
}

strong {
  color:red;
  font-style: italic;
}
```

</div>

<div v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: 520, y: -275}" class="absolute flex items-center p-2 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <style>
    #quiz1 h1 {
      text-align: blue;
      color: blue;
    }
    #quiz1 section {
      background: green;
      color: white;
    }
    #quiz1 article {
      font-size: 12px;
    }
    #quiz1 strong {
      color:red;
      font-style: italic;
    }
  </style>
  <div id="quiz1">
    <h1>My important heading</h1>
    <section>
      <img class="h-20" src="/images/grumpy_cat.jpg" alt="Easy right?" />
      <p>I don’t know what I’m doing here.</p>
    </section>
    <article>
      These are <strong>very</strong>, but like,
      <strong>very</strong>, for real,
      important <strong>words</strong>!
    </article>
  </div>
</div>

---
layout: dynamic-image
image: ./images/float.jpg
equal: false
---

# Floaty float float
Floating, left and right

Sometimes we want to write some text surrounding a picture for effect, so it looks cooler. In order to do that, we make our picture **float**

<div v-click>

```html {*}{lines:true}
<!-- The floating element comes first! -->
<img class="my-picture" src="path/to/image.jpg" alt="I’m floating" />
<p>Surrounding that cool picture!</p>
```
```css {*}{lines:true}
.my-picture {
  /* Elements can float either on the left or the right */
  float: left;
}
```

</div>

<div v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: -350, y: -225}" class="absolute p-4 max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <img class="h-20 float-left" src="/images/grumpy_cat.jpg" alt="Cat cat cat" />
  <p class="text-xs !leading-3 !m-0">Dolor aliquyam nulla ut dignissim clita exerci elitr ea laoreet consetetur ut ipsum dolore diam clita vel consequat iusto. Justo et gubergren sadipscing gubergren amet labore takimata ad suscipit eirmod. Elitr vero lorem duo ipsum aliquyam. Ipsum dolores stet nonumy sed elitr et velit eros aliquyam stet eos laoreet et wisi clita. Esse ipsum takimata est diam nonumy augue facilisi labore stet tation erat sed et. Ea option duo dolor takimata duis ut consectetuer diam rebum facilisis. Aliquip adipiscing augue iriure et duis laoreet lorem amet. Sit voluptua clita duo consectetuer. </p>
</div>

---
layout: dynamic-image
image: ./images/clear.jpg
equal: false
left: false
---

# Now let’s be clear
But is it clear though?

In some cases, we only want a small portion of text to encircle our floaty friend. We need to **clear** the following text.

<div v-click>

```css {*}{lines:true}
.left-picture {
  float: left;
}
.right-picture {
  float: right;
}
p.cleared {
  /*
    We either clear the left side, the right or both
    depending on which element(s) is/are floating
   */
  clear: both;
}
```

</div>

<div v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: 560, y: -200}" class="absolute p-4 max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <img class="h-20 float-left" src="/images/grumpy_cat.jpg" alt="Cat cat cat" />
  <img class="h-20 float-right" src="/images/grumpy_cat.jpg" alt="Cat cat cat" />
  <p class="text-xs !leading-3 !m-0 text-justify">Dolor aliquyam nulla ut dignissim clita exerci elitr ea laoreet consetetur ut ipsum dolore diam clita vel consequat iusto. </p>
  <p class="text-xs !leading-3 !m-0 clear-both">Dolor aliquyam nulla ut dignissim clita exerci elitr ea laoreet consetetur ut ipsum dolore diam clita vel consequat iusto. </p>
</div>

---
layout: dynamic-image
image: ./images/display.jpg
equal: false
---

# Put on display
Defining each element’s place in the flow layout

The **display** property will change the default way targeted elements are arranged in the flow layout.
In other words, should they take all the width available or allow some friends to "sit" next to them?

<div v-click>

```css {*}{lines:true}
span.block {
  /* I take the whole free width */
  display: block;
}
div.inline {
  /* I’m nice and take only the width I need and I can’t be resized */
  display: inline;
}
section.inline-block {
  /* I’m nice and take only the width I need BUT I can be resized */
  display: inline-block;
}
```

</div>
<ComplementaryMessage>

**display: none;** will completly hide an element as if it were never there.

</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/measure.jpg
equal: false
left: false
---

# Width and height
Size matters here…

Controlling the **width** and **height** of your elements will allow you to keep your layout organized.

<div v-click>

```css {*}{lines:true}
/* Units can be %, px, em, rem, etc. */
div {
  width: 80%;
}
section {
  display: inline-block;
  height: 50px;
}
span {
  width: 30px;
}
```

</div>

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 560, y: -185}" class="absolute p-4 max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600 text-xs">
  <div class="w-4/5 border border-gray-700 mb-2">My div takes 80% of the total width, see?</div>
  <section class="inline-block border border-gray-700 h-[50px] mb-2">My section is 50px heigh.</section><br>
  <span class="w-[30px] border border-gray-700">Can you guess my width, people?</span>
</div>

<ComplementaryMessage type="alert" bordered>

Remember, **inline** elements (**span**, **a**, etc.) cannot be resized!

</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/measure.jpg
equal: false
left: false
---

# Min and max
It’s time to set boundaries!

Resizable elements (again,  **not inline** elements) can have boundaries when it comes to **width** and **height**.

<div v-click>

```css {*}{lines:true}
div {
  display: inline-block;
  max-width: 80%;
  min-height: 40px;
}
```

</div>

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 560, y: -150}" class="absolute p-4 max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600 text-xs">
  <div class="inline-block max-w-4/5 min-h-[40px] border border-gray-700 mb-2">Only a few words. 40px heigh.</div><br>
  <div class="inline-block max-w-4/5 max-h-[40px] border border-gray-700 mb-2">This one is larger and goes to the set max width (80%). It’s gonna be more than 40px heigh as it has many lines!</div>
</div>

---
layout: dynamic-image
image: ./images/space.jpg
equal: false
---

# Give them space! (1/3)
Control outer and inner space of your elements

<div v-click>

### Outer space
```css {*}{lines:true}
section {
  margin: 12px;
}
```

</div>
<div v-click>

### Inner space
```css {*}{lines:true}
section {
  padding: 8px;
}
```

</div>

<div v-motion v-click="2" :initial="{x: 999, y: -999}" :enter="{x: -360, y: -180}" class="absolute max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <section class="border border-grey-700 m-3 p-2 text-xs">
  Adipiscing vel imperdiet eirmod dolore sit qui accusam diam quod et. Sit dolor sed est takimata vero dolores et odio dolores facilisis ut eum est lobortis ea. Duo sea aliquyam stet duo et vulputate voluptua eirmod elitr accusam elitr tempor gubergren kasd voluptua duo stet. Ad eirmod autem dolor tincidunt no eum dolor et veniam gubergren. In eirmod sanctus.</section>
</div>

<div class="absolute h-2 w-79 top-63 left-7" v-mark.box.yellow="3"></div>
<div class="absolute h-2 w-79 bottom-34 left-7" v-mark.box.yellow="3"></div>
<div class="absolute h-35 w-2 top-66 left-7" v-mark.box.yellow="3"></div>
<div class="absolute h-35 w-2 top-66 left-84" v-mark.box.yellow="3"></div>
<div class="absolute h-1 w-10 top-71 left-111" v-mark.underline.yellow="3"></div>

<div class="absolute h-1 w-73 top-66 left-10" v-mark.box.purple="4"></div>
<div class="absolute h-1 w-73 bottom-37 left-10" v-mark.box.purple="4"></div>
<div class="absolute h-31 w-1 top-68 left-10" v-mark.box.purple="4"></div>
<div class="absolute h-31 w-1 top-68 left-82" v-mark.box.purple="4"></div>
<div class="absolute h-1 w-12 top-97 left-111" v-mark.underline.purple="4"></div>

---
layout: dynamic-image
image: ./images/space.jpg
equal: false
---

# Give them space! (2/3)
Picking sides

The number of parameters will define sides to which you want to give space.

<div v-click>

```css {*}{lines:true}
section {
  /* Same space to each side */
  margin: 12px;
  /* 5px top/bottom and 3px left/right */
  padding: 5px 3px;
}
article {
  /* 
    2px top, 5px right, 3px bottom, 6px left.
    Starting from the top and going clockwise */
   */
  margin: 2px 5px 3px 6px;
}
```

</div>

---
layout: dynamic-image
image: ./images/space.jpg
equal: false
---

# Give them space! (3/3)
Setting a value to a specific side

<div v-click>

```css{*}{lines:true}
section {
  margin-left: 15px;
  padding-bottom: 3px;
}
article {
  padding-right: 5px;
  margin-top: 10px;
}
```

</div>

<ComplementaryMessage bordered>In a nutshell: either pick <strong>margin</strong> or <strong>padding</strong> and suffix it with
<ul class="text-left ml-8">
  <li>-top</li>
  <li>-right</li>
  <li>-bottom</li>
  <li>-left</li>
</ul>
</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/space.jpg
equal: false
---

# Give them space! (bonus)
Center an element thanks to margins

```css {*}{lines:true}
.my-block {
  width: 100px;
  margin: 0 auto; /* Magic trick */
}
```

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: -360, y: -55}" class="absolute w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600">
  <div class="border border-grey-700 w-25 my-3 mx-auto p-2 text-xs">
    I have a fixed width and auto margins on the left and right sides.
  </div>
</div>

<div v-click>
  <Arrow x1="26" y1="300" x2="135" y2="300" color="red" width="1" two-way />
  <Arrow x1="238" y1="300" x2="345" y2="300" color="red" width="1" two-way />
</div>

<ComplementaryMessage bordered type="alert">For auto margins to work, you need to set a width (or max-width)!</ComplementaryMessage>
<ComplementaryMessage bordered type="alert">Auto margins won’t work for vertical alignment</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/borders.jpg
equal: false
left: false
---

# Borders (1/2)
Frame elements and make them stand out

```css {*}{lines:true}
.my-element {
  border: 1px solid #FF0000;
}
```

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 560, y: -80}" class="absolute p-4 max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600 text-xs">
  <div class="border border-red p-4">What a beautiful frame you get me!</div>
</div>

<ComplementaryMessage bordered>When setting a border, only the <strong>type</strong> of border is mandatory. By default the thickness is set to 3px and the color will be the same as the text’s</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/borders.jpg
equal: false
left: false
---

# Borders (2/2)
Making a very ugly frame

What if you wanted to set a different border for each side?

<div v-click>

```css {*}{lines:true}
.my-element {
  border-top-style: dashed;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: double;
  border-top-color: red;
  border-right-color: blue;
  border-bottom-color: purple;
  border-left-color: green;
  border-width: 2px;
}
```

</div>

<div v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 560, y: -150}" class="absolute p-4 max-w-1/3 bg-gray-700 text-white dark:text-gray-800 dark:bg-white rounded-md border-2 border-teal-600 text-xs">
  <div class="border-3 border-t-red border-r-blue border-b-purple border-l-green border-t-dashed border-b-dotted border-l-double p-4">No one understands me, I am unique!</div>
</div>

<v-click>

More on the [border](https://developer.mozilla.org/en-US/docs/Web/CSS/border) rules.

</v-click>

<img v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 350, y: -400}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/vomit.webp" alt="Dry heaving GIF" />

---
layout: intro
image: ./images/html.jpg
---

<h1 class="absolute left-12 bottom-12">Back to HTML</h1>
<p class="opacity-85 absolute left-12 bottom-6">Didn’t expect that, did you?</p>

<img src="/images/gifs/bttf.webp" class="absolute right-8 top-[10%] border-2 border-white rounded-md" alt="Back to the future Gif" />

---
layout: dynamic-image
image: ./images/audio.jpg
equal: false
---

# Adding sound to your site (1/2)
Make it loud for your users…or not.

In order to insert audio files in your pages, you need to cast a wide net regarding format compatibility.

<v-click>

Learn more on audio [formats](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs)

</v-click>
<table v-click class="text-sm leading-4">
  <tr>
    <th class="!font-bold">Browser</th>
    <th class="!font-bold">MP3</th>
    <th class="!font-bold">AAC</th>
    <th class="!font-bold">OGG</th>
    <th class="!font-bold">WAV</th>
  </tr>
  <tr>
    <td class="font-bold">Edge</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-minus" color="orange" /><br><span class="text-[8px]">Si &ge; v17</span></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
  <tr>
    <td class="font-bold">Chrome</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
  <tr>
    <td class="font-bold">Firefox</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-minus" color="orange" /><br><span class="!text-[8px]">Si codec installé et encapsulé dans MP4</span></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>  
  <tr>
    <td class="font-bold">Safari</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-x" color="red" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
  <tr>
    <td class="font-bold">Opera</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
</table>

---
layout: dynamic-image
image: ./images/audio.jpg
equal: false
---

# Adding sound to your site (2/2)
Make it loud for your users…or not.

### Single format
```html {*}{lines:true}
<audio src="./my/path/to/file.mp3" controls></audio>
```

### Multiple formats for better compatibility
```html {*}{lines:true}
<audio controls>
  <source src="./my/path/to/file.mp3"></source>
  <source src="./my/path/to/file.wav"></source>
  <source src="./my/path/to/file.aac"></source>
  <source src="./my/path/to/file.ogg"></source>
</audio>
```
<v-click>

More on the [audio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) element.

</v-click>

<div v-click class="mt-4 flex justify-center">
  <audio src="./media/ring.wav" controls class="h-8"></audio>
</div>

<ComplementaryMessage type="alert" bordered>The <strong>controls</strong> attribute does not have a value and has to be present for the control bar to appear.</ComplementaryMessage>

<img v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: -320, y: -350}" class="absolute rounded-md border-2 border-teal-600 h-56" src="/images/gifs/kid-dancing.webp" alt="Kid dancing GIF" />

---
layout: dynamic-image
image: ./images/video.jpg
equal: false
left: false
---

# Adding video to your site (1/2)
Grab the popcorn and enjoy.

As you can imagine, it’s best to use multiple formats for the same video for a better compatibility.

<v-click>

Learn more on video [formats](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs)

</v-click>
<table v-click class="text-sm leading-4">
  <tr>
    <th class="!font-bold">Browser</th>
    <th class="!font-bold">H.264</th>
    <th class="!font-bold">OGG Theora</th>
    <th class="!font-bold">WebM</th>
  </tr>
  <tr>
    <td class="font-bold">Edge</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-x" color="red" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
  <tr>
    <td class="font-bold">Chrome</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-x" color="red" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
  <tr>
    <td class="font-bold">Firefox</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>  
  <tr>
    <td class="font-bold">Safari</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-x" color="red" /></td>
    <td><light-icon icon="square-minus" color="orange" /><br><span class="text-[8px]">Si &ge; v16 ou &ge; 12.1 si codec installé</span></td>
  </tr>
  <tr>
    <td class="font-bold">Opera</td>
    <td><light-icon icon="square-check" color="green" /></td>
    <td><light-icon icon="square-x" color="red" /></td>
    <td><light-icon icon="square-check" color="green" /></td>
  </tr>
</table>

---
layout: dynamic-image
image: ./images/video.jpg
equal: false
left: false
---

# Adding video to your site (2/2)
Grab the popcorn and enjoy.

### Single format
```html {*}{lines:true}
<video src="./my/path/to/file.mp4" controls></video>
```

### Multiple formats for better compatibility
```html {*}{lines:true}
<video controls>
  <source src="./my/path/to/file.mp4"></source>
  <source src="./my/path/to/file.webm"></source>
  <source src="./my/path/to/file.ogv"></source>
</video>
```
<v-click>

More on the [video](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video) element.

</v-click>

<video v-motion v-click :initial="{x: 999, y: -999}" :enter="{x: 570, y: -225}" class="absolute rounded-md border-2 border-teal-600 max-w-1/3" src="/media/video.mp4" controls></video>

<ComplementaryMessage type="alert" bordered>The <strong>controls</strong> attribute does not have a value and has to be present for the control bar to appear.</ComplementaryMessage>

---
layout: dynamic-image
image: ./images/figure.jpg
equal: false
---

# Figuring things out
A good way to caption your elements

If you need to add a caption to your videos, illustrations, pieces of code, etc. There is an ~~app~~ element for that.

<div v-click>

```html {*}{lines:true}
<figure>
  <img src="/path/to/img.jpg"/>
  <figcaption>That’s a very grumpy cat!</figcaption>
</figure>
```

</div>

<figure class="mt-4 text-sm" v-click>
  <img class="h-40" src="/images/grumpy_cat.jpg"/>
  <figcaption>That’s a very grumpy cat!</figcaption>
</figure>

---
layout: intro
image: ./images/quiz.jpg
---

<h1 class="absolute left-12 bottom-12">Quiz time</h1>

<img src="/images/gifs/deja-vu.webp" class="absolute right-12 top-[30%] border-2 border-white rounded-md" alt="Déjà vu Gif" />

---
layout: dynamic-image
image: ./images/question.jpg
equal: false
---

# Get creative
This is almost over don’t worry

<v-clicks>

- Create a block with a width of 80% and a red dotted border of 2px
- Add a centered important heading. It should be green
- Make a superb image float on the left
- Create two paragraphs with a font set to 12px. The second paragraph should **not** be affected by the floating image
- You are free to use **ids** and/or **classes**

</v-clicks>

---
layout: dynamic-image
image: ./images/time.jpg
equal: false
left: false
---

# Time’s up!
Who wants to write some code?

<Transform v-click="1" scale="0.9">

```html {*|all|1,6|2|3|4-5|5|all}{lines:true,at:1}
<div id="container">
  <h2>My great heading</h2>
  <img src="images/grumpy_cat.jpg" alt="This is a very grumpy cat" />
  <p>This cat is surely not happy</p>
  <p class="last-paragraph">Why is it always in a bad mood?</p>
</div>
```

</Transform>
<Transform v-click="1" scale="0.9">

```css {*|all|1-4|5-8|9-11|12-14|15-17|all}{lines:true,at:1}
#container {
  width: 80%;
  border: 2px dotted red;
}
h2 {
  text-align: center;
  color: green;
}
img {
  float: left;
}
p {
  font-size: 12px;
}
.last-paragraph {
  clear: left;
}
```

</Transform>

<div v-motion v-click="8" :initial="{x: 999, y: -999}" :enter="{x: 550, y: -350}" class="absolute p-2 rounded-md bg-white border-2 border-teal-600 w-1/3">
  <div class="w-4/5 border-2 border-red border-dotted text-gray-800">
    <h2 class="text-green text-xl">My great heading</h2>
    <img class="float-left h-30" src="/images/grumpy_cat.jpg" alt="This is a very grumpy cat" />
    <p class="text-xs !my-1">This cat is surely not happy</p>
    <p class="clear-left text-xs">Why is it always in a bad mood?</p>
  </div>
</div>

---
layout: intro
image: ./images/thinker.jpg
---

<div class="absolute inset-0 flex justify-center items-center">
  <h1 class="text-6xl !text-white font-500">Questions?</h1>
</div>

<div class="absolute bottom-4 right-4 opacity-50 text-sm italic">
  © Unsplash<br>© Giphy<br>© imgflip
</div>
