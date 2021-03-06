#JavaScript Basics (complete course)
[View full playlist here](https://www.youtube.com/playlist?list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5)

## 1. Variables ✔️
### Variables are containers for storing data values. This video also covers naming conventions.
12/23/2017

## 2. Data Types ✔️️
### The seven data types in JavaScript are boolean, null, undefined, number, string, symbol, and object.
12/23/2017

```js
// JS Nuggets: Data Types

// There are 7 data types

// Boolean. true and false

var data = true;

if (data) {
  console.log("Booleans rule!")
} else {
  console.log("Booleans are lame.")
}

// null. is an assignment value that means “no value”

var n = null;
console.log(n * 32);

// undefined. means a variable has not been declared, or has been declared but has not yet been assigned a value

var a;
console.log(a + 2);

// Number. 42 or 3.14159.

var num = 3.6;
var ber = 6.4;
console.log(num + ber);

// String. "Hey!"

var name = "Beau";
console.log("Hi! My name is " + name);

// Symbol (new in ECMAScript 2015). A data type whose instances are unique and immutable.

var sym1 = Symbol("foo");
var sym2 = Symbol("foo");
console.log(sym1 === sym2)
console.log(String(sym1) === String(sym2))

// Object - An object is a collection of properties, and a property is an association between a name (or key) and a value.

var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";

console.log(myCar.make);
```

## 3. Numbers ✔️️
### Working with numbers including adding, subtracting, multiplying, dividing, modulus, increment, decrement, and compound assignment.
12/23/2017

## 4. String Basics ✔️️ 
### Strings are a group of characters.
12/23/2017

```js
var myName = 'Beau';

var sentence = "He said \"Hi!\""; // He said Hi!
var sentence = 'He said "Hi!"'; // He said Hi!

/*
Code	Output
\'	single quote
\"	double quote
\\	backslash
\n	newline
\r	carriage return
\t	tab
\b	backspace
\f	form feed
*/

var fullName = 'Beau ' + 'Carnes';  // 'Beau Carnes'

var sentence2 = 'My name is ' + fullName; // 'My name is Beau Carnes'

fullName += ' is my name.'; // 'Beau Carnes is my name'
```

## 5. Strings: bracket notation ✔️️
### Bracket notation allows you to access a specific character in a string.
12/23/2017

## 6. 20 String Methods in 7 Minutes
### String methods featured in this video: charAt, charCodeAt, concat, endsWith, fromCharCode, includes, indexOf, lastIndexOf, match, repeat, replace, search, slice, split, startsWith, substr, substring, toLowerCase, toUpperCase, trim.
12/24/2017

- `slice` and `match` returns arrays

```js
/* 20 String Methods */

var stringOne = "freeCodeCamp is the best place to learn"
var stringTwo = "frontend and backend development"

// charAt()
console.log(stringOne.charAt(1))

// charCodeAt()
console.log(stringOne.charCodeAt(1))

// concat()
console.log(stringOne.concat(stringTwo))

// endsWith()
console.log(stringOne.endsWith("to"))

// fromCharCode()
console.log(String.fromCharCode(114))

// includes()
console.log(stringTwo.includes("end"))

// indexOf()
console.log(stringTwo.indexOf("end"))

// lastIndexOf()
console.log(stringTwo.lastIndexOf("end"))

// match()
console.log(stringTwo.match(/end/g))

// repeat()
console.log(stringOne.repeat(3))

// replace()
console.log(stringTwo.replace(/end/g, "END"))

// search()
console.log(stringTwo.search("end"))

// slice()
console.log(stringTwo.slice(2, 4))

// split()
console.log(stringOne.split(" "))

// startsWith()
console.log(stringOne.startsWith("free"))

// substr()
console.log(stringTwo.substr(2, 4))

// substring()
console.log(stringTwo.substring(2, 4))

// toLowerCase()
console.log(stringOne.toLowerCase())

// toUpperCase()
console.log(stringOne.toUpperCase())

// trim()
var stringThree = "     Subscribe now!      ";
console.log(stringThree.trim())
```

## 7. Functions ✔️️
### Functions are one of the fundamental building blocks in JavaScript. This video covers function definitions, names, arguments, parameters, scope, and nesting functions.
12/24/2017

```js
/* Functions */

function square(number) {
  return number * number;
}

console.log(square(4));

var someVar = "Hat";
function myFun() {
  var someVar = "Shoes";
  console.log(someVar);
}

myFun();
console.log(someVar);

console.log(addSquares(1, 3));

function addSquares(a, b) {
  function square(x) {
    return x * x;
  }
  return square(a) + square(b);
}

a = addSquares(2, 3); // returns 13
b = addSquares(3, 4); // returns 25
c = addSquares(4, 5); // returns 41
```

## 8. Hoisting ✔️️
### Hoisting is when variable and function declarations are processed before any code is executed.
12/24/2017

```js
// JS Nuggets
// Hoisting

// console.log(notDeclared); // Uncaught ReferenceError: notDeclared is not defined

console.log(definedLater);
var definedLater;
definedLater = 'I am defined!'
console.log(definedLater)


console.log(definedSimulateneously);
var definedSimulateneously = 'I am defined!'
console.log(definedSimulateneously)


doSomethingElse();
function doSomethingElse(){
  console.log('I did it!');
}


functionVar(); // Uncaught TypeError: functionVar is not a function
var functionVar = function(){
  console.log('I did it!');
}
```

## 9. Comparison Operators & If Else ✔️️
### Comparison operators like >, <, =>, and =<. Also, use if / else statements to execute a block of code if a specified condition is true.
12/24/2017

```js
/** Comparison Operators & If... Else **/

var isFCCGreat = true;

if (isFCCGreat) {
  console.log("Free Code Camp is amazing!");
} else {
  console.log("Free Code Camp is horrible!");
}; 

// Comparison Operators: > < <= >= == !=

var age = 10;

if (age >= 18) {
  console.log("You are an adult!");
} else if (age < 2) {
  console.log("You are a baby!");
} else if (age < 18) {
  console.log("You are a child!");
};

if (age != 18) {console.log("You are NOT eighteen.")};
```

## 10. == vs === ✔️️
### Differences between abstract and strict equality.
12/24/2017

```js
// JS Nuggets: == vs ===

// == abstract equality

// === strict equality

console.log(3 == "3"); // true
console.log(3 === "3"); // false

console.log(true == '1'); // true
console.log(true === '1'); // false

console.log("This is a string." == new String("This is a string.")); // true
console.log("This is a string." === new String("This is a string.")); // false
```

## 11. Null vs Undefined ✔️️
### Differences between null and undefined.
12/26/2017

```js
// JS Nuggets: Null vs Undefined

var test
console.log(test)

test = null

console.log(test)

console.log(typeof null)
console.log(typeof undefined)
console.log(null === undefined)
console.log(null == undefined)
console.log(null === null)
console.log(null == null)
console.log(!null)
console.log(!!null)
console.log(1 + null)
console.log(1 + undefined)
```

## 12. Logical operators && TRICKS with short-circuit evaluation 
### Logical operators are ‘and’ (&&) and ‘or’ (||). These also allow you to do some tricks using short-circuit evaluation.
12/26/2017

```js
// JS Nuggets: Short-circuit Evaluation
if ( 4 > 5 && 5 > 6 ) {
  console.log("hi")
} else {
  console.log("no")
}

var test = true;
var isTrue = function(){
  console.log('Test is true.');
};
var isFalse = function(){
  console.log('Test is false.');
};

if(test){
//  isTrue();
}

( test && isTrue() );


test = false;
if(!test){
  isFalse(); 
}

( test || isFalse());



function theSameOldFoo(name){ 
  name = name || 'Bar' ;
  console.log("My best friend's name is " + name);
}
theSameOldFoo(); 
theSameOldFoo('Beau'); 
```

## 13. Ternary Operator ✔️️
### The ternary operator, or conditional operator, takes three arguments and is basically a shortened way of writing an if-else statement.
12/26/2017

```js
// JS Nuggets: Ternary Operator

// condition ? expr1 : expr2

var age = 15;

if (age >= 18) {
	console.log("You are an adult!");
} else {
	console.log("You are a kid");
};

console.log((age >= 18) ? "You are an adult!" : "You are a kid.");

var stop;

age > 18 ? (
    console.log("OK, you can go."),
    stop = false
) : (
    console.log("Sorry, you are much too young!"),
    stop = true
);

var firstCheck = false,
    secondCheck = false,
    access = firstCheck ? "Access denied" : secondCheck ? "Access denied" : "Access granted";

console.log(access);
```

## 14. Switch Statements ✔️️
### Control the flow of your program with switch statements.
12/26/2017

```js
// JS Nuggets: Switch Statements

let day;
switch (new Date().getDay()) {
    case 0:
    	day = "Sunday";
        break;
    case 1:
    	day = "Monday";
        break;
    case 2:
    	day = "Tuesday";
        break;
    case 3:
    	day = "Wednesday";
        break;
    case 4:
    	day = "Thursday";
        break;
    case 5:
    	day = "Friday";
        break;
    case 6:
    	day = "Saturday";
}
console.log(day)


var Animal = 'chicken';
switch (Animal) {
  case 'Cow':
  case 'Giraffe':
  case 'Dog':
  case 'Pig':
    console.log('This animal will go on Noah\'s Ark.');
    Break;
  case 'Spoon':
    console.log('A spoon is not an animal!');
    break;
  case 'Dinosaur':
  default:
    console.log('This animal will not be on the Ark.');
}
```

## 15. Arrays ✔️️
### Arrays are ways to store more than one value in a single variable. This video also covers nested arrays and the forEach method.
12/26/2017

```js
/* Array Basics */

var sandwich = ["peanut butter", "jelly", "bread"];

var teams = [["Bulls", 23], ["White Sox", 45]];

console.log(sandwich[1]);

sandwich[1] = "bananas";
console.log(sandwich);

console.log(teams[1][0]);
teams[1][0] = "red socks";
console.log(teams);

sandwich.forEach(function(element) {
    console.log(element);
});
```

## 16. Common Array Method
### Learn how to use 10 different array methods: push, pop, concat, join, reverse, shift, unshift, sort, slice, and splice.
1/8/2018

```js
// JS Nuggets: 10 Common Array Methods

var arr = ["a", "b", "c"];

arr.push("d");
console.log(arr);

console.log(arr.pop());
console.log(arr);

var arr2 = ["g", "q"];
console.log(arr.concat(arr2));
console.log(arr2);

console.log(arr.join("!"));

console.log(arr.reverse());
console.log(arr);

console.log(arr.shift());
console.log(arr);

console.log(arr.unshift("p"));
console.log(arr);

console.log(arr.slice(1,3));

arr.push("i");
arr.push("f");
arr.sort(arr);
console.log(arr);

console.log(arr.splice(2, 2, "JS Nuggets"));
console.log(arr);
```

## 17. Copying Arrays (deep and shallow)
### Shallow copy arrays using slice and the spread operator. Deep copy arrays using JSON.stringify.
1/8/2018

```js
/* Copying Arrays */

var original = [true, true, undefined, false, null];

// slice
var copy1 = original.slice(0);


// spread operator
var copy2 = [...original];
console.log(copy1, copy2);


// DEEP copying
var deepArray = [["freeCodeCamp"]];
var shallowCopy = deepArray.slice(0);

shallowCopy[0].push("is great");
console.log(deepArray[0], shallowCopy[0])

var deepCopy = JSON.parse(JSON.stringify(deepArray));

deepCopy[0].push("is great");
console.log(deepArray[0], deepCopy[0])
```

## 18. Random numbers & parseInt️️️️ ✔ ️ ️
### Create random numbers! Also, use parseInt to convert strings to integers.
1/8/2018

```js
/* Random numbers & parseInt */

// console.log(Math.floor(Math.random() * 20));

function randomRange(min, max) {

  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(randomRange(1, 9));


console.log(parseInt("11", 2));
```

## 19. For Loops ✔
### For loops are one of the most common ways to repeat things in JavaScript.
1/10/2018

```js
/* For Loops */

// for ([initialization]; [condition]; [final-expression]) {}

var ourArray = [];
for (var i = 0; i < 5; i++) {
  if (i > 2) break;
  ourArray.push(i);
}
console.log(ourArray);

var arr = [10,9,8,7,6];
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}

var arr = [
 [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
 for (var j=0; j < arr[i].length; j++) {
   console.log(arr[i][j]);
 }
}
```

## 20. While / Do While ✔
### While and do… while are ways to loop over code in JavaScript.
1/10/2018

```js
/* While, Do While */

var n = 0;

while (n < 5) {
  n++;
  
  if (n == 3) break;
  console.log("n = " + n);
}

var i = 0;

do {
  i++;
  console.log("i = " + i);
} while (i < 5);

// &turn_off_js=true
```

## 21. For in / For of
### For… in and for… of loops allow you to loop through property names and values in JavaScript.
1/10/2018

```js
/* for... in / for... of */

// usage

// for (variable in object) {
//   statements
// }

// for (variable of object) {
//   statement
// }

let person = {fname:"Beau", lname:"Carnes", arms:2}; 

let arr = [3, 5, 7];
arr.foo = 'hello';

let text = "";
for (let x in person) {
  text += person[x];
  console.log(x);
};
console.log(text);

for (let i in arr) {
  console.log(i);
};

for (let i of arr) {
  console.log(i);
};

```

## 22. Array Iteration: 8 Methods
### Learn eight methods to iterate through an array in JavaScript! Methods include: forEach, map, filter, reduce, sum, every, find, findIndex.
1/10/2018

```js
// JS Nuggets
// Array iteration: 8 methods

// forEach
[1, 2, 3].forEach(function (item, index) {
  console.log(item, index);
});


// map
const three = [1, 2, 3];
const doubled = three.map(function (item) {
  return item * 2;
});
console.log(doubled);


// filter
const ints = [1, 2, 3];
const evens = ints.filter(function (item) {
  return item % 2 === 0;
});
console.log(evens);


// reduce
const sum = [1, 2, 3].reduce(function (result, item) {
  return result + item;
}, 0);
console.log(sum)


// some
const hasNegativeNumbers = [1, 2, 3, -1, 4].some(function (item) {
  return item < 0;
});
console.log(hasNegativeNumbers);


// every
const allPositiveNumbers = [1, 2, -3].every(function (item) {
  return item > 0;
});
console.log(allPositiveNumbers);


// find
const objects = [{ id: 'a' }, { id: 'b' }, { id: 'c' }];
const found = objects.find(function (item) {
  return item.id === 'b';
});
console.log(found);


// find index
const objects2 = [{ id: 'a' }, { id: 'b' }, { id: 'c' }];
const foundIndex = objects2.findIndex(function (item) {
  return item.id === 'b';
});
console.log(foundIndex)
```

## 23. Objects
### Objects are stand-alone entities with properties and types.
1/10/2018

```js
// JS Nuggets: Objects

var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";
myCar.color;
console.log(myCar.make);
console.log(myCar.color);

myCar["year"] = 1969;
console.log(myCar["model"])

myCar["Do I like?"] = "I hate my car.";
console.log(myCar["Do I like?"]);



function showProps(obj, objName) {
  var result = "";
  for (var i in obj) {
    // obj.hasOwnProperty() is used to filter out properties from the object's prototype chain
    if (obj.hasOwnProperty(i)) {
      result += objName + "." + i + " = " + obj[i] + "\n";
    }
  }
  return result;
}
console.log(showProps(myCar, "myCar"));

// Creation: object initializer
var myHonda = {color: "red", wheels: 4, engine: {cylinders: 4, size: 2.2}};

// Creation: constructor function
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

var mycar = new Car("Chevy", "Malibu", 1993);
var anothercar = new Car("Mazda", "Miata", 1990);
console.log(mycar.model);
mycar.color = "black";
console.log(mycar.color);

// Creation: Object.create
var Animal = {
  type: "Invertebrates", 
  displayType: function() {  
    console.log(this.type);
  }
}

var animal1 = Object.create(Animal);
animal1.displayType(); 

var fish = Object.create(Animal);
fish.type = "Fishes";
fish.displayType();
```

## 24. Objects, part 2 ✔
### Learn more about objects. This video covers using objects for lookups, removing properties using delete, testing for properties, accessing and modifying nested objects, and creating an array of all object keys.
1/10/2018

```js
// Objects: Part 2

// Using Objects for Lookups
var alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W"
  // ...
};
console.log(alpha[2]);

  // Remove Object Properties
let dishes = {
  plates: 8,
  cups: 10,
  forks: 28,
  bowls: 13
};
delete dishes.cups;
console.log(dishes);

// Testing Objects for Properties
console.log(dishes.hasOwnProperty('plates'));
console.log(dishes.hasOwnProperty('cups'));

// Accessing and Modifying Nested Objects
var ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": {
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};
console.log(ourStorage.cabinet["top drawer:].folder2);
console.log(ourStorage.desk.drawer);

ourStorage.cabinet["top drawer"].folder2 = "cake recipe";
console.log(ourStorage.cabinet["top drawer"].folder2);

// Generate an Array of All Object Keys
console.log(Object.keys(ourStorage));
```

## 25. AJAX
### AJAX in allows allows you to update parts of a web page without reloading the entire page.
1/19/2018

```html
<h1>AJAX with JavaScript!</h1>
<p id="demo">Let AJAX change this text</p> 
<button type="button" onclick="loadDoc()">Change Content</button>
```

```js
// AJAX = Asynchronous JavaScript And XML

function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     document.getElementById("demo").innerHTML = this.responseText;
    }
  };
  xhttp.open("GET", "https://cors-anywhere.herokuapp.com/http://carnes.cc/code/ajax_example.txt", true);
  xhttp.send();
}

/* 
Adding "https://cors-anywhere.herokuapp.com/" prevents the following error:

XMLHttpRequest cannot load http://carnes.cc/code/ajax_example.txt. No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'https://s.codepen.io' is therefore not allowed access.
*/
```

## 26. JSON
### JSON stands for JavaScript Object Notation. It is a syntax for storing and exchanging data.

```js
//JS Nuggets: JSON

// example
var myJSON = {
    "name": {
        "first": "Beau",
        "last": "Carnes"
    },
    "age":33,
    "skills": [ "juggling", "stiltwalking", "coding" ],
    "married": true,
    "superpowers": null
 }

// stringify method
var stringified = JSON.stringify(myJSON);
console.log(stringified);


// parse method
var stringJSON = '{ "name":"Beau", "kids":2,"state":"Michigan"}';
var myParse = JSON.parse(stringJSON);
console.log(myParse);

```

## 27. Closures
### A closure is the combination of a function and the environment where the function is declared.
1/19/2018

```js
// JS Nuggets: Closures

function makeFunc() {
  var name = "JS Nuggets";
  function displayName() {
    console.log(name);
  }
  return displayName;
}

var myFunc = makeFunc();
myFunc();


var counter = (function() {
  var privateCounter = 0;
  function changeBy(val) {
    privateCounter += val;
  }
  return {
    increment: function() {
      changeBy(1);
    },
    decrement: function() {
      changeBy(-1);
    },
    value: function() {
      return privateCounter;
    }
  };   
})();

console.log(counter.value());
counter.increment();
counter.increment();
console.log(counter.value()); 
counter.decrement();
console.log(counter.value());
```


## 28. this
### The keyword ‘this’ refers to the object that “owns” the JavaScript code.
1/19/2018

```js
/* THIS */

console.log(this.document === document);

console.log(this === window);

this.a = 37;
console.log(window.a); 


function f1() {
  'use strict';
  return this;
}
console.log(f1() === window);



function add(c, d) {
  return this.a + this.b + c + d;
}

var o = {a: 1, b: 3};
console.log(add.call(o, 5, 7));
console.log(add.apply(o, [10, 20]));


function f() {
  return this.a;
}

var g = f.bind({a: 'unicycle'});
console.log(g());

var h = g.bind({a: 'cereal'}); // won’t work a second time
console.log(h());

var o = {a: 8, f: f, g: g, h: h};
console.log(o.f(), o.g(), o.h());


var o = {
 traditionalFunc: function () {
   console.log('traditionalFunc this === o?', this === o);
 },
 arrowFunc: () => {
   console.log('arrowFunc this === o?', this === o);
   console.log('arrowFunc this === window?', this === window);
 }
};

o.traditionalFunc();

o.arrowFunc();


var o = {
  prop: 37,
  f: function() {
    return this.prop;
  }
};

console.log(o.f()); // logs 37

var o = {prop: 23};

function independent() {
  return this.prop;
}

o.f = independent;

console.log(o.f());
```

## 29. Promises
### A promise represents the eventual result of an asynchronous operation.
1/20/2018

```js
// JS Nuggets: Promises

// Basic usage
var p = new Promise(function(resolve, reject) {
	
	// Do an async task async task and then...

	if(good_condition) {
		resolve('Success!');
	}
	else {
		reject('Failure!');
	}
});

p.then(function() { 
	/* do something with the result */
}).catch(function() {
	/* error */
})


// Complete example

var promiseCount = 0;

function testPromise() {
  var thisPromiseCount = ++promiseCount;
  console.log(thisPromiseCount + ': Started - Sync code started');

  var p1 = new Promise(function(resolve, reject) {
    console.log(thisPromiseCount + ': Promise started - Async code started');
    // This is only an example to create asynchronism
    window.setTimeout(
      function() {
        resolve(thisPromiseCount);
      }, Math.random() * 2000 + 1000);
  });

  p1.then(function(val) {
    console.log(val + ': Promise fulfilled - Async code terminated');
  }).catch(function(reason) {
    console.log('Handle rejected promise ('+reason+') here.');
  });

  console.log(thisPromiseCount + ': Promise made - Sync code terminated');
}

testPromise();
testPromise();
testPromise();
```

## 30. Desktop Notifications
### The Notifications API lets a web page or app send notifications that are displayed outside the page at the system level. This lets web apps send information to a user even if the application is idle or in the background.
1/20/2018

```js
// JS Nuggets: Notifications API

//Notification.requestPermission();

//new Notification("Subscribe to JS Nuggets!");

function notifyMe() {
  if (!("Notification" in window)) {
    alert("This browser does not support system notifications");
  }
  else if (Notification.permission === "granted") {
    notify();
  }
  else if (Notification.permission !== 'denied') {
    Notification.requestPermission(function (permission) {
      if (permission === "granted") {
        notify();
      }
    });
  }
  
  function notify() {
    var notification = new Notification('TITLE OF NOTIFICATION', {
      icon: 'http://carnes.cc/jsnuggets_avatar.jpg',
      body: "Hey! You are on notice!",
    });

    notification.onclick = function () {
      window.open("http://carnes.cc");      
    };
    setTimeout(notification.close.bind(notification), 7000); 
  }

}
notifyMe();
```

## 31. Immediately Invoked Function Expression
### An Immediately Invoked Function Expression (IIFE) is a JavaScript function that runs as soon as it is defined.
1/20/2018

```js
/* Immediately Invoked Function Expression (IIFE)  */

(function () {
  console.log("My favorite number is 3");
})();

(favNumber = function (num = 3) {
  console.log("My favorite number is " + num);
})();

favNumber(5);


var a = 2;

(function() {
  var a = 3;
  console.log(a);
})();

console.log(a);

let b = 2;

{
  let b = 3;
  console.log(b);
}

console.log(b);
```

## 32. Strict Mode
### “use strict” — Strict mode in JavaScript tightens the rules for certain behaviors. You can execute JavaScript code in strict mode by using the “use strict” directive.
1/20/2018

```js
"use strict";
/* Strict Mode */

function myFunction() {
  "use strict";
	var y = 3.14;  
}

// CONVERTING MISTAKES INTO ERRORS

var x = 3.14;
delete x;   

var obj = {};
Object.defineProperty(obj, "x", {value:0, writable:false});
obj.x = 3.14;

var obj = {get x() {return 0} };
obj.x = 3.14;

delete Object.prototype;

function sum(a, a, c) { 
  'use strict';
  return a + b + c; 
}


// WITH AND EVAL CHANGES

var x = 17;
with (obj) {
  x; // Is this var x or obj.x?
}

eval("var x;")

var x = 17;
var evalX = eval("'use strict'; var x = 42; x;");
console.assert(x === 17);
console.assert(evalX === 42);


// SECURING JAVASCRIPT
```

## 33. Check if a property is in an object
###How do you check if a property is in an object in JavaScript? Learn three ways in this video. Two of the ways are ‘in’ and ‘hasOwnProperty’.
1/21/2018

```js
// JS Nuggets: Check if a property is in an object

var myObject = {
  name: 'JS Nuggets'
};

if (myObject.name) {
  console.log("it is in!")
}

console.log(myObject.hasOwnProperty('name'));
console.log('name' in myObject);

console.log(myObject.hasOwnProperty('valueOf'));
console.log('valueOf' in myObject);
```

## 34. setInterval and setTimeout: timing events
### setTimeout and setInterval are timing events in JavaScript that both allow execution of code at specified time intervals. This quick tutorial shows how to use them.
1/21/2018

```html
<button onclick="clearInterval(intId)">Stop time</button>
```

```js
/* setTimeout and setInterval */

// setTimeout
var timeoutID = setTimeout(bye, 3000);

console.log('hello');

clearTimeout(timeoutID);

function bye() {
  console.log('goodbye');
}


// setInterval

var count = 0
var intId = setInterval(counter, 1000);
 
function counter() {
  console.log(++count);
}
```

## 35. try, catch, finally, throw — error handling in JavaScript
### Error handling in JavaScript uses the keywords: try, catch, finally, and throw.
1/21/2018

```js
/* Try, catch, finally */

try {
  console.log('Start of try runs');
  
  unicycle;

  console.log('End of try runs -- never reached'); 

} catch(err) {

  console.log('Error has occured: ' + err); 

} finally {
  console.log('This is always run'); 
}

console.log('...Then the execution continues');




let json = '{ "age": 30 }';
 
try {
 
  let user = JSON.parse(json); 
  if (!user.name) {
    throw new SyntaxError("Incomplete data: no name");
  }
 
  console.log( user.name );
 
} catch(e) {
  console.log( "JSON Error: " + e ); 
}
```

## 36. Dates
### Work with dates in JavaScript.
1/21/2018

```js
/* Dates */

var d1 = new Date()
console.log(d1.toTimeString())

var d2 = new Date(2017, 1, 3, 42, 43, 23, 23)
console.log(d2.toString())

var d3 = new Date(929397621000)
console.log(d3.toString())

var d4 = new Date("March 25 2017")
console.log(d4.toString())

console.log(d4.getDay())
d4.setYear(2020)
console.log(d4.toString())

var start = new Date();
doSomething();
var end = new Date();

var elapsed = end.getTime() - start.getTime();
console.log(elapsed);

function doSomething() {
    for(var i = 0; i < 1000000000; i++) {

    }
};
```

#ES6 Basics (complete course)
[View full playlist here](https://www.youtube.com/playlist?list=PLWKjhJtqVAbljtmmeS0c-CEl2LdE-eR_F)

## Var vs Const vs Let ️️️️️️️️✔️️
### Three different ways to declare variables.
1/22/2018

```js
// JS Nuggets: Const vs Let vs Var

// const - for values that never change

const Pi = 3.14
// Pi = 1 //error
console.log(Pi);


// let - for block-level variables

for(let i = 0; i < 3; i++) {
  console.log(i);
}
// console.log(i) //error


// var - for variables available to entire function or program

console.log(j)
for(var j = 0; j < 3; j++) {
  console.log(j);
}
console.log(j)
```

## Classes
### Learn about class expressions, class declarations, and inheritance / extending.
1/22/2018

```js
//**JS Nuggets: Classes**

//**class declaration**
class Person {
  constructor(name, year_born) {
    this.name = name;
    this.year_born = year_born;
  }
  
  get age() {
    return this.calcAge();
  }

  calcAge() {
    return new Date().getFullYear() - this.year_born;
  }
  
  what() {
    console.log(this.name + ' is a person.');
  }
  
  static arms() {
    return 2;
  }
}

var me = new Person("Beau", 1983);
console.log(me.name + " was born in " + me.year_born + "!")
me.what();
console.log(me.name + " has " + Person.arms() + " arms!")

class Juggler extends Person {
  what() {
    super.what();
    console.log(this.name + " is a juggler.");
  }
}

var you = new Juggler ("Jay", 1980);
me.what();
you.what();


//**class expressions**
// unnamed
var Person2 = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

// named
var Person3 = class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};
```

## Symbols
### Symbols are a unique immutable data type.
1/22/2018

```js
// JS Nuggets: Symbols

// Creation

let symbol1 = Symbol('symbol2');
let symbol2 = Symbol('symbol2');
console.log(symbol1 === symbol2);
console.log(typeof symbol1);
console.log('symbol: ' + symbol1.toString());


// Use case 1: Symbols as property keys
   const MY_KEY = Symbol();
    let obj = {};
    
    obj[MY_KEY] = 123;
    console.log(obj[MY_KEY]);


// Use case 2: constants representing concepts
const COLOR_RED    = Symbol('Red');
const COLOR_ORANGE = Symbol('Orange');
const COLOR_YELLOW = Symbol('Yellow');
const COLOR_GREEN  = Symbol('Green');
const COLOR_BLUE   = Symbol('Blue');
const COLOR_VIOLET = Symbol('Violet');

function getComplement(color) {
    switch (color) {
        case COLOR_RED:
            return COLOR_GREEN;
        case COLOR_ORANGE:
            return COLOR_BLUE;
        case COLOR_YELLOW:
            return COLOR_VIOLET;
        case COLOR_GREEN:
            return COLOR_RED;
        case COLOR_BLUE:
            return COLOR_ORANGE;
        case COLOR_VIOLET:
            return COLOR_YELLOW;
        default:
            throw new Exception('Unknown color: '+color);
    }
}
```

## Tepmlate Literals
### Template literals are string literals allowing embedded expressions. These are surrounded by backticks ``.
1/23/2018

```js
// JS Nuggets: Template Literals

// multi-line strings
console.log(`string text line 1 string text line2`)

// expression interpolation
var a = 5;
var b = 10;
console.log(`Fifteen is ${a + b} and \nnot ${2 * a + b}.`)

// Tagged template literals
function tag(strings, ...values) {
  console.log(strings);
  console.log(values);

  return "JS Nuggets";
}

console.log(tag`Hello ${a+b} world ${a * b});
```

## Proxies 
### Proxies are used in to give objects custom behavior. One use is for data validation.
1/24/2018

```js
// JS Nuggets: Proxies!

// Syntax: var p = new Proxy(target, handler);

// Example 1
var handler = {
  get (target, key) {
    return key in target ? target[key] : 37;
    }
};

var p = new Proxy({}, handler);
p.a = 1;
p.b = undefined;

console.log(p.a, p.b);
console.log('c' in p, p.c);

// Example 2
let validator = {
  set: function(obj, prop, value) {
    if (prop === 'age') {
      if (typeof value !== 'number' || Number.isNaN(value)) {
        console.log('Age must be a number')
      }
      if (value < 0) {
        console.log('Age must be a positive number')
      }
    }

    obj[prop] = value;
  
    return true;
  }
};

let person = new Proxy({}, validator);
person.age = 'young';
console.log(person.age)
person.age = -30;
person.age = 100;
console.log(person.age)
```

## …spread operator and rest operator 
### The spread operator (…) spreads out the elements of an array (or iterable object). The rest operator condenses elements.
1/24/2018

```js
/* Spread Operator / Rest Operator */

// add the elements of an existing array into a new array
var certsToAdd = ['Algorithms and Data Structures', 'Front End Libraries']; 
var certifications = ['Responsive Web Design', ...certsToAdd, 'Data Visualization', 'APIs and Microservices', 'Quality Assurance and Information Security'];
console.log(certifications);

// pass elements of an array as arguments to a function
function addThreeNumbers(x, y, z) { 
	console.log(x+y+z)
}
var args = [0, 1, 2, 3];
addThreeNumbers(...args);

// copy arrays
var arr = [1, 2, 3];
var arr2 = [...arr]; // like arr.slice()
arr2.push(4); 
console.log(arr);
console.log(arr2);


// concatenate arrays
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
//arr1.concat(arr2);
arr1 = [...arr1, "freeCodeCamp", ...arr2];
console.log(arr1);


// REST: condense multiple elements into an array
function multiply(multiplier, ...theArgs) {
  return theArgs.map(function(element) {
    return multiplier * element;
  });
}

var arr = multiply(2, 1, 2, 3); 
console.log(arr)
```

## Arrow Functions ✔️️
### An arrow function in ES6 has a shorter syntax than a normal function and does not bind its own this.
1/24/2018

```js
/*Arrow Functions */

//Syntax
(param1, param2) => { statements }
(param1, param2) => expression
(param1, param2) => { return expression; }

(singleParam) => { statements }
singleParam => { statements }

() => { statements }
() => expression
() => { return expression; }

(param1, param2, paramN) => expression 

// NORMAL FUNCTION
var multiply = function(x, y) {
  return x * y;
}; 
 
// ARROW FUNCTION 
var multiply = (x, y) => { return x * y };
// or
var multiply = (x, y) => x*y;

// Example
var materials = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];

