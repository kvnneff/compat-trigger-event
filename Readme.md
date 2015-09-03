# compat-trigger-event

[![npm][npm-image]][npm-url]
[![travis][travis-image]][travis-url]

[npm-image]: https://img.shields.io/npm/v/compat-trigger-event.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/compat-trigger-event
[travis-image]: https://img.shields.io/travis/kvnneff/compat-trigger-event.svg?style=flat-square
[travis-url]: https://travis-ci.org/kvnneff/compat-trigger-event

[trigger-event](https://github.com/adamsanderson/trigger-event) forked to ensure compatibility with both Duo and Browserify.

Trigger native DOM events.  This is primarily useful for testing, or for
triggering common DOM events such as the `change` event for custom components.

## Installation

    npm install compat-trigger-event

## API

### trigger(el, name, options)

Triggers the `name` event on `el`.  Options may be passed in to customize the event.

HTMLEvents support the following options:

    bubbles
    cancelable

MouseEvents support the following options:

    bubbles
    cancelable
    detail (number of clicks)
    screenX / screenY
    clientX / clientY
    ctrlKey
    altKey
    shiftKey
    metaKey
    button (mouse button)

Any other event will be triggered as a [CustomEvent](https://developer.mozilla.org/en-US/docs/DOM/Event/CustomEvent).

See the [W3C Event Spec](http://www.w3.org/TR/DOM-Level-2-Events/events.html) for more details.

Where sensible, sane defaults will be filled in.  See the list of event
types for supported events.

## Attribution

This is loosely based on [kangax](https://github.com/kangax)'s [event.simulate.js](https://github.com/kangax/protolicious/blob/master/event.simulate.js).

Contributions from:

* [Tim Oxley](https://github.com/timoxley)
* [Manuel Stofer](https://github.com/manuelstofer)
* [John Syrinek](https://github.com/johntron)
