Let's create our own jQuery. Let's call it CillasQuery.

We'll need something like this:

```
cq('div')
```

that returns every `div` element in the document. Over those elements, we'll be able to chain a series of functions to help with their manipulation.

`.addClass(className)`

`.removeClass(className)`

`.hasClass(className)`

`.toggleClass(className)`

`.append(el)`

`.find(selector)`

`.empty()`

`.attr('src')` returns `src` attribute.

`.attr('src', 'https://carto.com')` sets `src` attribute.

`.css(rulename)` returns element's css rule value.

`.css(rulename, value)` sets elements css rul value.

`.text()` returns element's text.

`.text('some text)` sets element's text.

`.parent()` returns the parent of the element.

`.remove()` remove the element from the document.

`.children()`

`.clone()`

`.create('div')` creates a DIV element.

`.on(eventName, eventHandler)`

`off(eventName, eventHandler)`

These functions must be chainable.

cq('div')
  .find('a')
  .attr('src', 'https://carto.com')
  .on('click', onLinkClicked)
  .text('Go to CARTO');

Let's keep it simpler in a first round, having `cq()` to return only the first element that corresponds to the selector.