var materialsLength1 = materials.map(function(material) { 
  return material.length;
});

var materialsLength2 = materials.map((material) => {
  return material.length;
});

var materialsLength3 = materials.map(material => material.length);

// No binding of 'this'
function Person(){
  this.age = 0;

  setInterval(() => {
    this.age++; // In a normal function, 'this' refers to global object, here it properly refers to the person object
    console.log(this.age)
  }, 3);
}

var p = new Person();

// Returning object literals
var func = () => ({foo: 1});

// Line breaks
var func = ()
           => 1; 
```

## Destructuring
### Destructuring assignment is special syntax for neatly assigning values taken directly from objects and arrays to variables.
1/24/2018

```js
/* Destructuring */

// Assign variables from objects
var voxel = {x: 3.6, y: 7.4, z: 6.54 };

const {x, y, z} = voxel;
console.log(x);
const {x : a, y : b, z : c} = voxel;
console.log(b);

// Assign variables from nested objects
const nest = {
  start: { x: 5, y: 6},
  end: { x: 6, y: -9 }
};
const { start : { x: startX, y: startY }} = nest;
console.log(startX);

// Assign Variables from Arrays
//const [q,,, r] = [1, 2, 3, 4, 5];
//console.log(q, r);

// Rest Operator to Reassign Array Elements
const [q, r, ...rest] = [1, 2, 3, 4, 5];
console.log(q, r);
console.log(rest);

