# getter-setter

[![Build Status](https://secure.travis-ci.org/techjacker/getter-setter.png)](http://travis-ci.org/techjacker/getter-setter)

### Install
```Shell
npm install getter-setter
```

### 2 methods for decorating objects with getters and setters:
1. __proto__ method (only works in node.js or v8 browsers)
2. underscore extend method (works in all browsers as well as node.js)


## Example
```JavaScript
// or with ...extend does the same thing
// var decorate = require('getter-setter').extend;

var decorate = require('getter-setter').proto;
var obj = {
	hello: 'world'
};

decorate(obj);

// outputs "world"
console.log(obj.get('hello'));

// outputs "bye"
console.log(obj.set('hello', 'bye'));
console.log(obj.get('hello'));
```