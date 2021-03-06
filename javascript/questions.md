## Explain event delegation.
```
Event delegation
Capturing and bubbling allow us to implement one of most powerful event handling patterns called event delegation.

The idea is that if we have a lot of elements handled in a similar way, then instead of assigning a handler to each of them – we put a single handler on their common ancestor.

In the handler we get event.target to see where the event actually happened and handle it.
```


### Explain how "this" works in JavaScript. Can you give an example of one of the ways that working with this has changed in ES6?
```
What is this?
The JavaScript this keyword refers to the object it belongs to.

It has different values depending on where it is used:

- In a method, this refers to the owner object.
- Alone, this refers to the global object.
- In a function, this refers to the global object.
- In a function, in strict mode, this is undefined.
- In an event, this refers to the element that received the event.
- Methods like call(), and apply() can refer this to any object.
```

### Explain how prototypal inheritance works.
```
In JavaScript, all functions are also objects, which means that they can have properties. And as it so happens, they all have a property called `prototype`, which is also an object.

function foo() {
}
typeof foo.prototype // ‘object’

JavaScript uses an inheritance model called “differential inheritance”. What that means is that methods aren’t copied from parent to child. Instead, children have an “invisible link” back to their parent object.

function Dog() {
}
Dog.prototype.bark = function() {
 console.log(‘woof!’);
};
var fido = new Dog();
fido.bark(); // ‘woof!’

What actually happens when I write fido.bark() is this:
1. The JS engine looks for a property called bark on our fido object.
2. It doesn’t find one, so it looks “up the prototype chain” to fido’s parent, which is Dog.prototype.
3. It finds Dog.prototype.bark, and calls it with this bound to fido.

There’s really no such property as fido.bark. It doesn’t exist. Instead, fido has access to the bark() method on Dog.prototype because it’s an instance of Dog. This is the “invisible link” I mentioned. More commonly, it’s referred to as the “prototype chain”.

```

### What is the difference in Debouncing & Throttling?

```
Debouncing - Skipping function call between two events execution like two keypress event in search bar.

Throttling - Halts calling of an api/function between two function call till an interval is over.
```

What's the difference between a variable that is: null, undefined or undeclared?
How would you go about checking for any of these states?

### What is a closure, and how/why would you use one?

```
In javascript, an inner function enclose the scope along with its out functions lexical scope is called closure.
```

What language constructions do you use for iterating over object properties and array items?

Can you describe the main difference between the Array.forEach() loop and Array.map() methods and why you would pick one versus the other?
What's a typical use case for anonymous functions?
What's the difference between host objects and native objects?
Explain the difference between: function Person(){}, var person = Person(), and var person = new Person()?
Explain the differences on the usage of foo between function foo() {} and var foo = function() {}
Can you explain what Function.call and Function.apply do? What's the notable difference between the two?
Explain Function.prototype.bind.
What's the difference between feature detection, feature inference, and using the UA string?
Explain "hoisting".
Describe event bubbling.
Describe event capturing.
What's the difference between an "attribute" and a "property"?
What are the pros and cons of extending built-in JavaScript objects?
What is the difference between == and ===?
Explain the same-origin policy with regards to JavaScript.
Why is it called a Ternary operator, what does the word "Ternary" indicate?
What is strict mode? What are some of the advantages/disadvantages of using it?
What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
What tools and techniques do you use debugging JavaScript code?
Explain the difference between mutable and immutable objects.
What is an example of an immutable object in JavaScript?
What are the pros and cons of immutability?
How can you achieve immutability in your own code?
Explain the difference between synchronous and asynchronous functions.
What is event loop?
What is the difference between call stack and task queue?
What are the differences between variables created using let, var or const?
What are the differences between ES6 class and ES5 function constructors?
Can you offer a use case for the new arrow => function syntax? How does this new syntax differ from other functions?
What advantage is there for using the arrow syntax for a method in a constructor?
What is the definition of a higher-order function?
Can you give an example for destructuring an object or an array?
Can you give an example of generating a string with ES6 Template Literals?
Can you give an example of a curry function and why this syntax offers an advantage?
What are the benefits of using spread syntax and how is it different from rest syntax?
How can you share code between files?
Why you might want to create static class members?
What is the difference between while and do-while loops in JavaScript?
What is a promise? Where and how would you use promise?
