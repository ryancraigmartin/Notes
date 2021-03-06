# Q & A

## What does it mean to be Asynchronous?

By default, many frameworks and runtime environments are `blocking`. This, at a very simple level, means you can only complete one instruction at a time, and cannot continue to the next instruction until the previous is done.

Javascript code runs on a single thread which means that it can only do one thing at a time.

Asynchronous code means that a programming language can complete instructions in a different order than they are written.

In Asynchronous code, requests are handed off to another thread so that the "code thread" can continue to move on to the next code block.

Once the data is retrieved the callback function from the request is adding on to the end of the thread at the end of the queue.

Synchronous code waits for one action to complete before moving on to the next. This delays the rest of the code.

When we looked at JavaScript, we learned that code executes from top to bottom, instruction by instruction sequentially. We can add loops and conditionals to construct the logic of our algorithms,but in the end, it’s just one instruction after another

---

## Framework vs. Toolkit vs. Library

The most important difference, and in fact the defining difference between a library and a framework is Inversion of Control.

What does this mean? Well, it means that when you call a library, you are in control. But with a framework, the control is inverted: the framework calls you. (This is called the Hollywood Principle: Don't call Us, We'll call You.) This is pretty much the definition of a framework. If it doesn't have Inversion of Control, it's not a framework. (I'm looking at you, .NET!)

Basically, all the control flow is already in the framework, and there's just a bunch of predefined white spots that you can fill out with your code.

A library on the other hand is a collection of functionality that you can call.

I don't know if the term toolkit is really well defined. Just the word "kit" seems to suggest some kind of modularity, i.e. a set of independent libraries that you can pick and choose from. What, then, makes a toolkit different from just a bunch of independent libraries? Integration: if you just have a bunch of independent libraries, there is no guarantee that they will work well together, whereas the libraries in a toolkit have been designed to work well together – you just don't have to use all of them.

But that's really just my interpretation of the term. Unlike library and framework, which are well-defined, I don't think that there is a widely accepted definition of toolkit.

**Martin Fowler** discusses the difference between a library and a framework in his article on Inversion of Control:

Inversion of Control is a key part of what makes a framework different to a library. A library is essentially a set of functions that you can call, these days usually organized into classes. Each call does some work and returns control to the client.

A framework embodies some abstract design, with more behavior built in. In order to use it you need to insert your behavior into various places in the framework either by subclassing or by plugging in your own classes. The framework's code then calls your code at these points.

To summarize: your code calls a library but a framework calls your code.

[StackOverflow Link](https://stackoverflow.com/questions/3057526/framework-vs-toolkit-vs-library)

---

## Difference between =, ==, & ===

= -  Assignment operator

== & != - Loose/Lenient equality and inequality. Try to convert values of different types before comparing them. (Type coercion)

=== & !== - Strict equality and inequality. Equal value and equal type.
Ex.
``` js
'hello world' === 'hello world'
// true (Both Strings & equal values)

77 === '77'
// false (Number v.s String)
```

[Speaking JavaScript: An In-Depth Guide for Programmers by Dr. Axel Rauschmayer](http://speakingjs.com/es5/ch09.html)

---
## Falsy values

There are only six falsy values in JavaScript you should be aware of:

- **null**
- **undefined**
- **false** —  boolean false
- **0**  —  number zero
- **NaN** —  Not A Number
- “”  —  empty string

---

## Method vs Function vs Procedure

Practically speaking, there's really no difference, with the slight exception that "method" usually refers to a subroutine associated with an object in Object Oriented languages.

The terms "procedure, function, subroutine, subprogram, and method" all really mean the same thing: a callable sub-program within a larger program. But it's difficult to come up with a definition that captures all variant usages of these terms, because they are not used consistently across programming languages or paradigms. The only exception is probably "method", which seems to be used almost entirely with Object Oriented languages, referring to a function that is associated with an object

[Source](https://softwareengineering.stackexchange.com/questions/20909/method-vs-function-vs-procedure)

---

## 8 HTTP Methods every Dev should know

- GET: fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource.
- POST: create a new resource. POST requests usually carry a payload that specifies the data for the new resource.
- PUT: update an existing resource. The payload may contain the updated data for the resource.
- PATCH: Used for making partial changes to an existing resource.
- DELETE: delete an existing resource.
- HEAD: this is similar to GET, but without the message body. It's used to retrieve the server headers for a particular resource, generally to check if the resource has changed, via timestamps.
- OPTIONS: used to retrieve the server capabilities. On the client-side, it can be used to modify the request based on what the server can support.
- TRACE: used to retrieve the hops that a request takes to round trip from the server. Each intermediate proxy or gateway would inject its IP or DNS name into the Via header field. This can be used for diagnostic purposes.

[HTTP: The Protocol Every Web Developer Must Know ](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)

## When to use PUT and when to use PATCH

When a client needs to replace an existing Resource entirely, they can use `PUT`. When they’re doing a partial update, they can use HTTP `PATCH`. Another important aspect to consider here is idempotence; `PUT` is idempotent; `PATCH` can be, but isn’t required to.

[REST API - PUT vs PATCH with real life examples](https://stackoverflow.com/questions/28459418/rest-api-put-vs-patch-with-real-life-examples)
[HTTP PUT vs HTTP PATCH in a REST API](http://www.baeldung.com/http-put-patch-difference-spring)

---

## Immutable vs Mutable objects

A mutable object is an object whose state can be modified after it is created.

Immutables are the objects whose state cannot be changed once the object is created.

---

- JavaScript is a *multi paradigm language*. A *paradigm* is a way of thinking about software construction based off of fundamental design principles. JavaScript supports imperative / procedural programming along with OOP, and functional programming. JS supports **OOP with prototypal inheritance** where app state is shared and colocated with methods in objects.

---

What is a `Object Oriented Programming`?
OOP is method of computer programming that involves using 'objects'. It allows a developer to concentrate on the relationships between objects which are usually at the heart of an application. An object is essentially a piece of code that lets you create many similar pieces of code without actually re-writing the code each time. This is done by first writing a 'class', which is essentially a blueprint of the object, then you can easily create an 'instance' of the object, which is basically just one particular version of the object, built from the blueprint.

- Inheritance = Objects can inherit features from other objects.

![Example:](https://cdn-images-1.medium.com/max/800/1*fdxNTeWlEeIQHwYSYLCn5g.jpeg)

- Polymorphism = Objects can share the same interface — how they are accessed and used — while their underlying implementation of the interface may differ.

- Encapsulation = Each object is responsible for specific tasks.

---

- What is `Functional Programming?`: One of the two pillars of JavaScript. Produces programs by composing mathematical functions, avoids `shared state` and mutable data. Focuses on function purity, avoiding side effects, simple function composition, & first class functions. FP is declarative rather than imperative, and app state flows through pure functions.

---

What is a `Closure?`

- Inner functions have **access to the actual parameters of the outer functions (not copies)**
- If an object is created as a result of a function and assigned to myObject, myObject continues to share access to the variables in the functions that created it (actual variables, not copies)
  - It has access to *the context in which it was created*  this is *closure*.
  - This includes later on, even if *the outer function has completed its execution and returned*, when the inner function is called, it will still have **access to all the variables it had access to at the time it was defined** (i.e. the variables that were *in context* when the inner function was defined)

It is most frequently used in data privacy, event handlers, callback functions, currying, and other functional programming.

>“Closure is when a function is able to remember and access its lexical scope even when the function is executing outside its lexical scope.” - Kyle Simpson

---

What are `Callbacks?`

* A *callback function* is a function passed to another function as a parameter and executed in this other function
* When making a request to a server, use an *asynchronous request* as asynchronous functions return immediately, therefore freeing up the client
	* In this example, we pass the callback function to the asynchronous request as a parameter so the callback function will only be called when a response is available
```javascript
request = prepare_the_request();
send_request_asynchronously(request, function(response){     //function being passed in as a parameter
	display(response);
});
```

---

What is a `promise?`: 
A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: fulfilled, rejected, or pending. Promise users can attach callbacks to handle the fulfilled value or the reason for rejection.

The then() function accepts 2 functions as parameters: a function to be executed when the promise is fulfilled, and a function to be executed when the promise is rejected.

Native JavaScript promises don’t expose promise states. Instead, you’re expected to treat the promise as a black box. Only the function responsible for creating the promise will have knowledge of the promise status, or access to resolve or reject.

[A standard for promises was defined by the Promises/A+ specification community.](https://promisesaplus.com/implementations)

> Kyle Simpson: "Think of a promise as being like a meal receipt at a fast-food restaurant. You order your meal and pay for it, and the clerk gives you a number that you need to claim the food when it is done. When the food comes out, the clerk calls your number and you exchange the receipt for the food. Promises work the same way. You've called a function, passed it some data, and received a promise in return. When the "food" is done, the function resolves the promise (calls your number) and passes you the result. Attaching a callback to the promise is your way of handing back the receipt."Why not just use a callback?" you may ask. Well, promises offer some control flow advantages that are kind of cumbersome to do with callbacks, but the real advantage is that the promise acts as a data escrow. A promise can never be resolved multiple times, will always be resolved asynchronously, bubbles up any errors that occur, and ensure that the code you're calling can't accidentally hang on to your calling context and create a memory leak. Callbacks have none of these abilities and can actually be dangerous for your application if a third party library handles them wrong."

- What is `async`/`await`?: Async Await was added to JavaScript to make working with asynchronous functions more enjoyable and easy to understand. It's built on top of promises and is compatible with existing Promise-based APIs.

`Async` - declares an asynchronous function `(async function someName(){...})`.
- Automatically transforms a regular function into a Promise.
- When called async functions resolve with whatever is returned in their body.
- Async functions enable the use of await.

`Await` - pauses the execution of async functions. `(var result = await someAsyncCall();)`.
- When placed in front of a Promise call, await forces the rest of the code to wait until that Promise finishes and returns a result.
- Await works only with Promises, it does not work with callbacks.
- Await can only be used inside async functions.

What is `recursion?` A recursive function is a function that calls itself, either directly or indirectly. It's a powerful programming technique in which a problem is divided into a set of similar sub problems, each solved with a trivial solution. Generally, a recursive function calls itself to solve its sub-problems. They can be very effective in manipulating tree structures such as the browser's DOM.

What is `Scope`? Scope in programming languages controls the visibility and lifetimes of variables and parameters. The parameters and variables defined inside of a function are not visible outside of the function, and a variable defined anywhere within a function is visible everywhere within that function. This reduces naming collisions and provides automatic memory management.

- A *block* is a set of statements contained in curly brackets {}
- Javascript **does not have block scope** but **does have function scope**
  - All variables declared *anywhere* within a function are **available everywhere in that function** - i.e. and inner function will have access to the variables of the outer function in which it is defined
  - A variable can be *overwritten* with a new value in an inner function and that new value's scope will be just the body of the inner function - as soon as you're back out to the outer function, the value of that variable will revert to what it was before the inner function began its execution
  - All variable should be **declared at the top of the function body**

---

What is `lexical scope`?
With (static) lexical scoping, the structure of the program source code determines what variables you are referring to.

---

What is `Hoisting`?

---

What is a `pure function`?

---

What is an `AJAX request`?

- *AJAX* = Asynchronous JavaScript and XML.

- *AJAX* is the technique used to exchange data with a server, and update parts of a web page and load portions of a page dynamically without reloading the whole page.
  - EX: Think of an online shopping cart.

Asynchronous is the important part of *AJAX*. Traditionally you load a web page all at the same time (right when you first click a link or type in an address). *AJAX* allows for delaying in loading parts of that data until some later time, usually based on user actions.

[What is `use strict / strict mode`?](https://stackoverflow.com/questions/1335851/what-does-use-strict-do-in-javascript-and-what-is-the-reasoning-behind-it)

Strict Mode is a new feature in ECMAScript 5 that allows you to place a program, or a function, in a "strict" operating context. This strict context prevents certain actions from being taken and throws more exceptions.

Strict mode helps out in a couple ways:

It catches some common coding bloopers, throwing exceptions.
It prevents, or throws errors, when relatively "unsafe" actions are taken (such as gaining access to the global object).
It disables features that are confusing or poorly thought out.
Also note you can apply "strict mode" to the whole file... Or you can use it only for a specific function (still quoting from John Resig's article):

``` js
// Non-strict code...

(function(){
  "use strict";

  // Define your library strictly...
})();

// Non-strict code...
```