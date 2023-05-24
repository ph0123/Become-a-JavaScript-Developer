# Table of Contents
- [Table of Contents](#table-of-contents)
  - [1. Introduction ](#1)
  - [2. Up and Running with JS](#2)
  - [3. Objects](#3)
  - [4. Sidebar: String Output](#4)
  - [5. DOM](#5)
  - [6. Sidebar: Variables and Data Types](#6)
  - [7. Arrays](#7)
  - [8. Functions and Methods](#8)
  - [9. Events](#9)
  - [10. Troubleshooting and Vlidating JS ](#10)
  - [11. Conclusion](#11)


1. Introduction <a name="1"></a>
   * Quiz
     * 1. Question 1 of 7: What does it mean when we say JavaScript is an "object-oriented" language?
       * JavaScript is uses objects for data storage and manipulation.
       * JavaScript objects enforce a directional flow of data. Their orientation tells us whether the data flows up or down.
       * JavaScript is modeled on a Java object, and provides a browser-level scripting language to interact with that Java object.
       * <b>JavaScript is modeled around objects with properties and methods which can be handled in a modular fashion.</b>
     * Question 2 of 7: What happens to the website and the code when you write code in the browser console?
       * When you write code in the console, that code only exists in the console. It doesn't do anything to the website or the window.
       * The console allows you to write code to your project directly in the browser. The code is automatically added to your JavaScript file in your project.
       * <b>Code in the browser console impacts the current browser instance only. It exists in the console for as long as the window is open.</b>
       * Code in the browser console impacts the website and is saved to the original files automatically. Once saved, you can recall the code in the console at any time.
     * Question 3 of 7: What is an indicator of someone being a good JavaScript developer?
       * <b>They follow standards, invest in learning, use formatting and linting tools for consistency, and write accessible code.</b>
       * They use only tabs for indentation.
       * They use only single quotes for strings.
       * They are a React expert and write only ES6.
     * Question 4 of 7: What is the natural environment for JavaScript?
       * <b>The browser, server environments, and your computer.</b>
       * The browser.
       * The code editor.
       * Server environments.
     * Question 5 of 7: What is ECMAScript?
       * A variant of JavaScript used by advanced developers.
       * <b>The specification describing how browsers should implement and interpret JavaScript.</b>
       * A specification describing the JavaScript programming language and how developers use it.
       * A modern version of JavaScript used by React developers.
     * Question 6 of 7: Where should you develop and test your JavaScript code?
       * Develop in a code editor, test in your primary browser.
       * Develop in the browser, test in the same browser.
       * <b>Develop in a code editor, test in as many browsers as you can get your hands on.</b>
       * Develop in command line tools like the browser console, test on a different computer.
     * Question 7 of 7: Why have command line and automation tools become popular in JavaScript development?
       * <b>They simplify complex processes and introduce features to help developers write better code.</b>
       * They add complexity to the development setup to ensure only real JavaScript developers are able to do the work and that amateurs give up.
       * They help developers write better code by transforming the code for browser optimization.
       * They make developers look like hackers from movies and are great for showing off.
2. Up and Running with JS <a name="2"></a>
  *Quiz
    * Question 1 of 4: When does the browser execute JavaScript?
      * By default: When the script is encountered. If the script is set to "async", asynchronously as the HTML page loads. If the script is set to "defer", when all other script is executed.
      * <b>By default: When the script is encountered. If the script is set to "async", when the script is fully loaded. If the script is set to "defer", when the entire HTML page is rendered.</b>
      * By default: After the HTML page is rendered. If the script is set to "async", asynchronously while the HTML page is rendered. If the script is set to "defer", when the user performs an action.
      * Always when the script is encountered. The difference between "async" and "defer" is in what order the scripts are executed.
    * Question 2 of 4: What is the correct markup for adding an external JavaScript file to an HTML document?
      * <b> <script src="javascript.js" async></script> </b>
      * <script src="javascript.js" async="true"></script>
      * <script type="text/javascript">javascript.js</script>
      * <script src="javascript.js" type="text/javascript"></script>
    * Question 3 of 4: What happens when you defer JavaScript?
      * The browser loads and executes the JavaScript after all HTML is rendered.
      * <b>The browser loads the JavaScript asynchronously when it is encountered, then waits until all HTML is rendered before executing the script.</b>
      * The browser loads the JavaScript asynchronously when it is encountered, then executes it when it is fully loaded.
      * The browser defers loading of the JavaScript until a function tells it to load and execute it.
    * Question 4 of 4: JavaScript modules are heavily used in frameworks like React and Vue. What is the advantage of using modules?
      * <b>Modules enable modularization of code where individual functions, components, data objects, and other parts can be separated into individual files.</b>
      * Modules are required for modern JavaScript frameworks to work properly.
      * Modules allow developers to split code into multiple files for easier sharing and maintenance.
      * Modules enable modern loading of JavaScript to improve performance.
3. Objects<a name="3"></a>
  * Some ways to access object properties:
    * console.log("The backpack object:", backpack);
    * console.log("The pocketNum value: ",backpack.pocketNum);
    * console.log("Strap length L: ",backpack.strapLength.left);
    * var query = "pocketNum";
    * console.log("The pocketNum value: ",backpack["pocketNum"]);
    * console.log("The pocketNum value: ",backpack[query]);
  * Quiz
    * Question 1 of 15: Given the code below, how do you access the property named in "let propName"?  ``` let propName = "color";
    const myObject = { ID = 3,color = "pink", propLength = 4, use = false }; 
      * Using bracket notation: myObject[propName] (correct answer)
      * Using bracket notation: myObject.[propName]
      * Using dot notation: myObject.propName
      * Using the getProperty() method: myObject.getProperty(propName)
    * Question 2 of 15: In the following object, what is the code in the second line called? const myObject = {  color: "pink" };
      * An object attribute defined using a key/value pair.
      * An object argument with an argument name and an argument value.
      * An object variable defined using a key/value pair.
      * An object property with a property name and a property value. (correct answer)
    * Question 3 of 15: Why is the best-practice to place objects inside constants?
      * So the object and its properties is unchangeable.
      * So the object isn't accidentally altered or overwritten. (correct answer)
      * So the object can be used anywhere in the code.
      * So the object remains in a constant place in the code.
    * Question 4 of 15: Which of the below object property names are not valid?
        const myObject = {
            propName = "property",         // line 1
            prop-name = "hyphenated",  // line 2
            3rdProp = "numbered",          // line 3
            $prop = "dollar",                      // line 4
            %prop = "percentage",           // line 5
            prop name = "space"              // line 6
        };
    * Lines 3, 4, and 5
    * Lines 3, 4, 5, and 6
    * Lines 2, 3, 5, and 6 (correct answer)
    * Lines 2, 4, 5, and 6
  * Question 5 of 15: How do you access an object in JavaScript?
    * Call the object using the getObject([object name]) method
    * Call the object using bracket notation: [object name]
    * Call the object using the new keyword.
    * Call the object by naming its container. (correct answer)
  * Question 6 of 15: Can an object created from a class be given the same name as the class?
    * Yes: The object is a different data type from the class and they can both have the same name.
    * No: If you give an object the same name, it will be ignored by the browser.
    * Yes: If the class is defined using a var or a let, you can create an object with the same name without conflict.
    * No: If the class is a constant, this will cause an error. If the class is not a constant, the new object will overwrite the class. (correct answer)
  * Question 7 of 15: How do you define an object in JavaScript?
    * Create a variable, give it a name, and assign it an object using square brackets: const myObject = [ // Properties and methods go here.];
    * Create a variable, give it a name, and assign it an object using parentheses: const myObject = (  // Properties and methods go here.);
    * Create a variable, give it a name, and assign it an object using the "new" keyword: const myObject = new Object(  // Properties and methods go here.);
    * Create a variable, give it a name, and assign it an object using curly brackets: const myObject = {  // Properties and methods go here.}; (correct answer)
  * Question 8 of 15: What does the this keyword refer to in a class?
    * this refers to the current class itself.
    * this refers to the class constructor.
    * this refers to the current object created from the class.  (correct answer)
    * this refers to the current property.
  * Question 9 of 15: Where do you go to find official documentation and code examples for standard built in (global) objects?`
    * The W3C reference for standard built-in objects
    * The W3Schools reference for standard built-in objects
    * Google or your preferred search engine
    * The MDN Web Docs for standard built-in objects (correct answer)
  * Question 10 of 15: How do you create a new object from a class?
    * Using the "new" keyword, naming the class, and passing the properties as parameters. (correct answer)
    * Using the "newObject" method, naming the class, and passing the properties as parameters.
    * Using the "new Object" phrase, naming the class, and passing the properties as parameters.
    * Creating a new variable and setting it equal to the class name followed by curly brackets wrapped around the properties.
  * Question 11 of 15: What is one advantage to using a class over an object constructor method?
    * Classes are easier to understand.
    * Classes can be extended.(correct answer)
    * Classes can be added to their own JavaScript module.
    * Classes are less likely to cause errors.
  * Question 12 of 15: What is the established convention for formatting objects?
    * Properties are listed on one line, methods on their own separate lines.
    * All properties and methods are listed on one line.
    * Properties are listed on their own separate line, methods are listed on one line.
    * All properties and methods are listed on their own separate line. (correct answer)
  * Question 13 of 15: What is the difference between a function and a method?
    * "functions" and "methods" are two words for the same thing.
    * A function is a function within an object. A method is a stand-alone function.
    * A function is a stand-alone function. A method is a function within an object.(correct answer)
    * A function is declared using the function keyword. A method is declared using the method keyword.
  * Question 14 of 15: Can you use arrow functions to create object methods?
    * No, object methods are defined using function declarations.
    * Yes, arrow functions can be used.
    * No, object methods must be declared using function expressions or the method definition shorthand. (correct answer)
    * Yes, arrow functions can be used, but only when they are called in as an external function.
  * Question 15 of 15: When creating a class, the prototype methods are added inside the constructor method.
    * FALSE (correct answer)
    * TRUE
4. Sidebar: String Output<a name="4"></a>
  * Quiz
    * Question 1 of 2: How do you declare a JavaScript expression inside a template literal?
      * Using curly brackets: const myString = `Some text and an {expression}.`;
      * Using a dollar symbol followed by curly brackets:const myString = `Some text and an ${expression}.`; (correct answer)
      * Using a dollar symbol followed by square brackets:const myString = `Some text and an $[expression].`;
      * Using an ampersand symbol followed by curly brackets:const myString = `Some text and an &{expression}.`;
    * Question 2 of 2: What does the following code output in the console?   let number = 5; let subtracted = 5-1; console.log("The number before" + number + "is" + subtracted + ".");
      * The number before 5 is 4.
      * The number before 5 is 5-1.
      * The number before [number] is [subtracted].
      * The number before5is4.(correct answer)

5. DOM<a name="5"></a>
   * [MDN Javascripts document](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
   * Quiz
    * Question 1 of 11: What method(s) would you use to check if an element has a specific ID and if so replace it with a different ID?
      * The element.setAttribute() method.
      * The element.attribute property.
      * The element.hasAttribute() method.
      * the element.hasAttribute() and element.setAttribute() methods. (Correct)
    * Question 2 of 11: What is the difference in the return from the element.className and element.classList properties?
      * element.className returns a string containing the first class appended to the element. element.classList returns a string containing all classes appended to the element.
      * element.className returns the HTML content of an element with the specified class. element.classList returns a list of all classes used in the document.
      * element.className returns an array with each class appended to the element as an array item. element.classList returns a DOMTokenList with each class appended to the element.
      * element.className returns a string containing all classes appended to the element. element.classList returns a DOMTokenList with each class appended to the element. (Correct)
    * Question 3 of 11: What does the HTML markup of this image element look like after the following script has executed? " const newImage = document.createElement("img");    newImage.classList.add("feat-img");
    newImage.setAttribute("src", "logo.svg"); newImage.setAttribute("alt", "The company logo"); newImage.style.cssText = "display: block";"
      * <img style="display: block;" src="logo.svg" alt="The company logo">
      * <img class="feat-img" src="logo.svg" title="The company logo" tyle="display: block;">
      * <img class="feat-img" src="logo.svg" alt="The company logo" style="display: block;"> (Correct)
      * <img class="feat-img display: block;" src="logo.svg" alt="The company logo">
    * Question 4 of 11: What is the value of const target after this code has executed? const target = document.querySelectorAll("a");
      * A single element object of the first element matching the query.
      * An array containing each element object matching the query.
      * A node list containing each element object matching the query if there is more than one match, a single element object if there is only one match.
      * A node list containing each element object matching the query. (Correct)
    * Question 5 of 11: What is the value of const target after this code has executed (assuming there are elements in the DOM with the class "note")? const target = document.getElementsByClassName(".note");
      * An array-like HTMLCollection object containing each element with the class "note". 
      * An empty array-like HTMLCollection object. (Correct)
      * A node list containing each element with the class "note".
      * A value of "undefined
    * Question 6 of 11: The querySelector() and querySelectorAll() methods use what kind of selectors as their parameter?
      * Any HTML element or classname.
      * An HTML selector string.
      * A CSS selector string. (Correct)
      * A custom function.
    * Question 7 of 11: What happens if you run this code: const target = document.querySelector(".first-paragraph"); target.style.font-family = "sans-serif";
      * "Uncaught SyntaxError: Invalid left-hand side in assignment" (Correct)
      * The inline style for the target element is set to "font-family: sans-serif;"
      * Nothing. The syntax is wrong so the browser ignores this line of code.
      * "Uncaught SyntaxError: Invalid CSS selector"
    * Question 8 of 11:     What does the element.classList.toggle() method do?
      * Adds the a class named "toggle" to the element.
      * Adds the specified class if it is not appended to the element, removes the specified class if it is appended to the element. (Correct)
      * Adds the specified class if it is not appended to the element, leaves the specified class in place if it is appended to the element.
      * Toggles the display property from "none" to "block" to hide or show the element.
    * Question 9 of 11: Where in the HTML document does the new element appear when you use the document.createElement() method?
      * Nowhere: The element is created, but has not been added to the DOM. (Correct)
      * At the bottom of the HTML document.
      * Inside the specified element container.
      * At the top of the HTML document.
    * Question 10 of 11: What is the "DOM"?
      * DOM is short for "Document Object Model", the document object the browser creates when it renders an HTML document. (Correct)
      * DOM is the JavaScript environment the browser creates for each HTML document.
      * DOM is the name of a 2012 album by German singer Joachim Witt
      * DOM is short for "Document Object Master", the original document the browser renders.
    * Question 11 of 11: How do you add an element created using reateElement() to the DOM?
      * Using the insertAdjacentElement() method.
      * All these options and more. (Correct)
      * Using the prepend() method.
      * Using the append() or appendChild() methods.
6. Sidebar: Variables and Data Types<a name="6"></a>
   * Question 1  of 8: What does a single equals symbol in JavaScript indicate?
   	* The values to the left and right are compared.
   	* A value is matched with the value of a named variable.
   	* The values to the left and right are equal.
   	* A value is assigned to the named variable. (Correct)
   * Question 2  of 8: What happens if you use a named variable without first declaring it using the var, let, or const keywords?
   	* A const is created with the name and value assignment.
   	* A global var is created with the name and value assignment. (Correct)
   	* JavaScript asks what type of variable this is.
   	* An error is triggered and JavaScript stops rendering.
   * Question 3  of 8: What is the value of defaultColor when it is logged in the console?
           var defaultColor = "purple";
           function setColor() {
               if ( defaultColor === "purple" ) {
                   let defaultColor = "orange";
               }
           }
           setColor();
           console.log(defaultColor);
   	* Undefined
   	* "purple" (Correct)
   	* The console.log statement happens in the global scope while the color is changed in a local scope where a separate let with the same name is created. let defaultColor only exists inside the function scope of setColor().
   	* defaultColor
   	* "orange"
   * Question 4  of 8: How do you capture the result of a math equation like 42 * 38 in JavaScript?
   	* Create a variable to hold the math equation and then capture the result in another variable.
   	* Create a variable and set it equal to the math equation. (Correct)
   	* Use the math() method.
   	* Use the sum() method.
   * Question 5  of 8: In what scenario should you use var instead of let to define a variable?
   	* When you need a variable to be available in other modules than the one it is defined (thus a "global" variable).
   	* When you need a locally scoped reassignable variable only available within the current function scope.
   	* When you need a globally scoped reassignable variable available to all functions and statements. (Correct)
   	* When you need a globally scoped unassignable variable available to all functions and statements.
   * Question 6  of 8: Which statement is true?
   	* Array items within a constant cannot be changed.
   	* A var or let variable containing an object cannot be reassigned to an array because it is a different data type.
   	* Only const variables can be exported from a JavaScript module for import in another module.
   	* Object properties within a constant can be changed. (Correct)
   * Question 7  of 8: What is logged in the console after this code is executed?
           let sum = 23.95;
           let tip = "3";
           console.log("The total is $" + sum + tip + ".");
   	* Syntax error.
   	* "The total is $26.95 + 3"
   	* "The total is $26.95."
   	* "The total is $23.953." (Correct)
   * Question 8  of 8: What is the do the operators (equals symbols) in these three lines of code signify?
   a = b a == b a === b
   	* a = b means b holds the result of whatever equation happens on the side of a. a == b means the value of b is assigned to a. a === b tests for equality between a and b.
   	* a = b assigns the value of b to a. a == b tests for equality between a and b. a === b tests for identical equality between a and b. (Correct)
   	* a = b tests for equality between a and b. a == b tests for identical equality between a and b. a === b tests for absolute equality between a and b.
   	* a = b assigns the value of b to a. a == b tests for identical equality between a and b. a === b is a misspelling of a == b and works the same way.
7. Arrays<a name="7"></a>
8. Functions and Methods<a name="8"></a>
9.  Events<a name="9"></a>
10.    Troubleshooting and Vlidating JS <a name="10"></a>
11.   Conclusion<a name="11"></a>
