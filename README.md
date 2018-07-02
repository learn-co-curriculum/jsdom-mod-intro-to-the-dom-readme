# Introduction to the DOM

## Problem Statement

Previously we've learned that JavaScript was _born_ in the browser along with
the Document Object Model (DOM). We've acquired some JavaScript sight words,
let's balance things out by learning about the DOM.

## Objectives

1. Identify the Document Object Model (DOM)
2. Explain How the DOM is Created
3. Identify the DOM as JavaScript _objects_

## Identify the Document Object Model

Let's start with a biology metaphor. Your DNA represents a code-based version
of you. The DOM represents a code-based version of a web page. If something
edits your DNA, <span style="text-decoration: line-through">mutant powers</span> changes will be made in your body. Similarly,
if something changes the DOM, what's displayed in the browser _changes as
well_.

## Explain How the DOM is Created

The DOM is created when the page loads from the HTML that the web server
provides the browser. Let's step through that process.

> **NOTE**: We use [Google Chrome][chrome].

### Change the URL of a web page to view the source

1. In a Google Chrome browser, go to the URL `https://learn.co/tracks/javascript-with-style`
2. To see the HTML of that page, add `view-source:` to the front of the URL.
   The complete final URL will be `view-source:https://learn.co/tracks/javascript-with-style`.
   By using the `view-source` URL prefix, all the page's source HTML appears.
   It will look something like this:
   ![html-source](https://s3.amazonaws.com/learn-verified/html-javascript-lesson.png)
3. The browser reads this HTML, along with CSS and JavaScript defined in
   `<script>` or `<link>` tags, to create the DOM _inside the browser_. At this
   point, nothing is displayed on the screen. This time when nothing is
   displayed is _very brief_ so our human eyes never really catch it.
4. The browser _then_ uses the DOM _object_ to create the rendered page. While we
   often learn that browsers "display HTML" that's not _exactly_ accurate.
   Browsers use the HTML to create a "middleman" that they, _in turn_ use to
   display the structured and styled content

Recalling our biology metaphor, adding elements, removing elements, changing
elements in the DOM changes what you see in the browser screen. We'll explore
this in a later lesson.

## Identify the DOM as JavaScript _objects_

Recall that JavaScript is Object-Oriented. The DOM is available inside Chrome
through two _variables_: `window` and `document`.

The `window` variable points to an _object_ the represents Chrome's information
about the browser, well, "window." It has many functions, but the main one is
"it's a place where everything is." Not to be Zen here, but a browser without
`window` is like the Universe before the Big Bang: there's just..._nothing_
everywhere where it wasn't. It's in the `window` that the Things are defined
(`Array` and `Number`).

In the `window`, JavaScript also tracks operating system browser information
like:

```javascript
window.innerHeight;
// returns the inner height of the browser window.
```

Like all objects, `window` also has _methods_.  We won't use them too much.
We don't want to mess with the container of everything that is or operating
system stuff.

We want, rather, to change content. We're going to focus on an object called
`document`.

As an _object_, `document` has _properties_:

```javascript
document.URL //=> http://www.flatironschool.com
```

As an _object_ `document` also has _methods_:

```javascript
document.write("Moof") //=> Removes all existing DOM content, replaces it with "Moof"
```

The _methods_ and _properties_ that the DOM provides via its objects is called
the DOM's "Application Programming Interface", or "API." It's just a programming
word that you're likely to see online. But it just means "the things that these
objects know how to do."

## Resources

- [CSS Tricks - What is the DOM?](https://css-tricks.com/dom/)
- [MDN - The DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

## Conclusion

In this lesson we've met our partner, the DOM, a JavaScript object that is a
representation of the HTML, CSS and JavaScript loaded by the browser when we
visit a page. We normally interact with it through the `document` object.
Because it is the "source of truth" for what browsers display, changes to the
DOM create changes in the browser screen.

[chrome]: https://www.google.com/chrome/browser/desktop/index.html
