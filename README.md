# swipelistener-js

Small JS plugin to handle swipe gestures.

### [Demo](https://yurayarosh.github.io/swipelistener-js/)

### Install

```bash
$ yarn add swipelistener-js
```

```js
import Swipe from 'swipelistener-js/src/main'

const swipe = new Swipe(el, options)
swipe.init()

function up() {
  printText('Swipe up')
}

swipe
  .on('swipeup', up)
  .on('swipedown', () => {
    printText('Swipe down')
  })

swipe.off('swipeup', up)
```

### Options

Standart options
```js
{
  moveCallbacks: false,
  resistance: 0,
}
```

### Methods

```js
swipe.on(eventName, callback)
swipe.off(eventName, callback)
swipe.destroy() 
```

### Events names

* swipeup
* swipedown
* swipeleft
* swiperight
* moveup
* movedown
* moveleft
* moveright
