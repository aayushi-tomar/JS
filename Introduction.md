What is JavaScript?

JavaScript is a cross-platform, object-oriented scripting language used to make webpages interactive (e.g., having complex animations, clickable buttons, popup menus, etc.). There are also more advanced server side versions of JavaScript such as Node.js, which allow you to add more functionality to a website than downloading files (such as realtime collaboration between multiple computers)

JavaScript contains a standard library of objects, such as Array, Map, and Math, and a core set of language elements such as operators, control structures, and statements.

Core JavaScript can be extended for a variety of purposes by supplementing it with additional objects; for example:
Client-side JavaScript extends the core language by supplying objects to control a browser and its Document Object Model (DOM). For example, client-side extensions allow an application to place elements on an HTML form and respond to user events such as mouse clicks, form input, and page navigation.

Server-side JavaScript extends the core language by supplying objects relevant to running JavaScript on a server. For example, server-side extensions allow an application to communicate with a database, provide continuity of information from one invocation to another of the application, or perform file manipulations on a server.

JavaScript and Java:-
JavaScript and Java are similar in some ways but fundamentally different in some others. The JavaScript language resembles Java but does not have Java's static typing and strong type checking. JavaScript follows most Java expression syntax, naming conventions and basic control-flow constructs which was the reason why it was renamed from LiveScript to JavaScript.

In contrast to Java's compile-time system of classes built by declarations, JavaScript supports a runtime system based on a small number of data types representing numeric, Boolean, and string values.
 JavaScript has a prototype-based object model instead of the more common class-based object model

 JavaScript is a very free-form language compared to Java. You do not have to declare all variables, classes, and methods. You do not have to be concerned with whether methods are public, private, or protected, and you do not have to implement interfaces. Variables, parameters, and function return types are not explicitly typed.

 Java is a class-based programming language designed for fast execution and type safety. Type safety means, for instance, that you can't cast a Java integer into an object reference or access private memory by corrupting the Java bytecode.Java's class-based model means that programs consist exclusively of classes and their methods.

 JavaScript	Java:-
Object-oriented. No distinction between types of objects. Inheritance is through the prototype mechanism, and properties and methods can be added to any object dynamically.	Class-based. Objects are divided into classes and instances with all inheritance through the class hierarchy. Classes and instances cannot have properties or methods added dynamically.
Variable data types are not declared (dynamic typing, loosely typed).	Variable data types must be declared (static typing, strongly typed).
Cannot automatically write to hard disk.	Can automatically write to hard disk.

Getting started with JavaScript:-
A very useful tool for exploring JavaScript is the JavaScript Console (sometimes called the Web Console, or just the console): this is a tool which enables you to enter JavaScript and run it in the current page.
console.log(eval("3 + 5"));

(function () {
  "use strict";
  /* Start of your code */
  function greetMe(yourName) {
    alert(`Hello ${yourName}`);
  }

  greetMe("World");
  /* End of your code */
})();

Grammar and types:-
Basics:-
JavaScript is case-sensitive and uses the Unicode character set. For example, the word Früh (which means "early" in German) could be used as a variable name.
const Früh = "foobar";
But, the variable früh is not the same as Früh because JavaScript is case sensitive.
In JavaScript, instructions are called statements and are separated by semicolons (;).

Declarations:-
JavaScript has three kinds of variable declarations.

var
Declares a variable, optionally initializing it to a value.

let
Declares a block-scoped, local variable, optionally initializing it to a value.

const
Declares a block-scoped, read-only named constant.

Variables
You use variables as symbolic names for values in your application. The names of variables, called identifiers, conform to certain rules.
A JavaScript identifier usually starts with a letter, underscore (_), or dollar sign ($). Subsequent characters can also be digits (0 – 9). Because JavaScript is case sensitive, letters include the characters A through Z (uppercase) as well as a through z (lowercase)

Some examples of legal names are Number_hits, temp99, $credit, and _name.

Declaring variables
You can declare a variable in two ways:

With the keyword var. For example, var x = 42. This syntax can be used to declare both local and global variables, depending on the execution context.
With the keyword const or let. For example, let y = 13. This syntax can be used to declare a block-scope local variable

Declaration and initialization
In a statement like let x = 42, the let x part is called a declaration, and the = 42 part is called an initializer. The declaration allows the variable to be accessed later in code without throwing a ReferenceError, while the initializer assigns a value to the variable. In var and let declarations, the initializer is optional. If a variable is declared without an initializer, it is assigned the value undefined.
let x;
console.log(x); // logs "undefined"

In essence, let x = 42 is equivalent to let x; x = 42.

Variable scope
A variable may belong to one of the following scopes:

Global scope: The default scope for all code running in script mode.
Module scope: The scope for code running in module mode.
Function scope: The scope created with a function.
In addition, variables declared with let or const can belong to an additional scope:

Block scope: The scope created with a pair of curly braces (a block).

When you declare a variable outside of any function, it is called a global variable, because it is available to any other code in the current document. When you declare a variable within a function, it is called a local variable, because it is available only within that function.

let and const declarations can also be scoped to the block statement that they are declared in.
if (Math.random() > 0.5) {
  const y = 5;
}
console.log(y); // ReferenceError: y is not defined

For example, the following code will log 5, because the scope of x is the global context (or the function context if the code is part of a function). The scope of x is not limited to the immediate if statement block.
if (true) {
  var x = 5;
}
console.log(x); // x is 5

Variable hoisting
var-declared variables are hoisted, meaning you can refer to the variable anywhere in its scope, even if its declaration isn't reached yet.
console.log(x === undefined); // true
var x = 3;

(function () {
  console.log(x); // undefined
  var x = "local value";
})();

var x;
console.log(x === undefined); // true
x = 3;

(function () {
  var x;
  console.log(x); // undefined
  x = "local value";
})();
Because of hoisting, all var statements in a function should be placed as near to the top of the function as possible. This best practice increases the clarity of the code.

console.log(x); // ReferenceError(RF)
const x = 3;

console.log(y); // ReferenceError
let y = 3;
Unlike var declarations, which only hoist the declaration but not its value, function declarations are hoisted entirely — you can safely call the function anywhere in its scope. See the hoisting glossary entry for more discussion.

Global variables
Global variables are in fact properties of the global object.