// Pass an Object as a Function's Parameters
const profileUpdate = ({ name, age }) => {
  // do something with these variables
}
```

## Map
### Maps are data structures that store key-value pairs. See how they work and learn about the ES6 map object.
1/25/2018

```js
/* Maps */

let myMap = function() {
	this.collection = {};
	this.count = 0;
	this.size = function() {
		return this.count;
	};
	this.set = function(key, value) {
		this.collection[key] = value;
		this.count++;
	};
	this.has = function(key) {
		return (key in this.collection);
	};
	this.get = function(key) {
		return (key in this.collection) ? this.collection[key] : null;
	};
	this.delete = function(key) {
		if (key in this.collection) {
			delete this.collection[key];
			this.count--;
		}
	};
	this.values = function() {
		let result = new Array();
		for (let key of Object.keys(this.collection)) {
			result.push(this.collection[key]);
		};
		return (result.length > 0) ? result : null;
	};
	this.clear = function() {
		this.collection = {};
		this.count = 0;
	};
};

let map = new myMap();
map.set('arms', 2);
map.set('fingers', 10);
map.set('eyes', 2);
map.set('belley button', 1);

console.log(map.get('fingers'));
console.log(map.size());
console.log(map.values());

let map2 = new Map();
map2.has('hands');
map2.entries();

