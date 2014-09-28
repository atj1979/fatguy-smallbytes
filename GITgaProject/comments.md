## General things to keep in mind
- image names: it's almost always best to keep asset names all lower case. Some file systems don't distinguish differences in case so if you had an image named AMAZONsymbol.jpg and amazonsymbol.jpb, it's kind of a crapshoot.

- CSS class names: the broad convention isn't to camel case classnames, but rather use space-separated names. ie: `.tableData` would be more appropriately named `.table-data`. it's really nit-picky, I know.

- CSS positioning is tricky: see [MDN CSS Position](https://developer.mozilla.org/en-US/docs/Web/CSS/position), but you'll find that your fixed position table moves along with the page as you scroll, whereas the absolutely positioned one doesn't.

- HTML: try and use semantic elements. `<div>`s for headlines, probably aren't the best choice. Blocks of text, like:
```
I've taken just a few coureses concerning HTML and CSS.
I'm McLovin it!
I have been working as a full time Field Engineer for GE.
I've coordinated the maintenance, repair as well as designed and implemented  mondifications to many High Voltage systems at companies like:
```
should probably be wrapped in a `<p>` tag at the very least.

- HTML: avoid declaring any visual properties as attributes on an HTML element.. that's what CSS is for!
for instance: `<img class="topRight" src="Pic/RaidersEmblem.jpg" align="right" vertical-align="top">` shouldn't have the `align` and `vertical-align` properties. You could probably just apply `float: right;` to the corresponding css class in this case.

- HTML: indentation is your friend.  Always indent one tab for each nested tag so you can easily see where things begin and end: example:
```
<h1>Headline</h1>
<p>Sibling paragraph</p>
<div>
  <figure>
    <img src "..." />
    <figcaption>
      <span>some caption about the image</span>
    </figcaption>
  </figure>
</div>
...

```
- The markup for the tables looks good for the most part.. just keep that form in mind for the rest of the document.
