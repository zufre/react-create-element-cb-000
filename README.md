# React createElement()

## Objectives

1. Describe how to call `React.createElement()`
2. Describe how we can build elements out of other React elements

## Overview

First things first, have students include React in this lab: add

```html
<script src="node_modules/react/dist/react.js"></script>
<script src="node_modules/react-dom/react-dom.js"></script>
```

Just below the closing `</main>` tag in `index.html`.

We don't want to do this for them. It's really important that students start to
get an intuitive sense for how JavaScript gets to the page — it's not magic,
it's just `<script>`. (This understanding will be vital for introducing Babel,
Webpack, etc.)

Now have them create something simple — a contact list? a poem? — **using plain
ol' JavaScript**. We don't want to introduce JSX yet.

Start with the heading:

```javascript
const heading = React.createElement('h1', {}, 'People')
```

and render it

```javascript
ReactDOM.render(heading, document.getElementById('main'))
```

Now add children:

```javascript
const list =
  React.createElement('div', {},
    React.createElement('h1', {}, 'People'),
    React.createElement('ul', {},
      React.createElement('li', {}, 'Someone Cool'),
      // etc.
      ))

ReactDOM.render(list, document.getElementById('main'))
```

And keep building from there.

## Resources

- [Raw React](http://jamesknelson.com/learn-raw-react-no-jsx-flux-es6-webpack/)