let keyObj = {},
    keyFunc = function() {};

map2.set('hello', 'string value');
map2.set(keyObj, 'obj value');
map2.set(keyFunc, 'func value');
map2.set(NaN, 'NaN value')

console.log(map2.size);

console.log(map2.get('hello'));
console.log(map2.get(keyObj));
console.log(map2.get(keyFunc));
console.log(map2.get(NaN));
```

## Import/Export (Modules) ✔️️ ️ ️
### The import and export statements allow you to break up your code in different files or modules.
1/25/2018

```js
/* Import / Export */

// NAMED EXPORTS

//------ lib.js ------
export const sqrt = Math.sqrt;
export function square(x) {
    return x * x;
}
export function diag(x, y) {
    return sqrt(square(x) + square(y));
}

// IMPORT PART OF A MODULE

//------ main.js ------
import { square, diag } from 'lib';
console.log(square(11)); 
console.log(diag(4, 3)); 



// IMPORTING COMPLETE MODULE

//------ main.js ------
import * as lib from 'lib';
console.log(lib.square(11));
console.log(lib.diag(4, 3)); 


// IMPORTING WITH MORE CONVENIENT ALIAS
import {reallyReallyLongModuleMemberName as shortName}
  from 'my-module';



// SINGLE DEFAULT EXPORT

