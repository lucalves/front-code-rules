<img src="https://user-images.githubusercontent.com/17712401/90824368-b5a83080-e30d-11ea-8516-d324338f43a5.png" width="110px" height="100px" align="center">

# My Front-end Code Rules

The following document describes the rules of writing in development languages that I use: HTML, CSS and JavaScript.

The idea of this repository is not to be a complete code guide. Only to have a place for myself and other developers who participate in my projects able to inform the coding standards used.

As this is a new document, some rules may not have been applied in old projects.

This is a live document and changes can occur at any time.

## Summary

1. [Commits](#commits)
1. [HTML](#html)
1. [CSS](#css)

<a name="commits"></a>
## 1. Commits

To facilitate the contribution by anyone in a project, all commit messages, pull request title or issues discussion must be in **English**.

Before commit adjusts in project, check if exists an open issue and make references for this issue using '#' in your commit message.

```javascript
// Good
git commit -m "Add placeholder on input #10"

// Bad
git commit -m "Add placeholder on input"
```

<a name="html"></a>
## 2. HTML

The main influence for the HTML rules is the [Code Guide](http://diegoeis.github.io/code-guide/).

### HTML Summary

1. [HTML Syntax](#html-syntax)
1. [HTML Comments](#html-comments)
1. [HTML Character Encoding](#html-encoding)
1. [HTML Attribute Order](#html-attribute-order)
1. [HTML Performance](#html-performance)
1. [HTML Base Code](#html-base)

<a name="html-syntax"></a>
### 2.1. HTML Syntax

Use soft tabs with two spaces. You can configure your editor for this.

```html
<!-- Good -->
<nav class="navbar">
  <ul class="nav">
    <li class="nav-item">
      <a class="nav-link">

<!-- Bad-->
<nav class="navbar">
      <ul class="nav">
            <li class="nav-item">
                  <a class="nav-link">
```

Always use double quotes.

```html
<!-- Good -->
<main class="main">

<!-- Bad-->
<div class='main'>
```

Don't include a `/` in self-closing elements.

```html
<!-- Good -->
<hr>

<!-- Bad-->
<hr />
```

Separate block element by a blank line and agroup the inners block elements.

```html
<!-- Good -->
<ul class="nav-tabs">
  <li>...</li>
  <li>...</li>
  <li>...</li>
  <li>...</li>
</ul>

<div class="tab-content">
  ...
</div>

<!-- Bad-->
<ul class="nav-tabs">

  <li>...</li>

  <li>...</li>

  <li>...</li>

  <li>...</li>

</ul>
<div class="tab-content">
  ...
</div>
```

<a name="html-comments"></a>
### 2.2. HTML Comments

Follow this rule to add comments in HTML.

```html
<!-- This is a good example -->
<!-- /Closing a good example -->
```

<a name="html-encoding"></a>
### 2.3. HTML Character Encoding

Always use UTF-8 for character encoding.

```html
<head>
  <meta charset="UTF-8">
</head>
```

<a name="html-attribute-order"></a>
### 2.4. HTML Attribute Order

HTML attributes should be in this order for facilitate the reading.

1. `class`
1. `id`, `name`
1. `data-*`
1. `src`, `for`, `type`, `href`
1. `title`, `alt`
1. `aria-*`, `role`

```html
<a class="..." id="..." data-modal="#overlay" href="#">

<input class="form-control" type="text">

<img class="img-rounded" src="..." alt="...">
```

<a name="html-performance"></a>
### 2.5. HTML Performance

No need to specify a type when including CSS and JavaScript files as `text/css` and `text/JavaScript`.

```html
<!-- Good -->
<link rel="stylesheet" href="assets/css/style.css">
<script src="scripts.min.js"></script>

<!-- Bad -->
<link rel="stylesheet" href="assets/css/style.css" type="text/css">
<script src="scripts.min.js" type="text/JavaScript"></script>
</head>
<body>
```

For a better performance, all JavaScripts files must be at the end of the code. Before closing the `<body>`.

```html
<!-- Good -->
<script src="scripts.min.js"></script>
</body>

<!-- Bad -->
<script src="scripts.min.js"></script>
</head>
<body>
```

Always minify the code in projects only in HTML. Task builders like [Grunt](http://gruntjs.com/) leaves this easier.

```html
<!-- Good -->
<html><head>...</head><body><div class="container">...</div></body></html>

<!-- Bad -->
<html>
  <head>
    ...
  </head>
  <body>
    <div class="container">
      ...
    </div>
  </body>
</html>
```

<a name="html-base"></a>
### 2.6. HTML Base Code

The following code is a HTML base for faster start the projects.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="format-detection" content="telephone=no">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <link rel="shortcut icon" href="assets/ico/favicon.ico">
  <link rel="logo" type="image/svg" href="assets/img/logo/logo.svg">
  <link rel="stylesheet" href="assets/css/style.css">
  <title></title>
</head>
<body>
</body>
</html>
```

For give support a olds Internet Explorer...

```html
<!DOCTYPE html>
<!--[if IE]><![endif]-->
<!--[if IE 7 ]> <html lang="en" class="ie7">    <![endif]-->
<!--[if IE 8 ]>    <html lang="en" class="ie8">    <![endif]-->
<!--[if IE 9 ]>    <html lang="en" class="ie9">    <![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--><html lang="en"><!--<![endif]-->
<head>
...
```

<a name="css"></a>
## 3. CSS

### 3.1 CSS Sumary

1. [CSS Syntax](#css-syntax)
1. [CSS Declaration Order](#css-order)
1. [CSS Class Name](#css-class-name)
1. [CSS Performance](#css-performance)
1. [CSS Media Queries](#css-media-queries) 
