
# url.js

 [![Version](https://img.shields.io/npm/v/urljs.svg)](https://www.npmjs.com/package/urljs) [![Downloads](https://img.shields.io/npm/dt/urljs.svg)](https://www.npmjs.com/package/urljs)

> A lightweight JavaScript library to manipulate the page url.

## Demo

Browse the demos on http://jillix.github.io/url.js/


[![](http://i.imgur.com/BYxaxU1.png)](http://jillix.github.io/url.js/)

## CDN

The library is available on [CDNJS](https://cdnjs.com/libraries/urljs) as well. To use it, just do:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/urljs/1.2.0/url.min.js"></script>
```
## Usage
```html
<script src="path/to/url.js"></script>
<!-- or use the cdn
<script src="https://cdnjs.cloudflare.com/ajax/libs/urljs/1.2.0/url.min.js"></script>
-->
<script>
    Url.updateSearchParam("answer", 42);
</script>
```
## CommonJS-compatible

The library is CommonJS-compatible. You can `require("url.js")` in your files.


## :cloud: Installation


Check out the [`src`](/src) directory to download the needed files and include them on your page.

If you're using this module in a CommonJS environment, you can install it from `npm` and `require` it:

```sh
$ npm i --save urljs
```


## :memo: Documentation


### `queryString(name, notDecoded)`
Finds the value of parameter passed in first argument.

#### Params
- **String** `name`: The parameter name.
- **Boolean** `notDecoded`: If `true`, the result will be encoded.

#### Return
- **String|Boolean|Undefined** The parameter value (as string), `true` if the parameter is there, but doesn't have a value, or
`undefined` if it is missing.

### `parseQuery(search)`
Parses a string as querystring. Like the `queryString` method does, if
the parameter is there, but it doesn't have a value, the value will
be `true`.

#### Params
- **String** `search`: An optional string that should be parsed (default: `window.location.search`).

#### Return
- **Object** The parsed querystring. Note this will contain empty strings for

### `stringify(queryObj)`
Stringifies a query object.

#### Params
- **Object** `queryObj`: The object that should be stringified.

#### Return
- **String** The stringified value of `queryObj` object.

### `updateSearchParam(param, value, push, triggerPopState)`
Adds, updates or deletes a parameter (without page refresh).

#### Params
- **String|Object** `param`: The parameter name or name-value pairs as object.
- **String** `value`: The parameter value. If `undefined`, the parameter will be removed.
- **Boolean** `push`: If `true`, the page will be kept in the history, otherwise the location will be changed but by pressing the back button
will not bring you to the old location.
- **Boolean** `triggerPopState`: Triggers the popstate handlers (by default falsly).

#### Return
- **Url** The `Url` object.

### `getLocation()`
Returns the page url, but not including the domain name.

#### Return
- **String** The page url (without domain).

### `hash(newHash, triggerPopState)`
Sets/gets the hash value.

#### Params
- **String** `newHash`: The hash to set.
- **Boolean** `triggerPopState`: Triggers the popstate handlers (by default falsly).

#### Return
- **String** The location hash.

### `_updateAll(s, push, triggerPopState)`
Update the full url (pathname, search, hash).

#### Params
- **String** `s`: The new url to set.
- **Boolean** `push`: If `true`, the page will be kept in the history, otherwise the location will be changed but by pressing the back button
will not bring you to the old location.
- **Boolean** `triggerPopState`: Triggers the popstate handlers (by default falsly).

#### Return
- **String** The set url.

### `getLocation(pathname, push, triggerPopState)`
pathname
Sets/gets the pathname.

#### Params
- **String** `pathname`: The pathname to set.
- **Boolean** `push`: If `true`, the page will be kept in the history, otherwise the location will be changed but by pressing the back button
will not bring you to the old location.
- **Boolean** `triggerPopState`: Triggers the popstate handlers (by default falsly).

#### Return
- **String** The set url.

### `triggerPopStateCb()`
Calls the popstate handlers.

### `onPopState(cb)`
Adds a popstate handler.

#### Params
- **Function** `cb`: The callback function.

### `removeHash(push, trigger)`
Removes the hash from the url.

#### Params
- **Boolean** `push`: If `true`, the page will be kept in the history, otherwise the location will be changed but by pressing the back button
will not bring you to the old location.
- **Boolean** `trigger`: Triggers the popstate handlers (by default falsly).

### `removeQuery(push, trigger)`
Removes the querystring parameters from the url.

#### Params
- **Boolean** `push`: If `true`, the page will be kept in the history, otherwise the location will be changed but by pressing the back button
will not bring you to the old location.
- **Boolean** `trigger`: Triggers the popstate handlers (by default falsly).



## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :scroll: License

[MIT][license] © [jillix][website]

[license]: http://showalicense.com/?fullname=jillix%20%3Ccontact%40jillix.com%3E%20(http%3A%2F%2Fjillix.com)&year=2014#license-mit
[website]: http://jillix.com
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