//------ myFunc.js ------
export default function () { ··· } // no semicolon!

//------ main1.js ------
import myFunc from 'myFunc';
myFunc();
```

#Clean Code (complete course)
[View full playlist here](https://www.youtube.com/playlist?list=PLWKjhJtqVAbkK24EaPurzMq0-kw5U9pJh)

## Variables 
### [Article](https://github.com/ryanmcdermott/clean-code-javascript)
1/26/2018

```js
// ** JS Nuggets: Clean Code: Variables **

// Use meaningful and pronounceable variable names
var yearMonthDay = moment().format('YYYY/MM/DD');

// Use ES6 constants when variable values do not change
const FIRST_US_PRESIDENT = "George Washington";

// Use the same vocabulary for the same type of variable
getUser();

// Use searchable names
var MINUTES_IN_A_YEAR = 525600
for (var i = 0; i < MINUTES_IN_A_YEAR; i++) {
  runCronJob();
}

// Use explanatory variables
const cityStateRegex = /^(.+)[,\\s]+(.+?)\s*(\d{5})?$/;
const match = cityStateRegex.match(cityStateRegex);
const city = match[1];
const state = match[2]
saveCityState(city, state);

// Don't add unneeded context
var Car = {
  make: 'Honda',
  model: 'Accord',
  color: 'Blue'
};

