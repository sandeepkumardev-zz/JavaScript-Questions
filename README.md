<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/javascript.png">
  <h1>JavaScript Questions</h1>

From basic to advanced: test how well you know JavaScript, refresh your knowledge a bit, or prepare for your coding interview! 💪 🚀

</div>

## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.

<details><summary><b>Contributors List</b></summary>

- [@sandeepkumardev](https://github.com/sandeepkumardev)
- [@vickydonor-99](https://github.com/vickydonor-99)
- [AurobindoGupta](https://github.com/AurobindoGupta)

</details>

---

<h3 align="center"> Printing Patterns </h3>

###### 1. Square star pattern.

```javascript
*****
*****
*****
*****
*****
```

<p>
To create square star pattern run 2 nested for loop. Execute each loop for 'n' number of times, where 'n' is number of rows/columns in the square, i.e for(let i = 0;i < n;i++).

The internal loop will run for 'n' number of times which will print starts in a row and at the end of the loop print a newline (\n).

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 0; j < n; j++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 2. Right triangle pattern.

```javascript
*
**
***
****
*****
```

<p>
To create the right triangle pattern in javascript again run 2 nested for loop external loop will take care of columns of pattern and the internal loop will print rows of the pattern.

You can observe from the above-shown pattern that we need to run an external loop for 'n' time while the internal loop runs for 1 time in the first execution, 2 times in the second execution, and so on till 'n' times.

You can use the value of i from the external loop which will increase from 1 to 'n' inside the internal loop as a condition.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 0; j < i; j++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 3. Left triangle pattern.

```javascript
    *
   **
  ***
 ****
*****
```

<p>
To create a left triangle pattern in javascript you will have to deal with 3 loops, 1 of which is external and 2 are internal. The external loop will execute internal loops for 'n' number of times and the internal loop will design a pattern for each row.

From the above pattern, you can see each row has a series of stars and spaces. The number of stars in a row starting from 1 preceding with 'n-1' spaces and ends with 'n' star and 0 spaces.

Create 2 internal loops, 1st print n - i spaces and 2nd print i stars, where i is the number of time external loop executed.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 0; j < n - i; j++) {
    string += " ";
  }
  for (let k = 0; k < i; k++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 4. Downward Triangle Star Pattern.

```javascript
*****
****
***
**
*
```

<p>
To create a downward triangle star pattern use a nested loop, it is also known as a reverse star pattern. From the above-shown pattern, you can see the number of stars decreases from 'n' to 1.

Run a for loop inside an external loop whose number of iterations decreases from 'n' to 1.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 0; i < n; i++) {
  for (let k = 0; k < n - i; k++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 5. Javascript pyramid pattern.

```javascript
    *
   ***
  *****
 *******
*********
```

<p>
The Pyramid star pattern is a famous star pattern, you can see the shape of the pattern above.

It uses 2 loops inside the external loop one for printing spaces and the other to print stars.

The number of spaces in a row is n - i in each row and the number of stars in a row is 2 \* i - 1.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 1; j <= n - i; j++) {
    string += " ";
  }
  for (let k = 0; k < 2 * i - 1; k++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 6. Reversed pyramid star pattern.

```javascript
*********
 *******
  *****
   ***
    *
```

<p>
The reversed pyramid star pattern is a pyramid pattern upside-down.

It uses 2 loops inside the external loop one for printing spaces and the other to print the star. First loop prints spaces and other loop print stars. Here is the code of the reverse pyramid star pattern.

The number of spaces in a row is i and the number of stars is 2 \* (n - i) - 1.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 0; i < n; i++) {
  for (let j = 0; j < i; j++) {
    string += " ";
  }
  for (let k = 0; k < 2 * (n - i) - 1; k++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 7. Diamond pattern in javascript.

```javascript
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
```

<p>
The diamond star pattern is a combination of the pyramid and the reverse pyramid star pattern.

Observe in the above pattern it is a pyramid and a reverse pyramid together. Use the above concepts to create a diamond shape.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = n; j > i; j--) {
    string += " ";
  }
  for (let k = 0; k < i * 2 - 1; k++) {
    string += "*";
  }
  string += "\n";
}

for (let i = 1; i <= n - 1; i++) {
  for (let j = 0; j < i; j++) {
    string += " ";
  }
  for (let k = (n - i) * 2 - 1; k > 0; k--) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 8. Hourglass star pattern.

```javascript
*********
 *******
  *****
   ***
    *
   ***
  *****
 *******
*********
```

<p>
The hourglass star pattern is also made up of pyramid and reverse pyramid star pattern.

Observe in the above pattern it is a reverse pyramid and a pyramid together. Use the above concepts to create a diamond shape.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 0; i < n; i++) {
  for (let j = 0; j < i; j++) {
    string += " ";
  }
  for (let k = 0; k < (n - i) * 2 - 1; k++) {
    string += "*";
  }
  string += "\n";
}

for (let i = 2; i <= n; i++) {
  for (let j = n; j > i; j--) {
    string += " ";
  }
  for (let k = 0; k < i * 2 - 1; k++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 9. Right pascal star pattern.

```javascript
*
**
***
****
*****
****
***
**
*
```

<p>
The right pascal star pattern is created using 2 nested loops.

You can observe in the above pattern it is nothing but the right triangle star pattern and reversed triangle star pattern together. Here is the code for the right pascal star pattern.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 0; j < i; j++) {
    string += "*";
  }
  string += "\n";
}

for (let i = 1; i <= n - 1; i++) {
  for (let j = 0; j < n - i; j++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---

###### 10. Left pascal star pattern.

```javascript
    *
   **
  ***
 ****
*****
 ****
  ***
   **
    *
```

<p>
The left pascal star pattern is also created using 2 nested loops.

It is the same as the right pascal star pattern just mirrored. Here is the code for the right pascal star pattern.

</p>

<details><summary><b>Answer</b></summary>

```javascript
let n = 5;
let string = "";

for (let i = 1; i <= n; i++) {
  for (let j = 0; j < n - i; j++) {
    string += " ";
  }
  for (let k = 0; k < i; k++) {
    string += "*";
  }
  string += "\n";
}

for (let i = 1; i <= n - 1; i++) {
  for (let j = 0; j < i; j++) {
    string += " ";
  }
  for (let k = 0; k < n - i; k++) {
    string += "*";
  }
  string += "\n";
}
console.log(string);
```

</details>

---
  
<h3 align="center"> Questions on "This" keyword </h3>
  
###### 1. What logs to console in the following code snippet?
  
```javascript
const object = {
  message: 'Hello, World!',

  getMessage() {
    const message = 'Hello, Earth!';
    return this.message;
  }
};

console.log(object.getMessage()); // What is logged?
```

<details><summary><b>Answer</b></summary>
  <p>
    'Hello, World!' is logged to console. 
    
    -object.getMessage() is a method invocation, that’s why 'this' inside the method equals 'object'.

    -There’s also a variable declaration  const message = 'Hello, Earth!'  inside the method. 
    
    -The variable doesn’t influence anyhow the value of 'this.message'.
  </p>
</details>  
  
---  
  
###### 2. What logs to console in the following code snippet?
  
```javascript
function Pet(name) {
  this.name = name;

  this.getName = () => this.name;
}

const cat = new Pet('Fluffy');

console.log(cat.getName()); // What is logged?

const { getName } = cat;
console.log(getName());     // What is logged?
```

<details><summary><b>Answer</b></summary>
  <p>
  'Fluffy' and 'Fluffy' are logged to console.  
  
  ```
  -When a function is invoked as a constructor new Pet('Fluffy'), this inside the constructor function equals the constructed 
  
   object.

  -this.name = name expression inside Pet constructor creates name property on the constructed object.

  -this.getName = () => this.name creates a method getName on the constructed object. 
    
  -And since the arrow function is used, this inside the arrow function equals to this of the outer scope — the constructor 
    
   function Pet.

  -Invoking cat.getName(), as well as getName(), returns the expression this.name that evaluates to 'Fluffy'.
  ```
  </p>
</details>

---  
  
###### 3. What logs to console in the following code snippet?
  
```javascript
const object = {
  message: 'Hello, World!',

  logMessage() {
    console.log(this.message); // What is logged?
  }
};

setTimeout(object.logMessage, 1000);
```

<details><summary><b>Answer</b></summary>
  <p>
  After a delay of 1 second, undefined is logged to console.
  
  ```
  -While setTimeout() function uses the object.logMessage as a callback, still, it inovkes object.logMessage as a regular 
    
   function, rather than a method.

  -And during a regular function invocation this equals the global object, which is window in the case of the browser 
    
   environment.

  -That’s why console.log(this.message) inside logMessage method logs window.message, which is undefined.
  ```
  </p>
</details>
 
---
  
###### 4. How can you call logMessage function so that it logs "Hello, World!"?
  
```javascript
const object = {
  message: 'Hello, World!'
};

function logMessage() {
  console.log(this.message); // "Hello, World!"
}
```

<details><summary><b>Answer</b></summary>
  <p>
  There are at least 3 ways how to call logMessage() as a method on the object. Any of them is considered a correct answer:
  
 ```javascript
  const object = {
  message: 'Hello, World!'
};

function logMessage() {
  console.log(this.message); // logs 'Hello, World!'
}

// Using func.call() method
logMessage.call(object);

// Using func.apply() method
logMessage.apply(object);

// Creating a bound function
const boundLogMessage = logMessage.bind(object);
boundLogMessage();
```
  </p>
</details>
 
---  
  
###### 5. What logs to console in the following code snippet?
  
```javascript
const object = {
  who: 'World',

  greet() {
    return `Hello, ${this.who}!`;
  },

  farewell: () => {
    return `Goodbye, ${this.who}!`;
  }
};

console.log(object.greet());    // What is logged?
console.log(object.farewell()); // What is logged?
```

<details><summary><b>Answer</b></summary>
  <p>
  'Hello, World!' and 'Goodbye, undefined!' are logged to console.
  
  ```
  -When calling object.greet(), inside the method greet() this value equals object because greet is a regular function. 
    
  -Thus object.greet() returns 'Hello, World!'.

  -But farewell() is an arrow function, so this value inside of an arrow function always equals this of the outer scope.

  -The outer scope of farewell() is the global scope, where this is the global object.
   
  -Thus object.farewell() actually returns 'Goodbye, ${window.who}!', which evaluates to 'Goodbye, undefined!'.
  ```
  </p>
</details>
 
---
  
###### 6. What logs to console in the following code snippet?
  
```javascript
var length = 4;
function callback() {
  console.log(this.length); // What is logged?
}

const object = {
  length: 5,
  method(callback) {
    callback();
  }
};

object.method(callback, 1, 2);
```

<details><summary><b>Answer</b></summary>
  <p>
  4 is logged to console. 
  
  ```  
  -callback() is called using regular function invocation inside method(). Since this value during a regular function 
    
   invocation equals the global object, this.length is evaluated as window.length inside callback() function.

  -The first statement var length = 4, being in the outermost scope, creates a property length on the global object: 
    
   window.length becomes 4.

  -Finally, inside the callback() function this.length evaluates as window.length — 4 being logged to console.
  ```
  </p>
</details>
 
---

###### 7. What logs to console in the following code snippet?
  
```javascript
var length = 10;
function fn() {
  console.log(this.length); // What is logged?
}

var obj = {
  length: 5,
  method: function (fn) {
    fn();
    arguments[0]();
  },
};

obj.method(fn, 1);
```

<details><summary><b>Answer</b></summary>
  <p>
  10 and 2 are logged to console.
  
  ```  
  Why isn’t it 10 and 5?

  -In the first place, as fn is passed as a parameter to the function method, the scope (this) of the function fn is window. 
    
   var length = 10; is declared at the window level. It also can be accessed as window.length or length or this.length 
    
   (when this === window.)

  -method is bound to Object obj, and obj.method is called with parameters fn and 1. Though method is accepting only one 
    
   parameter, while invoking it has passed two parameters; the first is a function callback and other is just a number.

  -When fn() is called inside method, which was passed the function as a parameter at the global level, this.length will have 
    
   access to var length = 10 (declared globally) not length = 5 as defined in Object obj.

  -Now, we know that we can access any number of arguments in a JavaScript function using the arguments[] array.

  -Hence arguments[0]() is nothing but calling fn(). Inside fn now, the scope of this function becomes the arguments array, 
    
   and logging the length of arguments[] will return 2.
  ```
  </p>
</details>
 
---
  
###### 8. What logs to console in the following code snippet?
  
```javascript
var length = 4;
function callback() {
  console.log(this.length); // What is logged?
}

const object = {
  length: 5,
  method() {
    arguments[0]();
  }
};

object.method(callback, 1, 2);
```

<details><summary><b>Answer</b></summary>
  <p>
  3 is logged to console.
  
  ```  
  -obj.method(callback, 1, 2) is invoked with 3 arguments: callback, 1 and 2. As result the arguments special variable 
    
   inside method() is an array-like object of the following structure:
    
  {
    0: callback,
    1: 1, 
    2: 2, 
    length: 3 
  }
  
  -Because arguments[0]() is a method invocation of callback on arguments object, this inside the callback equals arguments. 
    
   As result this.length inside callback() is same as arguments.length — which is 3.
  ```
  </p>
</details>
 
---
  
<div align="center">
  <img height="60" src="https://img.icons8.com/ultraviolet/80/000000/react--v2.png"/>
  <h1>React Questions</h1>
  
  From basic to advanced: test how well you know React, refresh your knowledge a bit, or prepare for your coding interview! 💪 🚀
</div>
  
###### 1. Explain the lifecycle methods of components?

<details><summary><b>Answer</b></summary>

- **getInitialState()**: This is executed before the creation of the component.
- **componentDidMount()**: Is executed when the component gets rendered and placed on the DOM.
- **shouldComponentUpdate()**: Is invoked when a component determines changes to the DOM and returns a “true” or “false” value based on certain conditions.
- **componentDidUpdate()**: Is invoked immediately after rendering takes place.
- **componentWillUnmount()**: Is invoked immediately before a component is destroyed and unmounted permanently.

</details>

---
  



  
