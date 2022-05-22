### hey there <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">
<a href="https://www.instagram.com/abhisheknaiidu/">
  <img align="left" alt="Abhishek's Instagram" width="22px" src="https://raw.githubusercontent.com/hussainweb/hussainweb/main/icons/instagram.png" />
</a>
<a href="https://discord.gg/XTW52Kt">
  <img align="left" alt="Abhishek's Discord" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/discord.svg" />
</a>
<a href="https://twitter.com/abhisheknaiidu">
  <img align="left" alt="Abhishek Naidu | Twitter" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/twitter.svg" />
</a>
<a href="https://www.linkedin.com/in/abhisheknaiidu/">
  <img align="left" alt="Abhishek's LinkedIN" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/linkedin.svg" />
</a>

![](https://visitor-badge.glitch.me/badge?page_id=abhisheknaiidu.abhisheknaiidu)

<br />

hi, i'm [Abhishek Naidu](https://abhishknads.me/), a passionate self-taught full stack web developer and a freelance software engineer from india. my passion for software lies with dreaming up ideas and making them come true with elegant interfaces. i take great care in the experience, architecture, and code quality of the things I build.

i am also an open-source enthusiast and maintainer. i learned a lot from the open-source community and i love how collaboration and knowledge sharing happened through open-source.
  
<iframe width="620" height="345" src="https://www.youtube.com/embed/tgbNymZ7vqY">
</iframe>

- 💼 any freelance work? do reach, [email](mailto:abhishek.naidu@cred.club) :)
- 💬 ask me about anything, i am happy to help;


📊 **this week i spent my time on:**
<!--START_SECTION:waka-->

```text
TypeScript   3 hrs 39 mins   ███████▒░░░░░░░░░░░░░░░░░   29.79 %
MDX          3 hrs 22 mins   ███████░░░░░░░░░░░░░░░░░░   27.41 %
JavaScript   2 hrs 48 mins   █████▓░░░░░░░░░░░░░░░░░░░   22.91 %
SCSS         1 hr 6 mins     ██▒░░░░░░░░░░░░░░░░░░░░░░   09.03 %
HTML         36 mins         █▒░░░░░░░░░░░░░░░░░░░░░░░   04.92 %
JSON         22 mins         ▓░░░░░░░░░░░░░░░░░░░░░░░░   03.04 %
```

<!--END_SECTION:waka-->

if you like what i do, maybe consider buying me a coffee/tea 🥺👉👈

<a href="https://www.buymeacoffee.com/abhisheknaiidu" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-red.png" alt="Buy Me A Coffee" width="150" ></a>

🚧 **my todoist stats:**
<!-- TODO-IST:START -->
🏆  7,995 Karma Points           
🌸  Completed 0 tasks today           
✅  Completed 673 tasks so far           
⏳  Longest streak is 10 days
<!-- TODO-IST:END -->


📈 my github stats

<p align="center"> <img src="https://github-readme-stats.vercel.app/api?username=abhisheknaiidu&show_icons=true&theme=gotham" alt="abhisheknaiidu" />





# Intermediate Javascript