function paintCar(car) {
  car.color = 'Red';
}

// Short-circuiting is cleaner than conditionals
function createMicrobrewery(name) {
  var breweryName = name || 'Hipster Brew Co.';
}
```

## Functions (Part 1)
### [Article](https://github.com/ryanmcdermott/clean-code-javascript#functions)

```js
// JS Nuggets
// Clean Code: Functions (Part 1)

// Function arguments (2 or fewer ideally)
const menuConfig = {
  title: 'Foo',
  body: 'Bar',
  buttonText: 'Baz',
  cancellable: true
};

function createMenu(menuConfig) {
  // ...
}


// Functions should do one thing
function emailClients(clients) {
  clients
    .filter(isClientActive)
    .forEach(email);
}

function isClientActive(client) {
  const clientRecord = database.lookup(client);
  return clientRecord.isActive();
}



// Function names should say what they do
function addMonthToDate(month, date) {
  // ...
}

const date = new Date();
addToDate(1, date);


// Functions should only be one level of abstraction
function parseBetterJSAlternative(code) {
  const REGEXES = [
    // ...
  ];

  const statements = code.split(' ');
  const tokens = [];
  REGEXES.forEach((REGEX) => {
    statements.forEach((statement) => {
      // ...
    });
  });

  const ast = [];
  tokens.forEach((token) => {
    // lex...
  });

  ast.forEach((node) => {
    // parse...
  });
}
// ******
function tokenize(code) {
  const REGEXES = [
    // ...
  ];

  const statements = code.split(' ');
  const tokens = [];
  REGEXES.forEach((REGEX) => {
    statements.forEach((statement) => {
      tokens.push( /* ... */ );
    });
  });

  return tokens;
}

function lexer(tokens) {
  const ast = [];
  tokens.forEach((token) => {
    ast.push( /* ... */ );
  });

  return ast;
}

function parseBetterJSAlternative(code) {
  const tokens = tokenize(code);
  const ast = lexer(tokens);
  ast.forEach((node) => {
    // parse...
  });
}


// Remove duplicate code
function showList(employee) {
  developers.forEach((employee) => {
    const expectedSalary = employee.calculateExpectedSalary();
    const experience = employee.getExperience();
    
    let portfolio = employee.getGithubLink();
    
    if (employee.type === 'manager') {
      portfolio = employee.getMBAProjects();
    }
    
    const data = {
      expectedSalary,
      experience,
      portfolio
    };

    render(data);
  });
}


// Don't use flags as function parameters

function createFile(name) {
  fs.create(`./temp/${name}`);
} 

function createTempFile(name) {
  fs.create(name);
}
```

## Functions (part 2)
### [Article](https://github.com/ryanmcdermott/clean-code-javascript#functions)

```js
// JS Nuggets
// Clean Code: Functions (Part 2)

// Avoid side effects
let name = 'Beau Carnes';

function splitIntoFirstAndLastName() {
  return name.split(' ');
}

const newName = splitIntoFirstAndLastName(name);

console.log(name);
console.log(newName);

// Don't write to global functions
class SuperArray extends Array {
  diff(comparisonArray) {
    const hash = new Set(comparisonArray);
    return this.filter(elem => !hash.has(elem));
  }
}


// Favor functional programming over imperative programming
const programmerOutput = [
  {
    name: 'Uncle Bobby',
    linesOfCode: 500
  }, {
    name: 'Suzie Q',
    linesOfCode: 1500
  }, {
    name: 'Jimmy Gosling',
    linesOfCode: 150
  }, {
    name: 'Gracie Hopper',
    linesOfCode: 1000
  }
];

const INITIAL_VALUE = 0;

const totalOutput = programmerOutput
  .map((programmer) => programmer.linesOfCode)
  .reduce((acc, linesOfCode) => acc + linesOfCode, INITIAL_VALUE);


// Encapsulate conditionals

function shouldShowSpinner(fsm, listNode) {
  return fsm.state === 'fetching' && isEmpty(listNode);
}

if (shouldShowSpinner(fsmInstance, listNodeInstance)) {
  // ...
}


// Avoid negative conditionals
function isDOMNodePresent(node) {
  // ...
}

if (isDOMNodePresent(node)) {
  // ...
}


// Avoid conditionals
class Airplane {
  // ...
  getCruisingAltitude() {
    switch (this.type) {
      case '777':
        return this.getMaxAltitude() - this.getPassengerCount();
      case 'Air Force One':
        return this.getMaxAltitude();
      case 'Cessna':
        return this.getMaxAltitude() - this.getFuelExpenditure();
    }
  }
}

class Airplane {
  // ...
}

class Boeing777 extends Airplane {
  // ...
  getCruisingAltitude() {
    return this.getMaxAltitude() - this.getPassengerCount();
  }
}

class AirForceOne extends Airplane {
  // ...
  getCruisingAltitude() {
    return this.getMaxAltitude();
  }
}

class Cessna extends Airplane {
  // ...
  getCruisingAltitude() {
    return this.getMaxAltitude() - this.getFuelExpenditure();
  }
}


// Remove dead code

function newRequestModule(url) {
  // ...
}

const req = newRequestModule;
inventoryTracker('apples', req, 'www.carnes.cc');
```

## Objects
### [Article](https://github.com/ryanmcdermott/clean-code-javascript)
1/27/2018

```js
// Clean Code: Objects and Data Structures

