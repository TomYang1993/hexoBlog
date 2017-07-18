---
title: Looking Through JavaScript
date: 2017-07-17 22:14:48
tags:
---

## Basic concept about JavaScript(keep in mind)
>deep down javascript is a prototype-based language

## Basic reference
----
### false values
``` javascript
0  ""  false  null  undefined    NaN 
```

### primitive types
``` javascript
number string boolean null undefined
```

## Basic syntax of JavaScript
--------
### define a variable
``` javascript
var y = 1;
var y = {a:1, b:2};
```

### define a function
``` javascript
function foo() {  //do something  }
var y = function() {   //do something   }
```

## Interesting facts about false values 
`NaN` can not be compared by `==` or `===`
`isNaN()` function is the only one to verify

used in Math functions or parsing a number fails

## Difference between JSON object and JavaScript object

Formally, a JavaScript object is a data type in JavaScript, makes sense only in JavaScript

JSON(JavaScript Object annotation) object is a data **interchange** format, makes sense in languages, text file, database etc.

1.Javascript object can take object as key, while JSON can take only string as key

2.JSON can not take function as the value

## Conversion between JSON object and javascript object

`JSON.parse(aJsonString)`

reviver method to extract key-value pair, if interested

`JSON.stringfy(aliceObject)`

replacer method to choose which part to do the conversion

## How to iterate collection, array in JS

`forEach()` to iterate an array

`for(var i in ..)` for whatever |
**The for...in statement** iterates over the enumerable properties of an object, in original insertion order
``` javascript
var arr = [3, 5, 7];
arr.foo = "hello";

for (var i in arr) {
   console.log(i); // logs "0", "1", "2", "foo"
}
```

`for(var i of ..)` for collection, or more precisely |
**The for...of statement** creates a loop iterating over iterable objects (including Array, Map, Set, String, TypedArray, arguments object 
``` javascript
var arr = [3, 5, 7];
arr.foo = "hello";

for (var i of arr) {
   console.log(i); // logs "3", "5", "7"
    //it is does not log "3", "5", "7","hello"
}
```
