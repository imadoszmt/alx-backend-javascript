# ES6 Features Overview

## What is ES6?

ES6, also known as ECMAScript 2015, is the sixth major version of the ECMAScript language specification. It introduced significant enhancements to JavaScript, making the language more powerful and expressive.

## New Features in ES6

ES6 brought numerous new features and improvements to JavaScript. This README covers some of the key additions:

1. Constants and Block-Scoped Variables
2. Arrow Functions
3. Default Parameters
4. Rest and Spread Operators
5. String Templating
6. Enhanced Object Literals
7. Iterators and for-of Loops

## Constants vs Variables

### Constants (`const`)
- Declared using the `const` keyword
- Cannot be reassigned after initialization
- Block-scoped

### Variables (`let`)
- Declared using the `let` keyword
- Can be reassigned
- Block-scoped

## Block-Scoped Variables

ES6 introduced block-scoping with `let` and `const`, limiting variable visibility to the block they're defined in:

```javascript
if (true) {
  let x = 5;
}
console.log(x); // ReferenceError: x is not defined
```

## Arrow Functions

Arrow functions provide a concise syntax for writing function expressions:

```javascript
// Traditional function
function add(a, b) {
  return a + b;
}

// Arrow function
const add = (a, b) => a + b;
```

### Default Parameters

You can now specify default values for function parameters:

```javascript
const greet = (name = "Guest") => `Hello, ${name}!`;
console.log(greet()); // Output: Hello, Guest!
```

## Rest and Spread Operators

### Rest Parameters
Collect multiple arguments into an array:

```javascript
const sum = (...numbers) => numbers.reduce((acc, num) => acc + num, 0);
console.log(sum(1, 2, 3, 4)); // Output: 10
```

### Spread Operator
Spread elements of an iterable (like an array) into individual elements:

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2); // Output: [1, 2, 3, 4, 5]
```

## String Templating

ES6 introduced template literals, allowing for easier string interpolation and multiline strings:

```javascript
const name = "World";
console.log(`Hello, ${name}!`);

const multiline = `
  This is a
  multiline string
  in ES6
`;
```

## Enhanced Object Literals

ES6 made creating and working with objects easier:

```javascript
const name = "John";
const age = 30;

// Shorthand property names
const person = { name, age };

// Computed property names
const key = "skill";
const user = {
  [key]: "JavaScript"
};

// Method definition shorthand
const obj = {
  sayHi() {
    console.log("Hi!");
  }
};
```

## Iterators and for-of Loops

ES6 introduced a new way to iterate over arrays and other iterable objects:

```javascript
const arr = [1, 2, 3, 4, 5];

for (const num of arr) {
  console.log(num);
}

// You can also iterate over strings
for (const char of "Hello") {
  console.log(char);
}
```

This README provides an overview of some key ES6 features. For more detailed information, check out the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript).
