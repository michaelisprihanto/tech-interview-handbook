JavaScript
==

WIP.

## Contents

- [Glossary](#glossary)
- [Core Language](#core-language)
- [Design Patterns](#design-patterns)
- [Strict Mode](#strict-mode)

## Glossary

- **Closure** - TBD
- **Event Loop** - The event loop is a single-threaded loop that monitors the call stack and checks if there is any work to be done in the message queue. If the call stack is empty and there are callback functions in the message queue, a message is dequeued and pushed onto the call stack to be executed.
- **Hoisting** - TBD
- **Promise** - TBD
- **Prototype** - TBD
- **This** - The `this` keyword does not refer to the function in which it is used or it’s scope. It refers to the object on which a function is being executed and depends entirely on the call-site of the function.

## Core Language

### Variables

- https://github.com/getify/You-Dont-Know-JS/blob/master/types%20&%20grammar/README.md#you-dont-know-js-types--grammar
- Types
- Scopes
- Coercion

### Functions

- https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20&%20closures/README.md#you-dont-know-js-scope--closures
- Declaration vs Expression
- Closures
- `.call`, `.apply` and `.bind`
- Currying
- Arrow functions and lexical this

### Prototypes and Objects

- Reference: https://github.com/getify/You-Dont-Know-JS/blob/master/this%20%26%20object%20prototypes/README.md
- Prototype chain
- `this` keyword
  - https://rainsoft.io/gentle-explanation-of-this-in-javascript/
  - https://codeburst.io/the-simple-rules-to-this-in-javascript-35d97f31bde3
- Classes
  - Methods
    - Use non-arrow functions for methods that will be called using the `object.method()` syntax because you need the value of `this` to point to the instance itself.

### Async

- Reference: https://github.com/getify/You-Dont-Know-JS/blob/master/async%20&%20performance/README.md#you-dont-know-js-async--performance
- `setTimeout` and `setInterval`
- Event Loop
  -
- Debounce and Throttle
  - Throttling enforces a maximum number of times a function can be called over time.
  - Debouncing enforces that a function not be called again until a certain amount of time has passed without it being called.
  - https://css-tricks.com/debouncing-throttling-explained-examples/
- Callbacks
- Promises

**Reference**

- https://www.vikingcodeschool.com/falling-in-love-with-javascript/the-javascript-event-loop

## Design Patterns

- https://addyosmani.com/resources/essentialjsdesignpatterns/book/

## Strict Mode

1. Strict mode eliminates some JavaScript silent errors by changing them to throw errors.
1. Strict mode fixes mistakes that make it difficult for JavaScript engines to perform optimizations. Strict mode code can sometimes be made to run faster than identical code that's not strict mode.
1. Strict mode prohibits some syntax likely to be defined in future versions of ECMAScript.

**Converting Mistakes into Errors**

- Prevent accidental creation of global variables.
- Makes assignments which would otherwise silently fail throw an exception.
- Makes attempts to delete undeletable properties throw errors.
- Requires that all properties named in an object literal be unique. Duplicate property names are a syntax error in strict mode.
- Requires that function parameter names be unique. In normal code the last duplicated argument hides previous identically-named arguments.
- Forbids setting properties on primitive values in ES6. Without strict mode, setting properties is simply ignored (no-op), with strict mode, however, a `TypeError` is thrown.

**Simplifying Variable Uses**

- Prohibits `with`.
- `eval` of strict mode code does not introduce new variables into the surrounding scope.
- Forbids deleting plain variables. `delete` name in strict mode is a syntax error: `var x; delete x; // !!! syntax error`.

**Paving the way for future ECMAScript versions**

- Future ECMAScript versions will likely introduce new syntax, and strict mode in ECMAScript 5 applies some restrictions to ease the transition. It will be easier to make some changes if the foundations of those changes are prohibited in strict mode.
- First, in strict mode a short list of identifiers become reserved keywords. These words are `implements`, `interface`, `let`, `package`, `private`, `protected`, `public`, `static`, and `yield`. In strict mode, then, you can't name or use variables or arguments with these names.
- Second, strict mode prohibits function statements not at the top level of a script or function.

## Useful Links

- https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95#.l2n8icwl4
- https://github.com/mbeaudru/modern-js-cheatsheet