[https://github.com/sohamkamani/javascript-design-patterns-for-humans](https://github.com/sohamkamani/javascript-design-patterns-for-humans)

# **First-Class Functions**

In JavaScript, functions are *first-class* functions. This means that you can do with a *function* just about anything that you can do with other elements, such as numbers, strings, objects, arrays,  etc. JavaScript functions can:

1. Be stored in variables
2. Be returned from a function.
3. Be passed as arguments into another function.

Note that while we can, say, treat a function as an object, a key difference between a function and an object is that functions can be called (i.e., invoked with `()`), while regular objects *cannot*.

### **Functions Can Return Functions**

Recall that a function must always return a value. Whether the value is explicitly specified in a `return` statement (e.g., returning a string, boolean, array, etc.), or the function implicitly returns `undefined` (e.g., a function that simply logs something to the console), a function will always return just *one* value.

Since we know that functions are first-class functions, we can treat a *function* as a value and just as easily return a *function* from another function! A function that returns another function is known as **higher-order function**. Consider this example:

```jsx
function alertThenReturn() {
  alert('Message 1!');

  return function () {
    alert('Message 2!');
  };
}
```

# **Callback Functions**

A function that takes other functions as arguments (and/or *returns* a function, as we learned in the previous section) is known as a **higher-order function.** A function that is passed as an argument into another function is called a **callback** function.


https://user-images.githubusercontent.com/58986949/115314310-805b2780-a1a7-11eb-8558-648a367ea231.mp4


# Scope

> If you know JS, you learned about *block* scope vs. *function* scope. These determine where a variable can be seen in some code. Computer scientists call this **lexical scope**.
> 

However, there also exists *another* kind of scope called **runtime scope**. When a function is run, it creates a new runtime scope. This scope represents the *context* of the function, or more specifically, the set of variables available for the function to use.

A function's runtime scope describes the variables available for use inside a given function. The code inside a function has access to:

1. The function's arguments.
2. Local variables declared within the function.
3. Variables from its parent function's scope.
4. Global variables.

### **JavaScript is Function-Scoped**

You may be wondering why scope is so heavily associated with *functions* in JavaScript. Especially if you've had past experience in another programming language, this might seem a bit unusual (e.g., *blocks* in Ruby have their own scope)!

This is all because variables in JavaScript are traditionally defined in the scope of a *function*, rather than in the scope of a *block*. Since entering a function will change scope, any variables defined inside that function are *not* available outside of that function. On the other hand, if there are any variables defined inside a *block* (e.g., within an if statement), those variables *are* available outside of that block.

### **Scope Chain**

Whenever your code attempts to access a variable during a function call, the JavaScript interpreter will always start off by looking within its own local variables. If the variable isn't found, the search will continue looking up what is called the **scope chain**.

![Screenshot 2022-04-03 at 10.18.38 AM.png](Screenshot_2022-04-03_at_10.18.38_AM.png)

### **Variable Shadowing**

What happens when you create a variable with the *same name* as another variable somewhere in the scope chain?

JavaScript won't throw an error or otherwise prevent you from creating that extra variable. In fact, the variable with local scope will just temporarily "shadow" the variable in the outer scope. This is called **variable shadowing**. Consider the following example:

```jsx
const symbol = '¥';

function displayPrice(price) {
  const symbol = '$';
  console.log(symbol + price);
}

displayPrice('80');
// '$80'
```

# Closure

A **closure** refers to the combination of a function and the lexical environment in which that function was declared. Every time a function is defined, closure is created for that function. This is especially powerful in situations where a function is defined within another function, allowing the nested function to access variables outside of it. Functions also keep a link to its parent's scope even if the *parent* has returned. This prevents data in its parents from being garbage collected.

### **Creating a Closure**

Every time a function is defined, closure is created for that function. Strictly speaking, then, *every* function has closure! This is because functions close over at least one other context along the scope chain: the global scope. However, the capabilities of closures really shine when working with a nested function (i.e., a function defined within another function).

Recall that a nested function has access to variables outside of it. From what we have learned about the scope chain, this includes the variables from the outer, enclosing function itself (i.e., the parent function)! These nested functions close over (i.e., *capture*) variables that aren't passed in as arguments nor defined locally, otherwise known as **free variables**

In the below code example, after function declaration, still invoking result gives 1 as output.

As function logger forms a closure -

![Screenshot 2022-04-03 at 10.27.07 AM.png](Screenshot_2022-04-03_at_10.27.07_AM.png)

Another Example - 

![Screenshot 2022-04-03 at 10.28.50 AM.png](Screenshot_2022-04-03_at_10.28.50_AM.png)

As we can see below count is not available, so closure helps to create private state too

![Screenshot 2022-04-03 at 10.29.03 AM.png](Screenshot_2022-04-03_at_10.29.03_AM.png)

### **Garbage Collection**

JavaScript manages memory with automatic **garbage collection**. This means that when data is no longer referable (i.e., there are no remaining references to that data available for executable code), it is "garbage collected" and will be destroyed at some later point in time. This frees up the resources (i.e., computer memory) that the data had once consumed, making those resources available for re-use.

Let's look at garbage collection in the context of *closures*. We know that the variables of a parent function are accessible to the nested, inner function. If the nested function captures and uses its parent's variables (or variables along the scope chain, such as its parent's parent's variables), those variables will stay in memory as long as the functions that utilize them can still be referenced.

As such, referenceable variables in JavaScript are *not* garbage collected! Let's quickly look back at the `myCounter` function -

```jsx
function myCounter() {
  let count = 0;
 
  return function () {
    count += 1;
    return count;
  };
}
```

# **Immediately-Invoked Function Expressions (IIFE)**

### **Function Declarations vs. Function Expressions**

Before we jump into **immediately-invoked function expressions** (IIFE), let's make sure we're on the same page regarding the differences between function *declarations* and function *expressions*.

A function *declaration* defines a function and does not require a variable to be assigned to it. It simply declares a function, and doesn't itself return a value. Here's an example:

```jsx
function returnHello() {
  return 'Hello!';
}
```

On the other hand, a function *expression* does return a value. Function expressions can be anonymous or named, and are part of another expression's syntax. They're commonly assigned to variables, as well. Here's the same function as a function *expression*:

```jsx
// anonymous
const myFunction = function () {
  return 'Hello!';
};

// named
const myFunction = function returnHello() {
  return 'Hello!';
};
```

### **Immediately-Invoked Function Expressions: Structure and Syntax**

An immediately-invoked function expression, or IIFE (pronounced *iffy*
), is a function that is called immediately after it is defined. Check out the following example:

```jsx
(function sayHi(){
    alert('Hi there!');
  }
)();

// alerts 'Hi there!'
```

### **IIFE's and Private Scope**

One of the primary uses for IIFE's is to create *private scope*
 (i.e., private state). Recall that variables in JavaScript are traditionally scoped to a function. Knowing this, we can leverage the behavior of closures to protect variables or methods from being accessed! Consider the following example of a simple closure within an IIFE, referenced by `myFunction`:

```jsx
const myFunction = (
  function () {
    const hi = 'Hi!';
    return function () {
      console.log(hi);
    }
  }
)();
```

![Screenshot 2022-04-03 at 7.41.17 AM.png](Screenshot_2022-04-03_at_7.41.17_AM.png)

### **IIFE's, Private Scope, and Event Handling**

Let's check out another example of an immediately-invoked function expression -- this time in the context of handling an event. Say that we want to create a button on a page that alerts the user on every other click. One way to begin doing this would be to keep track of the number of times that the button was clicked. But how should we maintain this data?

We *could* keep track of the count with a variable that we declare in the global scope (this would make sense if other parts of the application need access to the count data). However, an even better approach would be to enclose this data *in event handler itself*!

For one, this approach prevents us from polluting the global with extra variables (and potentially variable name collisions). What's more: if we use an IIFE, we can leverage a *closure* to protect the `count` variable from being accessed externally! This prevents any accidental mutations or unwanted side-effects from inadvertently altering the count.

```jsx
// button.js

button.addEventListener('click', (function() {
  let count = 0;

  return function() {
    count += 1;

    if (count === 2) {
      alert('This alert appears every other press!');
      count = 0;
    }
  };
})());
```

Quite a bit is going on in the IIFE, so let's break it down!

First, we declare a local variable, `count`, which is initially set to `0`. We then return a function from *that* function. The returned function increments `count`, but alerts the user and resets the count back to `0` if the count reaches `2`.

What is important to note is that the returned function *closes over* the `count` variable. That is, because a function maintains a reference to its parent's scope, `count` is available for the returned function to use! As a result, we immediately invoke a function that returns that function. And since the returned function has access to the internal variable, `count`, a **private scope** is created -- effectively protecting the data!

### **Benefits of Immediately-Invoked Function Expressions**

We've seen how using an immediately-invoked function expression creates a private scope that protects variables or methods from being accessed. IIFE's ultimately use the returned functions to access private data within the closure. This works out very well: while these returned functions are publicly-accessible, they still maintain privacy for the variables defined within them!

Another great opportunity to use an IFFE is when you want to execute some code without creating extra global variables. However, note that an IIFE is only intended to be invoked once, to create a unique execution context. If you have some code that is expected to be re-used (e.g., a function meant to be executed more than once in the application), declaring the function and then invoking it might be a better option.

All in all, if you simply have a one-time task (e.g., initializing an application), an IIFE is a great way to get something done without polluting your the global environment with extra variables. Cleaning up the global namespace decreases the chance of collisions with duplicate variable names, after all.

### **Summary**

An **immediately-invoked function expression** (IIFE) is a function that is called immediately after it is defined. Utilizing an IIFE alongside closures allows for a **private scope**, which maintains privacy for variables defined within them. And since less variables are created, an IIFE will help to minimize pollution of the global environment, hindering the chances of variable name collisions.

# Classes

Previously, we have created objects using the object literal notation. Likewise, we can even write functions that *return* objects. There is yet another way for us to create objects, and it is the foundation of object-oriented JavaScript: the **constructor function**.

To instantiate (i.e., *create*) a new object, we use the `new` operator to invoke the function:

```jsx
new SoftwareDeveloper();
```

The first thing to note above is the use of the `new` keyword. Second, note that the name of the constructor function, `SoftwareDeveloper()`, is written with the first letter capitalized to *visually*
 distinguish it from a regular function.

**Constructor Functions: Structure and Syntax**

This is what the internals of a constructor function looks like:

```jsx
function SoftwareDeveloper() {
  this.favoriteLanguage = 'JavaScript';
}
```

**Creating a New Object**

```jsx
let developer = new SoftwareDeveloper();
```

![Screenshot 2022-04-03 at 6.26.44 PM.png](Screenshot_2022-04-03_at_6.26.44_PM.png)

**Creating Multiple Objects**

```jsx
let engineer = new SoftwareDeveloper();
let programmer = new SoftwareDeveloper();

console.log(engineer);
// SoftwareDeveloper { favoriteLanguage: 'JavaScript' }

console.log(programmer);
// SoftwareDeveloper { favoriteLanguage: 'JavaScript' }
```

**Constructor Functions Can Have Parameters**

```jsx
function SoftwareDeveloper(name) {
  this.favoriteLanguage = 'JavaScript';
  this.name = name;
}
let instructor = new SoftwareDeveloper('Andrew');

console.log(instructor);
// SoftwareDeveloper { favoriteLanguage: 'JavaScript', name: 'Andrew' }
```




📢 ***⚠️ Omitting the `new` Operator ⚠️**
What's going on? Without using the `new` operator, no object was created. The function was invoked just like any other regular function. Since the function doesn't return anything (except `undefined`, which all functions return by default), the `coder` variable ended up being assigned to `undefined`.*




```jsx
functionSoftwareDeveloper(name) {
this.favoriteLanguage = 'JavaScript';
this.name = name;
}

let coder = SoftwareDeveloper('David');

console.log(coder);
```

### **Summary**

JavaScript's class system is built directly on using functions and objects. Calling (i.e., invoking) a **constructor function** with the `new` operator instantiates a new object. The same constructor function can be used to create different objects.

# **The `this` Keyword**

As it turns out, when invoking a constructor function with the `new` operator, `this` gets set to the *newly-created object*! 

### ****When is `this` Assigned?**

A common misconception is that `this` refers to the object *where it is defined*. This is not the case!

The value of `this` is actually not assigned to anything until an object calls the method where `this` is used. In other words, the value assigned to `this` is based on *the object that invokes the method where `this` is defined*.

### ****What Does `this` Get Set To?**

At this point, we've seen `this` in many different contexts, such as within a method, or referenced by a constructor function. Let's now organize our thoughts and bring it all together!

There are four ways to call functions, and each way sets `this` differently.

First, calling a constructor function with the `new` keyword sets `this` to a newly-created object. Recall that creating an instance of `Cat` earlier had set `this` to the new `bailey` object.

```jsx
function Cat(name) {
 this.name = name;
 this.sayName = function () {
   console.log(`Meow! My name is ${this.name}`);
 };
}

const bailey = new Cat('Bailey');
```

On the other hand, calling a function that belongs to an object (i.e., a *method*) sets `this`
 to the object itself. Recall that earlier, the `dog` object's `barkTwice()` method was able to access properties of `dog` itself.

```jsx
const dog = {
  bark: function () {
    console.log('Woof!');
  },
  barkTwice: function () {
    this.bark();
    this.bark();
  }
};
```

Third, calling a function on its own (i.e., simply invoking a regular function) will set `this`
 to `window` , which is the global object if the host environment is the browser.

```jsx
function funFunction() {
  return this;
}

funFunction();
// (returns the global object, `window`)
```

The fourth way to call functions allows us to set `this` ourselves! Don't worry about this approach for now; we'll take a deep dive in the very next section.

![Screenshot 2022-04-03 at 6.47.08 PM.png](Screenshot_2022-04-03_at_6.47.08_PM.png)

### **Summary**

Functions, objects, and `this` are all interconnected. When invoking constructor functions with the `new` operator, a `this` variable is set to the newly-created object. When invoking a method on an object, `this` is set to that object itself. And when invoking a function in a browser environment, `this` is set to `window`, otherwise known as the global object.

# **Setting Our Own `this`**

### **More Ways to Invoke Functions**

We've seen various ways to invoke functions, each with their own implications regarding the value of `this`. There are yet two more ways to invoke a function: either using the `call()` or the `apply()` methods.

### ****call()****

`call()`  is a method directly invoked onto a function. We first pass into it a single value to set as the value of `this`; then we pass in any of the receiving function's arguments one-by-one, separated by commas.

```jsx
function multiply(n1, n2) {
  return n1 * n2;
}
multiply(3, 4);

// 12
multiply.call(window, 3, 4);

// 12
```

Along with invoking regular functions, how do we go upon invoking *functions attached to objects*
 (i.e., methods)? This is where the power of `call()` really shines. Using `call()` to invoke a method allows us to "borrow" a method from one object -- then use it for *another* object! Check out the following object, `mockingbird`:

```jsx
const mockingbird = {
  title: 'To Kill a Mockingbird',
  describe: function () {
    console.log(`${this.title} is a classic novel`);
  }
};
mockingbird.describe();

// 'To Kill a Mockingbird is a classic novel'
const pride = {
  title: 'Pride and Prejudice'
};

mockingbird.describe.call(pride);
// 'Pride and Prejudice is a classic novel'
```

### ****apply()****

Just like `call()`, the `apply()`method is called on a function to not only invoke that function, but also to associate with it a specific value of `this`. However, rather than passing arguments one-by-one, separated by commas -- `apply()` takes the function's arguments in an *array.*

```jsx
function multiply(n1, n2) {
  return n1 * n2;
}
multiply.apply(window, [3, 4]);

// 12
```

### **Choosing One Method Over the Other**

Both `call()` and `apply()` invoke a function in the scope of the first argument passed in them (i.e., the object to be the value of `this`). So when would you choose `call()` over `apply()`, or vice versa?

`call()` may be limited if you don't know ahead of time the number of arguments that the function needs. In this case, `apply()` would be a better option, since it simply takes an array of arguments, then unpacks them to pass along to the function. Keep in mind that the unpacking comes at a minor performance cost, but it shouldn't be much of an issue.

### Callbacks and `this`

The value of `this` has some potential scope issues when *callback functions* are involved, and things can get a bit tricky. Let's check it out below and see age doesn’t chaged-

![Screenshot 2022-04-05 at 10.28.39 AM.png](Screenshot_2022-04-05_at_10.28.39_AM.png)

### ****Saving `this` with an Anonymous Closure**

Let's recap the issue at hand. Here's the `invokeTwice()` function from the previous video, as well as the `dog`object:

Recall that simply invoking a normal function will set the value of `this` to the global object (i.e., `window`). This is an issue, because we want `this` to be the `dog` object!

So how can we make sure that `this` is preserved?

One way to resolve this issue is to use an **anonymous closure** to close over the `dog` object:

```jsx
function invokeTwice(cb) {
   cb();
   cb();
}

const dog = {
  age: 5,
  growOneYear: function () {
    this.age += 1;
  }
};

invokeTwice(function () { 
  dog.growOneYear(); 
});

dog.age;
// 7
```

### ****Saving `this` with bind()**

Similar to `call()` and `apply()`, the `bind()`method allows us to directly define a value for `this`. `bind()` is a method that is also called _on_ a function, but unlike `call()`
 or `apply()`, which both invoke the function right away -- `bind()`*returns* a new function that, when called, has `this`set to the value we give it.

![Screenshot 2022-04-05 at 10.23.13 AM.png](Screenshot_2022-04-05_at_10.23.13_AM.png)

### ****Summary****

JavaScript provides three methods that allow us to set the value of `this` for a given function:

- `call()` invokes the function and has arguments passed in individually, separated by commas.
- `apply()` is similar to `call()`; it invokes the function just the same, but arguments are passed in as an array.
- `bind()` returns a new function with `this` bound to a specific object, allowing us to call it as a regular function.

# **Prototypal Inheritance**

### ****Adding Methods to the Prototype****

```jsx
function Cat(name) {
 this.lives = 9;
 this.name = name;

 this.sayName = function () {
   console.log(`Meow! My name is ${this.name}`);
 };
}
```

This way, a `sayName` method gets added to all `Cat` objects by saving a function to the `sayName` attribute of newly-created `Cat` objects.

This works just fine, but what if we want to instantiate more and more `Cat` objects with this constructor? You'll create a new function every single time for that `Cat` object's `sayName`! What's more: if you ever want to make changes to the method, you'll have to update all objects *individually*. In this situation, it makes sense to have all objects created by the same `Cat` constructor function just *share* a single `sayName` method.

To save memory and keep things DRY, we can add methods to the constructor function's `prototype` property. The prototype is just an object, and all objects created by a constructor function keep a reference to the prototype. Those objects can even use the `prototype`'s properties *as their own*!

JavaScript leverages this secret link -- between an object and its prototype -- to implement inheritance.

### ****Finding Properties and Methods on the Prototype Chain****

1. First, the JavaScript engine will look at the object's *own* properties. This means that any properties and methods defined directly in the object itself will take precedence over any properties and methods elsewhere if their names are the same (similar to variable shadowing in the *scope chain*).
2. If it doesn't find the property in question, it will then search the object's constructor's prototype for a match.
3. If the property doesn't exist in the prototype, the JavaScript engine will continue looking up the chain.
4. At the very end of the chain is the `Object()` object, or the top-level parent. If the property *still* cannot be found, the property is undefined.

Previously, we simply defined methods directly in a constructor function itself. Let's see how things look if we defined methods in the constructor's `prototype` instead!

![Screenshot 2022-04-07 at 3.04.35 PM.png](Screenshot_2022-04-07_at_3.04.35_PM.png)

****💡 Replacing the `prototype` Object 💡**

```jsx
function Hamster() {
  this.hasFur = true;
}

let waffle = new Hamster();
let pancake = new Hamster();
```

First, note that even after we make the new objects, `waffle`and `pancake`, we can still add properties to `Hamster`'s prototype and it will still be able to access those new properties.

```jsx
Hamster.prototype.eat = function () {
  console.log('Chomp chomp chomp!');
};

waffle.eat();
// 'Chomp chomp chomp!'

pancake.eat();
// 'Chomp chomp chomp!'
```

Now, let's replace `Hamster`'s `prototype`object with something else entirely:

```jsx
Hamster.prototype = {
  isHungry: false,
  color: 'brown'
};
```

The previous objects don't have access to the updated prototype's properties; they just retain their secret link to the old prototype:

```jsx
console.log(waffle.color);
// undefined

waffle.eat();
// 'Chomp chomp chomp!'

console.log(pancake.isHungry);
// undefined
```

As it turns out, any new `Hamster` objects created moving forward will use the updated prototype:

```jsx
const muffin = new Hamster();

muffin.eat();
// TypeError: muffin.eat is not a function

console.log(muffin.isHungry);
// false

console.log(muffin.color);
// 'brown'
```

### ****hasOwnProperty()****

`hasOwnProperty()`allows you to find the origin of a particular property. Upon passing in a string of the property name you're looking for, the method will return a boolean indicating whether or not the property belongs to the object itself (i.e., that property was *not* inherited).

```jsx
function Phone() {
  this.operatingSystem = 'Android';
}

Phone.prototype.screenSize = 6;
const myPhone = new Phone();

const own = myPhone.hasOwnProperty('operatingSystem');

console.log(own);
// true
```

### ****isPrototypeOf()****

Objects also have access to the `isPrototypeOf()` method, which checks whether or not an object exists in another object's prototype chain. Using this method, you can confirm if a particular object serves as the prototype of another object. Check out the following `rodent` object:

```jsx
const rodent = {
  favoriteFood: 'cheese',
  hasTail: true
};

//Let's now build a Mouse() constructor function, and assign 
//its prototype to rodent:

function Mouse() {
  this.favoriteFood = 'cheese';
}

Mouse.prototype = rodent;

//If we create a new Mouse object, its prototype should be the rodent
// object. Let's confirm:

const ralph = new Mouse();

const result = rodent.isPrototypeOf(ralph);

console.log(result);
```

### ****Object.getPrototypeOf()****

`isPrototypeOf()` works well, but keep in mind that in order to use it, you must *have* that prototype object at hand in the first place! What if you're not sure what a certain object's prototype is? `Object.getPrototypeOf()` can help with just that!

Using the previous example, let's store the return value of `Object.getPrototypeOf()` in a variable, `myPrototype`, then check what it is:

```jsx
const myPrototype = Object.getPrototypeOf(ralph);

console.log(myPrototype);
// { favoriteFood: 'cheese', hasTail: true }
```

### ****The `constructor` Property**

Each time an object is created, a special property is assigned to it under the hood: `constructor`
. Accessing an object's `constructor` property returns a reference to the constructor function that created that object in the first place!

```jsx
function Longboard() {
  this.material = 'bamboo';
}

const board = new Longboard();
console.log(board.constructor);

// function Longboard() {
//   this.material = 'bamboo';
// }

//Excellent! Keep in mind that if an object was created using literal 
//notation, its constructor is the built-in Object() constructor function!

const rodent = {
  favoriteFood: 'cheese',
  hasTail: true
};

console.log(rodent.constructor);
// function Object() { [native code] }
```

# **Prototypal Inheritance: Subclasses**

Inheritance in JavaScript is all about setting up the prototype chain. This allows us to **subclass**, that is, create a "child" object that inherits most or all of a "parent" object's properties and methods. We can then implement any of the child object's unique properties and methods separately, while still retaining data and functionality from its parent.

An object (instance) is secretly linked to its constructor function's prototype object through that instance's `__proto__` property. **You should never use the `__proto__` property in any code you write.** Using `__proto__` in any code, or even inheriting just the prototype directly, leads to some unwanted side effects.

To efficiently manage inheritance in JavaScript, an effective approach is to avoid mutating the prototype completely. `Object.create()` allows us to do just that, taking in a parent object and returning a *new* object with its `__proto__` property set to that parent object.

### ****Subclasses****

One of the benefits of implementing inheritance is that it allows you to *reuse existing code*
. By establishing inheritance, we can **subclass**, that is, have a "child" object take on most or all of a "parent" object's properties while retaining unique properties of its own.

### ****Inheritance Via Prototypes****

As you know, an object's constructor function's prototype is first place searched when the JavaScript engine tries to access a property that doesn't exist in the object itself. Consider the following `bear` object with two properties, `claws` and `diet`:

```jsx
const bear = {
  claws: true,
  diet: 'carnivore'
};

//We'll assign the following PolarBear() constructor function's 
//prototype property to bear:

function PolarBear() { 
  // ...
}

PolarBear.prototype = bear;

//Let's now call the PolarBear() constructor to create a new object, 
//then give it two properties:

const snowball = new PolarBear();

snowball.color = 'white';
snowball.favoriteDrink = 'cola';

//Note that snowball has just two properties of its own: color and 
//favoriteDrink. However, snowball also has access to properties that
// don't exist inside it: claws and diet:

console.log(snowball.claws);
// true

console.log(snowball.diet);
// 'carnivore'
```

### ****Object.create()****

At this point, we've reached a few roadblocks when it comes to inheritance. First, even though `__proto__` can access the prototype of the object it is called on, using it in any code you write is not good practice.

What's more: we also shouldn't inherit *only* the prototype; this doesn't set up the prototype chain, and any changes that we made to a child object will also be reflected in a parent object.

So how should we move forward?

There's actually a way for us to set up the prototype of an object ourselves: using `Object.create()`. And best of all, this approach lets us manage inheritance *without* altering the prototype!

`Object.create()` takes in a single object as an argument, and returns a new object with its `__proto__` property set to what argument is passed into it. From that point, you simply set the returned object to be the prototype of the child object's constructor function. Let's check out an example!

First, let's say we have a `mammal` object with two properties: `vertebrate` and `earBones`:

```jsx
const mammal = {
  vertebrate: true,
  earBones: 3
};

const rabbit = Object.create(mammal);

console.log(rabbit);

// {}

//However, rabbit should now be secretly linked to mammal. 
//That is, its __proto__ property should point to mammal:

console.log(rabbit.__proto__ === mammal);

// true

//Great! This means that now, rabbit extends mammal (i.e., rabbit inherits 
//from mammal). As a result, rabbit can access mammal's properties as if 
//it were its own!

console.log(rabbit.vertebrate);
// true

console.log(rabbit.earBones);
// 3
```

# **Mixins / Extending Object Functionality with Mixins**

### ****An Object is Prototype-linked to a Single Object****

![Screenshot 2022-04-07 at 4.47.37 PM.png](Screenshot_2022-04-07_at_4.47.37_PM.png)

### ****Mixins****

If a JavaScript object can only be prototype-linked to a single object, how can we go about extending properties and methods from *multiple* different sources? A **mixin** allows us to just that!

A mixin is a technique that takes the properties and methods from one object and copies them over to another object. In other words: a mixin is an technique that provides some useful functionality, but is not meant to be added to the prototype chain.

### ****Object.assign()****

The simplest way to implement the mixin pattern is to use `Object.assign()`
. `Object.assign()`is a method that copies an object's own (non-inherited) properties from one or more *source* objects into a *target* object, then returns the updated target object. In other words, `Object.assign()`adds to the target object by *merging* in the source object(s).

```jsx
let target = {};

let source = { number: 7 };

Object.assign(target, source);

console.log(target);
// { number: 7 }
```

****Multiple Source Objects****

```jsx
const duck = {
  hasBill: true
};
const beaver = {
  hasTail: true
};
const otter = {
  hasFur: true,
  feet: 'webbed'
};

const platypus = Object.assign({}, duck, beaver, otter);

console.log(platypus);
// { hasBill: true, hasTail: true, hasFur: true, feet: 'webbed' }
```

# **Functional Mixins**

### ****Factory Functions****

Again, note that we used the `new` keyword each time to create a new object. Let's now shift gears a bit to **factory functions** which produce object instances *without* the use of the `new` operator!

Factory function is a function that returns an object, but isn't itself a class or constructor. As such, we invoke a factory function as a normal function without using the `new` operator. Using a factory function, we can easily create object instances without the complexity of classes and constructors!

Check out the following `Basketball()` factory function:

```jsx
function Basketball(color) {
  return {
    color: color,
    numDots: 35000
  };
}
```

What's important to note here is that `Basketball()`returns an object directly. This is different from a constructor function which returns its object automatically.

```jsx
const orangeBasketball = Basketball('orange');

console.log(orangeBasketball);
// { color: 'orange', numDots: 35000 }
```

![Screenshot 2022-04-07 at 5.01.20 PM.png](Screenshot_2022-04-07_at_5.01.20_PM.png)

### ****Functional Mixins****

In the previous section, we used **mixins** to add features into a composite object. We also just leveraged **factory functions** to create objects without using the `new` operator or messing with prototypal inheritance. Let's combine what we've learned from mixins and factory functions and take things a step further with **functional mixins**!

A functional mixin is a composable factory function that receives a _mixin_as an argument, copies properties and methods from that mixin, and returns a new object. Check out the following example: `CoffeeMaker()`:

```jsx
function CoffeeMaker(object) {
  let needsRefill = false;

  return Object.assign({}, object, {
    pourAll: function () {
      needsRefill = true;
    },
    isEmpty: function () {
      return needsRefill;
    }
  });
}

const mixedCoffeeMaker = CoffeeMaker({ style: 'percolator' });

//The returned mixedCoffeeMaker object now looks like:
{
  style: 'percolator',
  pourAll: function () {
    needsRefill = true;
  },
  isEmpty: function () {
    return needsRefill;
  }
}
```

### **Summary**

A factory function creates objects. It is invoked as normal function, *not* with the `new` operator. Functional mixins take things a bit further by accepting a mixin as an argument, copies properties and methods from the mixin, and returns a new object.

# **The Module Pattern**

Since JavaScript doesn't have private variables, properties, or methods built-in, we can leverage the Module Pattern to enforce such privacy. At its core, the Module Pattern leverages scope, closures, and (commonly) IIFE's to not only hide data from external access, but to also provide a public interface for such data.

### ****The Module Pattern: Recap****

Before moving on to the next section, let's make sure we're on the same page regarding the Module Pattern. We'll be improving upon it in the very next section! Consider the following:

```jsx
let diana = (function () {
  let secretIdentity = 'Diana Prince';

  return {
    introduce: function () {
      console.log(`Hi! I am ${secretIdentity}`);
    }
  };
})();
```

Recall that one of the key ingredients here is the IIFE! Not only does it prevent pollution of the global scope (which hinders the chance of variable name collisions) -- the IIFE helps prevent access to the `secretIdentity`variable.

```jsx
console.log(diana.secretIdentity);

// undefined

//And because the returned object's introduce() method retains access to its
// parent function's scope, we are given a public interface to interact with 
//secretIdentity:

diana.introduce();

// 'Hi! I am Diana Prince'
```

# ****The Revealing Module Pattern****

The underlying philosophy of the Revealing Module Pattern is that, while we still maintain encapsulation (as in the Module Pattern), we also *reveal* certain properties (and methods). The key ingredients to the Revealing Module Pattern are:

1. An IIFE (wrapper)
2. The module content (variables, methods, objects, etc.)
3. A returned object literal

```jsx
let person = (function () {
  let privateAge = 0;
  let privateName = 'Andrew';

  function privateAgeOneYear() {
    privateAge += 1;
    console.log(`One year has passed! Current age is ${privateAge}`);
  }

  function displayName() {
    console.log(`Name: ${privateName}`);
  }

  function ageOneYear() {
    privateAgeOneYear();
  }

  return {
    name: displayName,
    age: ageOneYear
  };
})();
```

In the above snippet, the IIFE has some private data: `privateAge`, `privateName`, and `privateAgeOneYear()`. The returned object is stored in `person`and provides a public interface through which we can access this data!

### **Benefits of the Revealing Module Pattern**

When writing your modules, there are a few key advantages of using the Revealing Module Pattern. For one, there is clarity at the end of the module (i.e., the `return` statement) as to which variables or methods may be accessed publicly. Modules may grow large, and this eases readability for other developers who read your code.

Along with clear intent of public or private data, the Revealing Module Pattern lends itself to consistent syntax as well. In contrast, the normal Module Pattern may contain variables and functions spread throughout the entire function body.

While you can't go wrong with either approach to create private properties in your code, be sure to take the time and choose which makes the most sense for your project!

### **Summary**

The Revealing Module Pattern is a slight variation on the Module Pattern. IIFE's, local variables/functions, and a returned object literal with revealed data make up the structure and syntax of the Revealing Module Pattern. While it still maintains encapsulation of data, certain variables and functions are returned in an object literal.

In the next section, we'll take a look at object-oriented JavaScript in the real-world, especially in popular library code and frameworks.