// Use getters and setters
function makeBankAccount() {
  let balance = 0;

  function getBalance() {
    return balance;
  }
  
  function setBalance(amount) {
    balance = amount;
  }
  
  return {
    getBalance,
    setBalance
  };
}
const account = makeBankAccount();
account.setBalance(100);
console.log(account.getBalance());



// Make objects have private members
const Employee = function(name) {
  return {
    getName() {
      return name;
    },
  };
};


const employee = new Employee('John Doe');
console.log(`Employee name: ${employee.getName()}`);
delete employee.name;
console.log(`Employee name: ${employee.getName()}`);
```

## Classes
### [Article](https://github.com/ryanmcdermott/clean-code-javascript)
1/27/2018

```js
/* Clean Code: Classes */

// Prefer ES2015/ES6 classes over ES5 plain functions

//BAD
const Animal = function(age) {
  if (!(this instanceof Animal)) {
    throw new Error('Instantiate Animal with `new`');
  }

  this.age = age;
};

Animal.prototype.move = function move() {};

const Mammal = function(age, furColor) {
  if (!(this instanceof Mammal)) {
    throw new Error('Instantiate Mammal with `new`');
  }

  Animal.call(this, age);
  this.furColor = furColor;
};

Mammal.prototype = Object.create(Animal.prototype);
Mammal.prototype.constructor = Mammal;
Mammal.prototype.liveBirth = function liveBirth() {};

const Human = function(age, furColor, languageSpoken) {
  if (!(this instanceof Human)) {
    throw new Error('Instantiate Human with `new`');
  }

  Mammal.call(this, age, furColor);
  this.languageSpoken = languageSpoken;
};

Human.prototype = Object.create(Mammal.prototype);
Human.prototype.constructor = Human;
Human.prototype.speak = function speak() {};

// GOOD

class Animal {
  constructor(age) {
    this.age = age;
  }

  move() { /* ... */ }
}

class Mammal extends Animal {
  constructor(age, furColor) {
    super(age);
    this.furColor = furColor;
  }

  liveBirth() { /* ... */ }
}

class Human extends Mammal {
  constructor(age, furColor, languageSpoken) {
    super(age, furColor);
    this.languageSpoken = languageSpoken;
  }

  speak() { /* ... */ }
}



// Use method chaining

// BAD
class Car {
  constructor() {
    this.make = 'Honda';
    this.model = 'Accord';
    this.color = 'white';
  }

  setMake(make) {
    this.make = make;
  }

  setModel(model) {
    this.model = model;
  }

  setColor(color) {
    this.color = color;
  }

  save() {
    console.log(this.make, this.model, this.color);
  }
}

const car = new Car();
car.setColor('pink');
car.setMake('Ford');
car.setModel('F-150');
car.save();

//GOOD
class Car {
  constructor() {
    this.make = 'Honda';
    this.model = 'Accord';
    this.color = 'white';
  }

  setMake(make) {
    this.make = make;
    // NOTE: Returning this for chaining
    return this;
  }

  setModel(model) {
    this.model = model;
    // NOTE: Returning this for chaining
    return this;
  }

  setColor(color) {
    this.color = color;
    // NOTE: Returning this for chaining
    return this;
  }

  save() {
    console.log(this.make, this.model, this.color);
    // NOTE: Returning this for chaining
    return this;
  }
}

const car = new Car()
  .setColor('pink')
  .setMake('Ford')
  .setModel('F-150')
  .save();

// Prefer composition over inheritance

// BAD
class Employee {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }

  // ...
}

// Bad because Employees "have" tax data. EmployeeTaxData is not a type of Employee
class EmployeeTaxData extends Employee {
  constructor(ssn, salary) {
    super();
    this.ssn = ssn;
    this.salary = salary;
  }

  // ...
}

//GOOD
class EmployeeTaxData {
  constructor(ssn, salary) {
    this.ssn = ssn;
    this.salary = salary;
  }

  // ...
}

class Employee {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }

  setTaxData(ssn, salary) {
    this.taxData = new EmployeeTaxData(ssn, salary);
  }
  // ...
}
```

## SOLID
### [Article](https://github.com/ryanmcdermott/clean-code-javascript)
1/27/2018

```js
/* Clean Code: S.O.L.I.D. */

// **Single Responsibility Principle**

//Bad

class UserSettings {
  constructor(user) {
    this.user = user;
  }

  changeSettings(settings) {
    if (this.verifyCredentials()) {
      // ...
    }
  }

  verifyCredentials() {
    // ...
  }
}

//Good

class UserAuth {
  constructor(user) {
    this.user = user;
  }

  verifyCredentials() {
    // ...
  }
}


class UserSettings {
  constructor(user) {
    this.user = user;
    this.auth = new UserAuth(user);
  }

  changeSettings(settings) {
    if (this.auth.verifyCredentials()) {
      // ...
    }
  }
}


// **Open/Closed Principle**

// BAD
var iceCreamFlavors=["chocolate","vanilla"];
var iceCreamMaker={
 makeIceCream (flavor) {
  if(iceCreamFlavors.indexOf(flavor)>-1){
   console.log("Great success. You now have ice cream.")
  }else{
   console.log("Epic fail. No ice cream for you.")
  }
 }
}
export default iceCreamMaker;

// GOOD
var iceCreamFlavors=["chocolate","vanilla"];
var iceCreamMaker={
 makeIceCream (flavor) {
  if(iceCreamFlavors.indexOf(flavor)>-1){
   console.log("Great success. You now have ice cream.")
  }else{
   console.log("Epic fail. No ice cream for you.")
  }
 }
 addFlavor(flavor){
  iceCreamFlavors.push(flavor);
 }
}
export default iceCreamMaker;


// **Liskov Substitution Principle**

// BAD

class Rectangle {
  constructor() {
    this.width = 0;
    this.height = 0;
  }

  setColor(color) {
    // ...
  }

  render(area) {
    // ...
  }

  setWidth(width) {
    this.width = width;
  }

  setHeight(height) {
    this.height = height;
  }

  getArea() {
    return this.width * this.height;
  }
}

class Square extends Rectangle {
  setWidth(width) {
    this.width = width;
    this.height = width;
  }

  setHeight(height) {
    this.width = height;
    this.height = height;
  }
}

function renderLargeRectangles(rectangles) {
  rectangles.forEach((rectangle) => {
    rectangle.setWidth(4);
    rectangle.setHeight(5);
    const area = rectangle.getArea(); // BAD: Returns 25 for Square. Should be 20.
    rectangle.render(area);
  });
}

const rectangles = [new Rectangle(), new Rectangle(), new Square()];
renderLargeRectangles(rectangles);


// GOOD

class Shape {
  setColor(color) {
    // ...
  }

  render(area) {
    // ...
  }
}

class Rectangle extends Shape {
  constructor(width, height) {
    super();
    this.width = width;
    this.height = height;
  }

  getArea() {
    return this.width * this.height;
  }
}

class Square extends Shape {
  constructor(length) {
    super();
    this.length = length;
  }

  getArea() {
    return this.length * this.length;
  }
}

function renderLargeShapes(shapes) {
  shapes.forEach((shape) => {
    const area = shape.getArea();
    shape.render(area);
  });
}

const shapes = [new Rectangle(4, 5), new Rectangle(4, 5), new Square(5)];
renderLargeShapes(shapes);


// **Interface Segregation Principle**

// BAD

class DOMTraverser {
  constructor(settings) {
    this.settings = settings;
    this.setup();
  }

