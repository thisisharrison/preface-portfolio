# Key Takeaways

## HTML

-   Skeleton of your website
-   `<head>` contains all non-visible tags

    -   Add CSS file (created by you or a library) by adding `<link>`
    -   Add styles with `<style>`
    -   Add JavaScript with `<script>`

-   `body` contains all visible tags
    -   Some tags have `open` and `close`, for eg. `<h1>Hello</h1>`
    -   Some tags do not, for eg. `<img src="cat.jpg" />`
    -   Tags have attributes:
        -   General ones:
            -   `class`
            -   `id`
            -   `style`
        -   Specific ones:
            -   `a` anchor tags have `href` to point to a link
            -   `input` input tags have `type` to specify input format `text`, `date`, `number`, `file` etc.
    -   Lastly we looked at `form`:
        -   Contains `label`, `input`. Once a `form` is submitted, _by default_ the page reloads
        -   Typically steps to handle form submissions are:
            1. Validate Input
            2. Submit Input
                1. In Todo List example, "submit" means showing the item on screen
            3. Clear Input
    -   Other JavaScript can be added _at the bottom_ of `body` before closing tags
-   Homework Reading:
    -   [https://www.w3schools.com/TAGS/default.ASP](https://www.w3schools.com/TAGS/default.ASP)

---

## CSS

-   Specificity and Selectors

    -   inline:
        -   HTML and CSS: `<h1 style="color: red; font-weight: 800">Hello</h1>`
    -   id:
        -   HTML: `<button id="new-task">New Task</button>`
        -   CSS: `#new-task`
    -   class:
        -   HTML: `<a href="index.html" class="nav-item active">Home</a>`
        -   CSS `.nav-item` or `.nav-item.active`
    -   Homework exercise:
        -   [CSS Diner](https://flukeout.github.io/)

-   Spacing

    -   Content:
        -   Analogy: Your bones. _How tall are you? How big are your hands? etc._
        -   Code:
            -   If it's text, then it's `font-size`
            -   Otherwise, you may have to define it yourself with `width`, `height`. (Reference: card page)
    -   Padding
        -   Analogy: Your muscle. _How much muscle do you have?_
        -   Code:
            -   Try changing `padding` of a `button`
    -   Border
        -   Analogy: Your clothes. _How many layers are you wearing? What kind of style? What color?_
        -   Homework reading:
            -   [https://css-tricks.com/almanac/properties/b/border/](https://css-tricks.com/almanac/properties/b/border/)
    -   Margin
        -   Analogy: How far are you from your friends? _A foot apart? An arm apart? 1m apart?_
        -   Homework reading:
            -   [https://developer.mozilla.org/en-US/docs/Web/CSS/margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)

-   Units of measurement: Absolute vs Relative

    -   Homework Reading:
        -   [https://www.w3schools.com/cssref/css_units.asp](https://www.w3schools.com/cssref/css_units.asp)

-   Display properties

    -   `box`, `inline`, `none`, `flex`
        -   First two are somewhat default. For eg., `<p>` is `box` you don't have to specify it. `<a href>` is `inline` you don't have to specify it.
        -   We used `none` in the todo page.
        -   We used `flex` in the gallery page.
            -   Homework reading:
                -   [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
            -   Homework exercise:
                -   [Flexbox Froggy](https://flexboxfroggy.com/)

-   Bootstrap

    -   How to use the [documentation](https://getbootstrap.com/docs/5.1/getting-started/introduction/)?
        1. What are you trying to change? _a button? a form? an input? the page width?_
        2. Search that thing in the search box.
        3. Read the `class` names being used in the example. For eg. `btn btn-primary`.
        4. Apply to your HTML tag.
    -   How to override the Bootstrap style?
        -   `inline` CSS
        -   Find the `class` name and update it in your CSS file
        -   Use `id` instead

-   Homework exercise (these are quite tough):
    -   [100 Days of CSS](https://100dayscss.com/)
    -   [CSS Battle](https://cssbattle.dev/)

---

## JavaScript

-   Querying (searching) the dom

    -   querySelector, querySelectorAll: CSS selectors (id: #name, class: .name, tag: name)
    -   getElementByID

-   Manipulating the dom

    -   `<A DOM Element>`.innerText
        -   eg. `document.querySelector('button').innerText = "Sign Up"`
    -   `<A DOM Element>`.style.<A CSS Property, for eg. display>
        -   eg. `document.querySelector('button').style.backgroundColor = "green"`
    -   `<A DOM Element>`.innerHTML
        -   eg. `document.querySelector('ol').innerHTML += "<li>New Item</li>"`

-   Scheduling / trigger event listeners

    -   `<A DOM Element>`.addEventListener('click', function)
        -   eg. `document.querySelector('button').addEventListener('click', function () { alert("hi") })`
    -   `<A DOM Element>`.onclick = function
        -   eg. `document.querySelector('button').onclick = alert("hi")`
    -   Method 1: `addEventListener('hover', 'click', 'scroll', 'submit'... )`
    -   Method 2: `onclick, onsubmit, onscroll, onhover`

-   Refer to [koans](https://github.com/thisisharrison/preface-koans) for more JS notes.

-   Homework exercise
    -   [https://edabit.com/challenges/javascript](https://edabit.com/challenges/javascript)
    -   [https://www.codewars.com/collections/javascript-basics-2](https://www.codewars.com/collections/javascript-basics-2)
    -   These can also be quite tough:
        -   [https://www.hackerrank.com/challenges/js10-hello-world/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-hello-world/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-data-types/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-data-types/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-arithmetic-operators/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-arithmetic-operators/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-function/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-function/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-let-and-const/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-let-and-const/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-if-else/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-if-else/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-loops/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-loops/problem?isFullScreen=true)
        -   [https://www.hackerrank.com/challenges/js10-arrays/problem?isFullScreen=true](https://www.hackerrank.com/challenges/js10-arrays/problem?isFullScreen=true)
