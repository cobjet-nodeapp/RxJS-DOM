### `Rx.DOM.mouseleave(element, [selector])`
[&#x24C8;](https://github.com/Reactive-Extensions/RxJS-DOM/blob/master/src/events.js "View in source") 

Creates an observable sequence by adding an event listener to the matching DOMElement or DOMNodeList for the `mouseleave` event.

#### Arguments
1. `element` *(`Any`)*: The DOMElement, DOMNodeList to attach a listener. 
2. `[selector]` *(`Function`)*: A selector which takes the arguments from the event handler to produce a single item to yield on next.

#### Returns
*(`Observable`)*: An observable sequence of events from the specified element and the `mouseleave` event.

#### Example

```js
var input = document.getElementById('input');

var source = Rx.DOM.mouseleave(input);

var subscription = source.subscribe(
    function (x) {
        console.log('Next!');
    },
    function (err) {
        console.log('Error: ' + err);   
    },
    function () {
        console.log('Completed');   
    });
```

### Location

File:
- [`/src/events.js`](https://github.com/Reactive-Extensions/RxJS-DOM/blob/master/src/events.js)

Dist:
- [`rx.dom.js`](https://github.com/Reactive-Extensions/RxJS-DOM/blob/master/dist/rx.dom.js) | - [`rx.dom.compat.js`](https://github.com/Reactive-Extensions/RxJS-DOM/blob/master/dist/rx.dom.compat.js)

Prerequisites:
- If using `rx.js`
  - [`rx.js`](https://github.com/Reactive-Extensions/RxJS/blob/master/dist/rx.js) | [`rx.compat.js`](https://github.com/Reactive-Extensions/RxJS/blob/master/dist/rx.compat.js)
  - [`rx.binding.js`](https://github.com/Reactive-Extensions/RxJS/blob/master/dist/rx.binding.js)
- [`rx.lite.js`](https://github.com/Reactive-Extensions/RxJS/blob/master/rx.lite.js) | [`rx.lite.compat.js`](https://github.com/Reactive-Extensions/RxJS/blob/master/rx.lite.compat.js)

NPM Packages:
- [`rx-dom`](https://preview.npmjs.com/package/rx-dom)

NuGet Packages:
- [`RxJS-Bridges-HTML`](http://www.nuget.org/packages/RxJS-Bridges-HTML/)

Unit Tests:
- [`/tests/events.js`](https://github.com/Reactive-Extensions/RxJS-DOM/blob/master/tests/events.js)
