# JavaScript Interview Prep - Complete Question Bank

> **150 Predict-the-Output Questions** covering Basics, Medium, and Advanced JavaScript concepts for interview preparation.

---

## 📚 Table of Contents

- [1. Basics (50 Questions)](#1-basics-50-questions)
  - [Core Concepts](#core-concepts)
  - [Hoisting & Scope](#hoisting--scope)
  - [Type Coercion](#type-coercion)
  - [Functions](#functions)
  - [Objects & Arrays](#objects--arrays)
  - [String Methods](#string-methods)
  - [Number Operations](#number-operations)
  - [Miscellaneous](#miscellaneous)
- [2. Medium (50 Questions)](#2-medium-50-questions)
  - [Closures & Scope Chain](#closures--scope-chain)
  - [this Keyword](#this-keyword)
  - [Prototypes](#prototypes)
  - [Array Methods](#array-methods)
  - [Promises & Async](#promises--async)
  - [Destructuring](#destructuring)
  - [Spread & Rest](#spread--rest)
  - [Object Methods](#object-methods)
  - [Event Loop](#event-loop)
- [3. Advanced (50 Questions)](#3-advanced-50-questions)
  - [Advanced Closures](#advanced-closures)
  - [Advanced this Binding](#advanced-this-binding)
  - [Prototype Chain Deep Dive](#prototype-chain-deep-dive)
  - [Complex Async Patterns](#complex-async-patterns)
  - [Generators](#generators)
  - [Symbol & Iterators](#symbol--iterators)
  - [Proxy & Reflect](#proxy--reflect)
  - [WeakMap & WeakSet](#weakmap--weakset)
  - [Advanced Array & Object Operations](#advanced-array--object-operations)
  - [Complex Type Coercion](#complex-type-coercion)
- [Important Full Forms](#important-full-forms)

---

## 1. BASICS (50 Questions)

### Core Concepts

**1.** `var x = 5; var x = 10; console.log(x);` - Output?

**2.** `let y = 5; let y = 10; console.log(y);` - Output?

**3.** `const z = [1,2]; z.push(3); console.log(z);` - Output?

**4.** `const obj = {a:1}; obj = {b:2}; console.log(obj);` - Output?

**5.** `console.log(typeof null);` - Output?

**6.** `console.log(typeof undefined);` - Output?

**7.** `console.log(typeof NaN);` - Output?

**8.** `console.log(5 == "5");` - Output?

**9.** `console.log(5 === "5");` - Output?

**10.** `console.log(null == undefined);` - Output?

---

### Hoisting & Scope

**11.** `console.log(a); var a = 10;` - Output?

**12.** `console.log(b); let b = 20;` - Output?

**13.** `var x = 1; { var x = 2; } console.log(x);` - Output?

**14.** `let y = 1; { let y = 2; } console.log(y);` - Output?

**15.** `function test() { console.log(x); var x = 5; } test();` - Output?

---

### Type Coercion

**16.** `console.log("5" + 3);` - Output?

**17.** `console.log("5" - 3);` - Output?

**18.** `console.log(true + 1);` - Output?

**19.** `console.log(false + 1);` - Output?

**20.** `console.log("hello" - 1);` - Output?

**21.** `console.log([] + []);` - Output?

**22.** `console.log([] + {});` - Output?

**23.** `console.log({} + []);` - Output?

**24.** `console.log(!![]);` - Output?

**25.** `console.log(!!{});` - Output?

---

### Functions

**26.** `function test() { return; { name: "JS" }; } console.log(test());` - Output?

**27.** `var x = function() { console.log("A"); }; x();` - Output?

**28.** `(function() { console.log("IIFE"); })();` - Output?

**29.** `function outer() { var x = 10; function inner() { console.log(x); } return inner; } var fn = outer(); fn();` - Output?

**30.** `const arrow = () => { return "arrow"; }; console.log(arrow());` - Output?

---

### Objects & Arrays

**31.** `var obj = {a: 1, b: 2}; delete obj.a; console.log(obj);` - Output?

**32.** `var arr = [1, 2, 3]; delete arr[1]; console.log(arr);` - Output?

**33.** `var arr = [1, 2, 3]; arr.length = 0; console.log(arr);` - Output?

**34.** `console.log([1, 2, 3] == [1, 2, 3]);` - Output?

**35.** `var a = [1, 2]; var b = a; b.push(3); console.log(a);` - Output?

---

### String Methods

**36.** `console.log("hello".toUpperCase());` - Output?

**37.** `console.log("WORLD".toLowerCase());` - Output?

**38.** `console.log("javascript".charAt(0));` - Output?

**39.** `console.log("hello world".split(" "));` - Output?

**40.** `console.log("abc".repeat(3));` - Output?

---

### Number Operations

**41.** `console.log(0.1 + 0.2 === 0.3);` - Output?

**42.** `console.log(Math.floor(4.9));` - Output?

**43.** `console.log(Math.ceil(4.1));` - Output?

**44.** `console.log(Math.round(4.5));` - Output?

**45.** `console.log(parseInt("123px"));` - Output?

---

### Miscellaneous

**46.** `console.log(1 < 2 < 3);` - Output?

**47.** `console.log(3 > 2 > 1);` - Output?

**48.** `console.log(typeof typeof 1);` - Output?

**49.** `var x; console.log(x);` - Output?

**50.** `console.log(!!null);` - Output?

---

## 2. MEDIUM (50 Questions)

### Closures & Scope Chain

**51.** `for(var i = 0; i < 3; i++) { setTimeout(() => console.log(i), 100); }` - Output?

**52.** `for(let i = 0; i < 3; i++) { setTimeout(() => console.log(i), 100); }` - Output?

**53.** `function outer() { var x = 10; return function() { console.log(x++); } } var fn = outer(); fn(); fn();` - Output?

**54.** `var x = 10; function test() { console.log(x); var x = 20; } test();` - Output?

**55.** `var a = 1; function b() { a = 10; return; function a() {} } b(); console.log(a);` - Output?

---

### this Keyword

**56.** `var obj = { name: "JS", getName: function() { console.log(this.name); } }; obj.getName();` - Output?

**57.** `var obj = { name: "JS", getName: () => console.log(this.name) }; obj.getName();` - Output?

**58.** `function test() { console.log(this); } test();` - Output?

**59.** `var obj = { test: function() { console.log(this); } }; var fn = obj.test; fn();` - Output?

**60.** `var obj = { test: function() { setTimeout(function() { console.log(this); }, 100); } }; obj.test();` - Output?

---

### Prototypes

**61.** `function Person(name) { this.name = name; } Person.prototype.greet = function() { return "Hi"; }; var p = new Person("JS"); console.log(p.greet());` - Output?

**62.** `var arr = [1, 2, 3]; console.log(arr.__proto__ === Array.prototype);` - Output?

**63.** `function Car() {} var c = new Car(); console.log(c.constructor === Car);` - Output?

**64.** `var obj = Object.create(null); console.log(obj.toString);` - Output?

**65.** `var a = {}; var b = {}; console.log(a.prototype === b.prototype);` - Output?

---

### Array Methods

**66.** `var arr = [1, 2, 3, 4]; console.log(arr.map(x => x * 2));` - Output?

**67.** `var arr = [1, 2, 3, 4]; console.log(arr.filter(x => x > 2));` - Output?

**68.** `var arr = [1, 2, 3, 4]; console.log(arr.reduce((acc, val) => acc + val, 0));` - Output?

**69.** `var arr = [1, 2, 3]; arr.forEach(x => console.log(x)); console.log("done");` - Output?

**70.** `var arr = [1, 2, 3]; console.log(arr.slice(1, 2));` - Output?

**71.** `var arr = [1, 2, 3]; arr.splice(1, 1); console.log(arr);` - Output?

**72.** `console.log([1, 2] + [3, 4]);` - Output?

**73.** `console.log([..."hello"]);` - Output?

**74.** `var arr = [1, [2, [3]]]; console.log(arr.flat(2));` - Output?

**75.** `console.log([1, 2, 3].some(x => x > 2));` - Output?

---

### Promises & Async

**76.** `console.log("1"); Promise.resolve().then(() => console.log("2")); console.log("3");` - Output?

**77.** `async function test() { return "hello"; } test().then(console.log);` - Output?

**78.** `Promise.resolve(1).then(x => x + 1).then(x => console.log(x));` - Output?

**79.** `Promise.reject("error").catch(e => console.log(e));` - Output?

**80.** `console.log("1"); setTimeout(() => console.log("2"), 0); Promise.resolve().then(() => console.log("3")); console.log("4");` - Output?

---

### Destructuring

**81.** `var [a, b] = [1, 2, 3]; console.log(a, b);` - Output?

**82.** `var {x, y} = {x: 1, y: 2, z: 3}; console.log(x, y);` - Output?

**83.** `var {a: newName} = {a: 10}; console.log(newName);` - Output?

**84.** `var [a, ...rest] = [1, 2, 3, 4]; console.log(rest);` - Output?

**85.** `var {a = 10} = {}; console.log(a);` - Output?

---

### Spread & Rest

**86.** `var arr1 = [1, 2]; var arr2 = [...arr1, 3]; console.log(arr2);` - Output?

**87.** `var obj1 = {a: 1}; var obj2 = {...obj1, b: 2}; console.log(obj2);` - Output?

**88.** `function sum(...args) { return args.reduce((a, b) => a + b); } console.log(sum(1, 2, 3));` - Output?

**89.** `var arr = [1, 2, 3]; console.log(Math.max(...arr));` - Output?

**90.** `var str = "hello"; console.log([...str]);` - Output?

---

### Object Methods

**91.** `var obj = {a: 1, b: 2}; console.log(Object.keys(obj));` - Output?

**92.** `var obj = {a: 1, b: 2}; console.log(Object.values(obj));` - Output?

**93.** `var obj = {a: 1, b: 2}; console.log(Object.entries(obj));` - Output?

**94.** `var obj1 = {a: 1}; var obj2 = Object.assign({}, obj1, {b: 2}); console.log(obj2);` - Output?

**95.** `var obj = {a: 1}; Object.freeze(obj); obj.a = 2; console.log(obj.a);` - Output?

---

### Event Loop

**96.** `console.log("1"); setTimeout(() => console.log("2"), 0); console.log("3");` - Output?

**97.** `for(var i = 1; i <= 3; i++) { setTimeout(() => console.log(i), i * 1000); }` - Output?

**98.** `Promise.resolve().then(() => console.log("1")); setTimeout(() => console.log("2"), 0);` - Output?

**99.** `console.log("start"); async function test() { console.log("async"); } test(); console.log("end");` - Output?

**100.** `setImmediate(() => console.log("immediate")); setTimeout(() => console.log("timeout"), 0);` - Output (Node.js)?

---

## 3. ADVANCED (50 Questions)

### Advanced Closures

**101.** `function createCounter() { let count = 0; return { inc: () => ++count, dec: () => --count, get: () => count }; } var c = createCounter(); c.inc(); c.inc(); console.log(c.get());` - Output?

**102.** `var funcs = []; for(var i = 0; i < 3; i++) { funcs[i] = (function(x) { return function() { console.log(x); } })(i); } funcs[0](); funcs[1](); funcs[2]();` - Output?

**103.** `function outer() { var x = 10; return { get: () => x, set: (val) => x = val }; } var obj = outer(); obj.set(20); console.log(obj.get());` - Output?

**104.** `var x = 10; (function() { console.log(x); var x = 20; })();` - Output?

**105.** `let x = 10; { console.log(x); let x = 20; }` - Output?

---

### Advanced this Binding

**106.** `var obj = { value: 10, test: function() { var inner = () => { console.log(this.value); }; inner(); } }; obj.test();` - Output?

**107.** `function Person(name) { this.name = name; } var p1 = new Person("A"); var p2 = Person("B"); console.log(p1.name, window.name);` - Output?

**108.** `var obj = { test: function() { return this; } }; console.log(obj.test() === obj);` - Output?

**109.** `var obj = { test: function() { return this; } }; var fn = obj.test; console.log(fn() === window);` - Output?

**110.** `var obj = { val: 10, test: function() { console.log(this.val); } }; setTimeout(obj.test, 100);` - Output?

---

### Prototype Chain Deep Dive

**111.** `function Animal() {} Animal.prototype.eat = function() { return "eating"; }; function Dog() {} Dog.prototype = Object.create(Animal.prototype); var d = new Dog(); console.log(d.eat());` - Output?

**112.** `var obj = { a: 1 }; var child = Object.create(obj); child.b = 2; console.log(child.a, child.b);` - Output?

**113.** `function F() {} var f = new F(); F.prototype = { a: 1 }; console.log(f.a);` - Output?

**114.** `var obj = {}; console.log(obj.hasOwnProperty('toString'));` - Output?

**115.** `Array.prototype.myMethod = function() { return "custom"; }; var arr = [1, 2]; console.log(arr.myMethod());` - Output?

---

### Complex Async Patterns

**116.** `async function f1() { console.log("1"); await f2(); console.log("2"); } async function f2() { console.log("3"); } f1(); console.log("4");` - Output order?

**117.** `Promise.resolve(1).then(x => { console.log(x); return x + 1; }).then(x => { console.log(x); });` - Output?

**118.** `Promise.all([Promise.resolve(1), Promise.resolve(2)]).then(console.log);` - Output?

**119.** `Promise.race([new Promise(res => setTimeout(() => res(1), 100)), Promise.resolve(2)]).then(console.log);` - Output?

**120.** `async function test() { try { await Promise.reject("error"); } catch(e) { console.log(e); } } test();` - Output?

---

### Generators

**121.** `function* gen() { yield 1; yield 2; yield 3; } var g = gen(); console.log(g.next().value);` - Output?

**122.** `function* gen() { yield 1; yield 2; } var g = gen(); console.log(g.next(), g.next(), g.next());` - Output?

**123.** `function* gen() { var x = yield 1; console.log(x); } var g = gen(); g.next(); g.next(10);` - Output?

**124.** `function* gen() { yield* [1, 2, 3]; } var g = gen(); console.log([...g]);` - Output?

**125.** `function* infinite() { let i = 0; while(true) yield i++; } var g = infinite(); console.log(g.next().value, g.next().value);` - Output?

---

### Symbol & Iterators

**126.** `var sym1 = Symbol('test'); var sym2 = Symbol('test'); console.log(sym1 === sym2);` - Output?

**127.** `var obj = { [Symbol('key')]: 'value' }; console.log(Object.keys(obj));` - Output?

**128.** `var arr = [1, 2, 3]; var iterator = arr[Symbol.iterator](); console.log(iterator.next().value);` - Output?

**129.** `var obj = { *[Symbol.iterator]() { yield 1; yield 2; } }; console.log([...obj]);` - Output?

**130.** `console.log(Symbol.for('test') === Symbol.for('test'));` - Output?

---

### Proxy & Reflect

**131.** `var obj = new Proxy({}, { get: (target, prop) => { return prop in target ? target[prop] : 'default'; } }); console.log(obj.name);` - Output?

**132.** `var arr = new Proxy([], { set: (target, prop, value) => { console.log('setting', prop); target[prop] = value; return true; } }); arr.push(1);` - Output?

**133.** `var obj = { a: 1 }; console.log(Reflect.has(obj, 'a'));` - Output?

**134.** `var obj = { a: 1 }; Reflect.deleteProperty(obj, 'a'); console.log(obj);` - Output?

**135.** `var obj = {}; Reflect.set(obj, 'name', 'JS'); console.log(obj.name);` - Output?

---

### WeakMap & WeakSet

**136.** `var wm = new WeakMap(); var obj = {}; wm.set(obj, 'value'); console.log(wm.get(obj));` - Output?

**137.** `var ws = new WeakSet(); var obj = {}; ws.add(obj); console.log(ws.has(obj));` - Output?

**138.** `var wm = new WeakMap(); var key = {id: 1}; wm.set(key, 'data'); key = null;` - What happens to WeakMap entry?

**139.** `var map = new Map(); map.set('a', 1); console.log(map.size);` - Output?

**140.** `var set = new Set([1, 2, 2, 3]); console.log(set.size);` - Output?

---

### Advanced Array & Object Operations

**141.** `var arr = [1, 2, 3]; Array.prototype.push.call(arr, 4, 5); console.log(arr);` - Output?

**142.** `var obj = { length: 2, 0: 'a', 1: 'b' }; console.log(Array.prototype.slice.call(obj));` - Output?

**143.** `console.log([1, 2, 3].flatMap(x => [x, x * 2]));` - Output?

**144.** `var arr = [1, 2, 3]; arr.copyWithin(0, 1, 2); console.log(arr);` - Output?

**145.** `console.log([1, 2, 3].reduceRight((acc, val) => acc - val, 10));` - Output?

---

### Complex Type Coercion

**146.** `console.log([] == ![]);` - Output?

**147.** `console.log([] == false);` - Output?

**148.** `console.log({} == {});` - Output?

**149.** `var obj = { valueOf: () => 42 }; console.log(obj + 0);` - Output?

**150.** `var obj = { toString: () => "hello", valueOf: () => 42 }; console.log(String(obj));` - Output?

---

## 📖 Important Full Forms

### JavaScript Ecosystem

| Abbreviation | Full Form |
|--------------|-----------|
| **JS** | JavaScript |
| **ES** | ECMAScript (ES6, ES2015, etc.) |
| **JSON** | JavaScript Object Notation |
| **DOM** | Document Object Model |
| **BOM** | Browser Object Model |
| **AJAX** | Asynchronous JavaScript And XML |
| **API** | Application Programming Interface |
| **REST** | Representational State Transfer |
| **CRUD** | Create, Read, Update, Delete |
| **SPA** | Single Page Application |
| **SSR** | Server Side Rendering |
| **CSR** | Client Side Rendering |

### Node.js & Runtime

| Abbreviation | Full Form |
|--------------|-----------|
| **Node.js** | Not an acronym (built on V8) |
| **NPM** | Node Package Manager |
| **NVM** | Node Version Manager |
| **REPL** | Read-Eval-Print Loop |
| **V8** | Google's JavaScript Engine |

### Frameworks & Libraries

| Abbreviation | Full Form |
|--------------|-----------|
| **React** | Not an acronym |
| **Vue** | Not an acronym |
| **Angular** | Not an acronym |
| **JSX** | JavaScript XML |
| **MVC** | Model-View-Controller |
| **MVVM** | Model-View-ViewModel |

### Development Tools

| Abbreviation | Full Form |
|--------------|-----------|
| **IDE** | Integrated Development Environment |
| **CLI** | Command Line Interface |
| **Git** | Not an acronym |
| **CI/CD** | Continuous Integration/Continuous Deployment |
| **Webpack** | Not an acronym |
| **Babel** | Not an acronym |
| **ESLint** | ECMAScript Lint |

### Web Technologies

| Abbreviation | Full Form |
|--------------|-----------|
| **HTML** | HyperText Markup Language |
| **CSS** | Cascading Style Sheets |
| **HTTP** | HyperText Transfer Protocol |
| **HTTPS** | HyperText Transfer Protocol Secure |
| **URL** | Uniform Resource Locator |
| **URI** | Uniform Resource Identifier |
| **CORS** | Cross-Origin Resource Sharing |
| **XSS** | Cross-Site Scripting |
| **CSRF** | Cross-Site Request Forgery |
| **JWT** | JSON Web Token |
| **OAuth** | Open Authorization |
| **WebSocket** | Not an acronym |
| **PWA** | Progressive Web App |
| **CDN** | Content Delivery Network |

### Testing

| Abbreviation | Full Form |
|--------------|-----------|
| **Jest** | Not an acronym |
| **TDD** | Test Driven Development |
| **BDD** | Behavior Driven Development |
| **E2E** | End-to-End (testing) |
| **Mocha** | Not an acronym |
| **Chai** | Not an acronym |

### Database & Backend

| Abbreviation | Full Form |
|--------------|-----------|
| **SQL** | Structured Query Language |
| **NoSQL** | Not Only SQL |
| **ORM** | Object-Relational Mapping |
| **MongoDB** | Not an acronym |
| **GraphQL** | Graph Query Language |

### Async & Performance

| Abbreviation | Full Form |
|--------------|-----------|
| **IIFE** | Immediately Invoked Function Expression |
| **HOF** | Higher Order Function |
| **Callback** | Not an acronym |
| **Promise** | Not an acronym |
| **Async/Await** | Not an acronym |

### Modern JS Concepts

| Concept | Description |
|---------|-------------|
| **Destructuring** | Not an acronym |
| **Spread Operator** | Not an acronym |
| **Rest Parameters** | Not an acronym |
| **Arrow Functions** | Not an acronym |
| **Template Literals** | Not an acronym |

---

## 🎯 How to Use This Guide

1. **Practice Daily**: Solve 10-15 questions per day
2. **Understand Concepts**: Don't just memorize outputs, understand WHY
3. **Write Code**: Type out each example and run it in browser console
4. **Track Progress**: Mark questions you've mastered
5. **Review Weak Areas**: Revisit topics where you struggle

---

## 📝 Contributing

Found an error or want to add more questions? Feel free to contribute!

---

## ⭐ Star this repo if it helped you!

**Good luck with your JavaScript interviews! 🚀**

---

**Total Questions: 150** | **Coverage: Basics → Medium → Advanced**
