# html-ll

![html-ll](https://raw.githubusercontent.com/vs-123/html-ll/main/ll-html-icon.png?token=AES3AMRNEU3BKGUXWYCE6X3APUKOA)

## Introduction:
**html-ll** is a lined-language designed for writing descriptive html code with ease.

## Quick Start:
Let's suppose, I want to make an html file with reset css, that has a `<h1>` with the text `Hello World`.
So I would create a file `main.ll` (the file name is arbitrary).

In `main.ll`, I would write the following code.
```
start html
  start head
    reset-css
    start title
      text hello world
    end title
  end head
  
  start body
    start h1
      text Hello World
    end h1
  end body
end html
```
To compile the html-ll code, use the following command.
```
$ ./html-ll main.ll output.html
```
It shows nothing, which means the `main.ll` file was compiled successfully.
Listing the contents of the current directory using the `ls` command gives the following result.
```
$ ls
main.ll output.html
```
There is the `output.html` file.
Now if we check the contents of the file, it has the following code:-
```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* RESET CSS */
      html, body, div, span, applet, object, iframe,
      h1, h2, h3, h4, h5, h6, p, blockquote, pre,
      a, abbr, acronym, address, big, cite, code,
      del, dfn, em, img, ins, kbd, q, s, samp,
      small, strike, strong, sub, sup, tt, var,
      b, u, i, center,
      dl, dt, dd, ol, ul, li,
      fieldset, form, label, legend,
      table, caption, tbody, tfoot, thead, tr, th, td,
      article, aside, canvas, details, embed,
      figure, figcaption, footer, header, hgroup,
      menu, nav, output, ruby, section, summary,
      time, mark, audio, video {
      margin: 0;
      padding: 0;
      border: 0;
      font-size: 100%;
      font: inherit;
      vertical-align: baseline;
      }
      article, aside, details, figcaption, figure,
      footer, header, hgroup, menu, nav, section {
      display: block;
      }
      body {
      line-height: 1;
      }
      ol, ul {
      list-style: none;
      }
      blockquote, q {
      quotes: none;
      }
      blockquote:before, blockquote:after,
      q:before, q:after {
      content: '';
      content: none;
      }
      table {
      border-collapse: collapse;
      border-spacing: 0;
      }
      *:focus{
      outline:0;
      }
    </style>
    <title>
      hello world
    </title>
  </head>
  <body>
    <h1>
      Hello World
    </h1>
  </body>
</html>
```

## Commands
For now (since 19 April 2021), there are 6 commands:
 - `start <tag> info: Makes the starting tag.`
 - `end <tag> info: Makes the closing tag.`
 - `text <text> info: Makes arbitrary text.`
 - `comment <comment> info: A comment (it is reflected in the compiled HTML code)`
 - `self-close <tag> info: Makes a self-closing tag`
 - `reset-css info: Inserts reset css code`
 - `import-js <url> info: Imports js code from the given URL`