  setup() {
    this.rootNode = this.settings.rootNode;
    this.animationModule.setup();
  }

  traverse() {
    // ...
  }
}

const $ = new DOMTraverser({
  rootNode: document.getElementsByTagName('body'),
  animationModule() {} // Most of the time, we won't need to animate when traversing.
  // ...
});

// GOOD

class DOMTraverser {
  constructor(settings) {
    this.settings = settings;
    this.options = settings.options;
    this.setup();
  }

  setup() {
    this.rootNode = this.settings.rootNode;
    this.setupOptions();
  }

  setupOptions() {
    if (this.options.animationModule) {
      // ...
    }
  }

  traverse() {
    // ...
  }
}

const $ = new DOMTraverser({
  rootNode: document.getElementsByTagName('body'),
  options: {
    animationModule() {}
  }
});

// **Dependency Inversion Principle**

// BAD

class InventoryRequester {
  constructor() {
    this.REQ_METHODS = ['HTTP'];
  }

  requestItem(item) {
    // ...
  }
}

class InventoryTracker {
  constructor(items) {
    this.items = items;

    // BAD: We have created a dependency on a specific request implementation.
    // We should just have requestItems depend on a request method: `request`
    this.requester = new InventoryRequester();
  }

  requestItems() {
    this.items.forEach((item) => {
      this.requester.requestItem(item);
    });
  }
}

const inventoryTracker = new InventoryTracker(['apples', 'bananas']);
inventoryTracker.requestItems();

// GOOD

class InventoryTracker {
  constructor(items, requester) {
    this.items = items;
    this.requester = requester;
  }

  requestItems() {
    this.items.forEach((item) => {
      this.requester.requestItem(item);
    });
  }
}

class InventoryRequesterV1 {
  constructor() {
    this.REQ_METHODS = ['HTTP'];
  }

  requestItem(item) {
    // ...
  }
}

class InventoryRequesterV2 {
  constructor() {
    this.REQ_METHODS = ['WS'];
  }

  requestItem(item) {
    // ...
  }
}

// By constructing our dependencies externally and injecting them, we can easily
// substitute our request module for a fancy new one that uses WebSockets.
const inventoryTracker = new InventoryTracker(['apples', 'bananas'], new InventoryRequesterV2());
inventoryTracker.requestItems();
```

## Testing, Concurrency, & Error Handling
### [Article](https://github.com/ryanmcdermott/clean-code-javascript)
1/28/2018

```js
/* Clean Code: Testing, Concurrency, & Error Handling */

/* TESTING */
// Single concept per test

// BAD
import assert from 'assert';

describe('MakeMomentJSGreatAgain', () => {
  it('handles date boundaries', () => {
    let date;

    date = new MakeMomentJSGreatAgain('3/1/2017');
    date.addDays(30);
    assert.equal('3/31/2017', date);

    date = new MakeMomentJSGreatAgain('2/1/2016');
    date.addDays(28);
    assert.equal('02/29/2016', date);

    date = new MakeMomentJSGreatAgain('2/1/2017');
    date.addDays(28);
    assert.equal('03/01/2017', date);
  });
});

// GOOD
import assert from 'assert';

describe('MakeMomentJSGreatAgain', () => {
  it('handles 30-day months', () => {
    const date = new MakeMomentJSGreatAgain('3/1/2017');
    date.addDays(30);
    assert.equal('3/31/2017', date);
  });

  it('handles leap year', () => {
    const date = new MakeMomentJSGreatAgain('2/1/2016');
    date.addDays(28);
    assert.equal('02/29/2016', date);
  });

  it('handles non-leap year', () => {
    const date = new MakeMomentJSGreatAgain('2/1/2017');
    date.addDays(28);
    assert.equal('03/01/2017', date);
  });
});

/* CONCURRENCY */
// Use ES6 Promises, not callbacks

// BAD
import { get } from 'request';
import { writeFile } from 'fs';

get('https://en.wikipedia.org/wiki/FreeCodeCamp', (requestErr, response) => {
  if (requestErr) {
    console.error(requestErr);
  } else {
    writeFile('article.html', response.body, (writeErr) => {
      if (writeErr) {
        console.error(writeErr);
      } else {
        console.log('File written');
      }
    });
  }
});

// GOOD
import { get } from 'request';
import { writeFile } from 'fs';

get('https://en.wikipedia.org/wiki/FreeCodeCamp')
  .then((response) => {
    return writeFile('article.html', response);
  })
  .then(() => {
    console.log('File written');
  })
  .catch((err) => {
    console.error(err);
  });

// ES8 Async/Await are even cleaner than Promises

// BAD
import { get } from 'request-promise';
import { writeFile } from 'fs-promise';

get('https://en.wikipedia.org/wiki/FreeCodeCamp')
  .then((response) => {
    return writeFile('article.html', response);
  })
  .then(() => {
    console.log('File written');
  })
  .catch((err) => {
    console.error(err);
  });

// GOOD
import { get } from 'request-promise';
import { writeFile } from 'fs-promise';

async function getCleanCodeArticle() {
  try {
    const response = await get('https://en.wikipedia.org/wiki/FreeCodeCamp');
    await writeFile('article.html', response);
    console.log('File written');
  } catch(err) {
    console.error(err);
  }
}

/* ERROR HANDLING */
// Don't ignore caught errors

// BAD
try {
  functionThatMightThrow();
} catch (error) {
  console.log(error);
}

// GOOD
try {
  functionThatMightThrow();
} catch (error) {
  // One option (more noisy than console.log):
  console.error(error);
  // Another option:
  notifyUserOfError(error);
  // Another option:
  reportErrorToService(error);
  // OR do all three!
}
```

## Formatting and Commenting
### [Article](https://github.com/ryanmcdermott/clean-code-javascript)
1/28/2018

```js
/* Clean Code: Formatting and Comments */

/* FORMATTING */
// Use consistent capitalization
const DAYS_IN_WEEK = 7;
const DAYS_IN_MONTH = 30;

const songs = ['Back In Black', 'Stairway to Heaven', 'Hey Jude'];
const artists = ['ACDC', 'Led Zeppelin', 'The Beatles'];

function eraseDatabase() {}
function restoreDatabase() {}

class animal {}
class alpaca {}

// Function callers and callees should be close
class PerformanceReview {
  constructor(employee) {
    this.employee = employee;
  }

  perfReview() {
    this.getPeerReviews();
    this.getManagerReview();
    this.getSelfReview();
  }

  getPeerReviews() {
    const peers = this.lookupPeers();
    // ...
  }
  
  lookupPeers() {
    return db.lookup(this.employee, 'peers');
  }

  getManagerReview() {
    const manager = this.lookupManager();
  }
  
  lookupManager() {
    return db.lookup(this.employee, 'manager');
  }

  getSelfReview() {
    // ...
  }
}

const review = new PerformanceReview(employee);
review.perfReview();


/* COMMENTS */
// Only comment things that have business logic complexity
function hashIt(data) {
  let hash = 0;

  const length = data.length;

  for (let i = 0; i < length; i++) {
    const char = data.charCodeAt(i);
    hash = ((hash << 5) - hash) + char;
    // Convert to 32-bit integer
    hash &= hash;
  }
}

// Don't leave commented out code in your codebase
doStuff();

// Don't have journal comments
function combine(a, b) {
  return a + b;
}

// Avoid positional markers
$scope.model = {
  menu: 'foo',
  nav: 'bar'
};

const actions = function() {
  // ...
};
```