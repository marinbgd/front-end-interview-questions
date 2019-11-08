# [Front-end Job Interview Questions]




## General


* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* What is Flash of Unstyled Content? How do you avoid FOUC?
* What does CORS stand for and what issue does it address?
* Have you heard for caniuse.com website and what is his purpose?



## HTML


* What does a <b>doctype</b> do?
	1) DOCTYPE describes the HTML that will be used in your page.
	2) Browser use DOCTYPE to determine how to render a page. Also, DOCTYPE tells the consuming user agent (web crawlers, validation tools) what type of document is and how parse/validate them.
* What's the difference between full standards mode, almost standards mode and quirks mode?
* What's the difference between HTML and XHTML?
	1) XHTML is an HTML that follows the XML rules, which means a XHTML document must have well-formed markups in order to be rendered properly in all web browsers. Differently from XHTML, the HTML document can be rendered in most of the browsers even with markup errors such as no closing tags or wrong nested tags.
* What are data- attributes good for and how you can use them?
    1) They are providing us to store some extra information's that we can later use in HTML. We can use them in our JS (via getAttribute method) with their full HTML name to read them. Also they can be used in CSS like this: .content:before {content: attr(data-content)}
* Why is it generally a good idea to position CSS links between head/head and JS scripts just before /body? Do you know any exceptions?
* What is progressive rendering?
    1) It is technique used to render web page as quickly as possible :)
     Examples are <i>Lazy Loading</i> (for images typically) and <i>Prioritizing visible content</i> (include only the minimum css/content/scripts) necessary for web page render as fast as possible for user. You can than use deferred JS to load rest of the content.
* Can you describe <b>aside</b> tag?
* When you're going to use <b>figure</b> tag?
* How are <b>figure</b> and <b>figcaption</b> related to each other?


## CSS
* What is the difference between classes and IDs in CSS?
    1) ID's are unique, classes are not. Each element can have just one ID, each page can have only one element with that ID. On the other side, you can use the same class on multiple elements and you can use multiple classes on same element.
    2) Classes have no special abilities in the browser, but ID's do have one very important trick up their sleeve. This is the "hash value" in the URL. If you have a URL like http://yourdomain.com#comments, the browser will attempt to locate the element with an ID of "comments"
       and will automatically scroll the page to show that element. It is important to note here that the browser will scroll whatever element it needs to in order to show that element, so if you did something special like a scrollable DIV area within your regular body, that div will be scrolled too.
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Explain CSS sprites, and how you would implement them on a page or site.
    1) That is collection of images put into a single image. Web page with many images can take a long time to load and multiple images requires more HTTP requests. Also, when you make sprite file size of that file is smaller than multiple files. That an save nice amount of bandwith.
* What are the different ways to visually hide content?
* What is the difference with display: none and visibility: hidden?
    1) display: none means that tag in question will not appear at page at all. - Although you can still  interact with it through the DOM.
    2) visibility: hidden means that the tag is not visible but space is allocated for it one the page. The tag is rendered (it have width and height).
* How do you optimize your webpages for print?
    1) There is media query @print for that purpose where you can write specific rules (margins, fonts size...) that will be used for print. Also, web site prepared for print is more SEO friendly.
* What are the advantages/disadvantages of using CSS preprocessors?
	* Describe what you like and dislike about the CSS preprocessors you have used.
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
    1) This model describes the content of the space taken by an element. Each box has four edges: the margin edge, border edge, padding edge, and content edge. With rule box:sizing: border-box, content box, initial, inherit, you can 'tell' browser how to render margin, padding, border on that element.
* What does * { box-sizing: border-box; } do? What are its advantages?
    1) Written by Paul Iris Box Sizing FTW uses border box on HTML (html: box-sizing: border-box;) and (*, *: before, after {box sizing: inherit;). That way, we're telling all components and their children to follow border box sizing property.
* Is there any reason you'd want to use translate() instead of absolute positioning, or vice-versa? And why?
	* - translate is a CSS3 feature
	* + translate would not trigger browsers re-render pipelint (js->style->layout->paint->composite), so it is fast
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
    1) display: inline; can't have width and height or a vertical margin. We're using inline element in sentence, when you have, let's say <em> </em> or <i></i>, tag in sentence.
    2) display: block; it gets full width of parent container, can have width, height and margins.
* What's the difference between a relative, fixed, absolute and statically positioned element?
* When would you use CSS float?
	1) Float is used when you want to make an element of your page (usually an image) be pushed to the right or left and make other elements wrap around it.
* When would you use CSS clear?
	1) When you want an element on the left or right of the floating element not to wrap around it, you can use clear.
* Does margin-top or margin-bottom has effect on inline element?
    1) No. You can use inline-block for that purpose.
* Does padding-top or padding-bottom has effect on inline element?
    1) Yes, padding will work.
* Which one would you prefer among px, em % or pt and why?
* What is specificity? How do u calculate specificity?
* What is shadow DOM?
* How does Z index function?
    1) Overlapping may occur while using CSS for positioning HTML elements. Z index helps in specifying the overlapping element. It is a number which can be positive or negative, the default value being zero.
* How comments can be added in CSS?
    1) The comments in CSS can be added with /* and */.
* What <b>div, p</b> will do?
    1) Selects all DIV elements and all P elements
* What <b>div p</b> will do?
    1) Selects all P elements that are anywhere inside a DIV element
* What <b>div > p</b> will do?
    1) Selects all P elements where the immediate parent is a DIV element
* What <b>div + p</b> will do?
    1) Selects all P elements that are placed immediately after a DIV element
* What <b>div ~ p</b> will do?
    1) Selects all P elements that are anywhere preceded by a DIV element
* In CSS3, how would you select every A element whose href attribute value begins with “https”?
    1) a[href^="https"]
* What is the use of column layout in CSS?
    1) CSS column layout helps you to divide your text in to columns:
    ```
        -moz-column-count:3; /* Firefox */
        -webkit-column-count:3; /* Safari and Chrome */
        column-count:3;
    ```
* Have you heard for Flexbox?
    1) If answer is YES...next question related with Flexbox.

## Responsive Web Design
* Have you used or implemented media queries or mobile specific layouts/CSS?


## JavaScript - DOM related
* Is there any difference between window and document?
    1) Window is the actual global object, it's main JS object root. Document is where DOM is.
* Does document.onload and window.onload fire at the same time?
    1) document.onload is fired when the DOM is ready which can be prior to images and other external content is loaded. On the other side, window.onload is fired when entire page is loaded -images, css, sprites.
* Is attribute similar to property?
	1) Attributes are in the HTML itself, rather than in the DOM. They are very similar to properties, but not quite as good. When a property is available it’s recommended that you work with properties rather than attributes.
	2) An attribute is only ever a string, no other type.
	3) Attributes can be useful when you want to set a custom attribute, that is, when there is no property associated.
	4) But, to be fair, you can also use custom properties (although this might be bad practice).
	5) JS DOM objects have properties. These properties are kind of like instance variables for the particular element. As such, a property can be different types (boolean, string, etc.).
* What are the different ways to get an element from DOM?
    1) by ID: getElementById('elemID');
    2) by Tag Name: getElementsByTagName('p');
    3) by class: getElementsByClassName('className');
    4) by CSS Selector: querySelectorAll('p.someClass');
* What is reflow? What causes reflow? How could you reduce reflow?
* What is repaint and when does this happen?
* How could you make sure to run some JavaScript when DOM is ready like $(document).ready?

## JavaScript
* Explain the difference between the JavaScript call and apply functions.
    1) Apply lets you to invoke function with arguments as an array.
* What are the differences between null and undefined?
	1) In javascript, null is an object with no value and undefined is a type.
	2) typeof null; // "object"
	3) typeof undefined; // "undefined"
* What are the differences between == and ===?
    1) When JS compiler sees == he try to coerce two types (LHS and RHS). 3 equal signs means 'check if they are same by the value and type' without coercion.
* How would you compare two objects in JavaScript?
	1) JSON.stringify(obj1) === JSON.stringify(obj2)
	Works when you have simple JSON-style objects without methods and DOM nodes inside. Also, the order of properties is important.
	2) check each property value
	3) lodash :) _.isEqual(object, other);
	4) In Angular JS angular.equals(o1, o2);
* Explain how prototypical inheritance works.
* What do you think of AMD vs CommonJS?
* What's the difference between a variable that is: null, undefined or undeclared?
    1) <b>undeclared</b> variable is when you try to access non-existing variable.
    2) <b>null</b> is a special value meaning "no value".
    3) <b>undefined</b> means that the variable has not been declared, or has not been given a value. (More info under hoisting question).
* What is a closure, and how/why would you use one?
  1) Consider this example:
     ```javascript
        function foo() {
          var a = 2;
          function bar() {
            console.log(a);
          }
          return bar;

        var baz = foo();

        baz(); //2
     ```
    2) bar() still has a reference to that scope, and that reference is called closure.
    3) Imagine you sharing some data between two mobile phones via bluetooth, lets say. One phone 'closes over' connection with other phone and have access to other phone data while connection is alive.
* Define the term 'closure' and give an example of it in JavaScript.
    1) Closure is when a function is able to remember and access its lexical scope even when that function is executing outside its lexical scope.
    2) Module Pattern example
    ```javascript
        function CoolModule() {
            var something = "cool";
            var another = [1, 2, 3];

            function doSomething() {
                console.log( something );
            }

            function doAnother() {
                console.log( another.join( " ! " ) );
            }

            return {
                doSomething: doSomething,
                doAnother: doAnother
            };
        }

        var foo = CoolModule();

        foo.doSomething(); // cool
        foo.doAnother(); // 1 ! 2 ! 3
    ```
* What's a typical use case for anonymous functions?
* How do you organize your code? (module pattern, classical inheritance?)
* Explain "hoisting".
    1) What actually rise the name 'Hoisting' is how compiler works. When he sees var a = 2; for him that is actually two assignments. (var a; is 'moved to top'). Only declaration is 'moved' to the top, while assignment is left in place.
* What is output of this? (Hoisting related)
    1)
    ```javascript
        a = 2;
        var a; //var a 'moved to top', then 2 is assigned as value, so result is 2
        console.log( a ); //2
     ```
* What is output of this? (Hoisting related)
    1)
    ```javascript
        console.log(a); Compiler sees var a; and a is undefined at the moment. When console.log executes, a is undefined, it has no value at that moment.
        var a = 2; //undefined
    ```
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Describe event capturing and bubbling.
    1) With capturing, the event is first captured by the outermost element and propagated to the inner elements.
    2) With bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements.
* Why is extending built-in JavaScript objects not a good idea?
* What is "use strict";? what are the advantages and disadvantages to using it?
    1) Disallows global variables.
    2) Silent failing assignments will throw error in strict mode (assigning NaN = 5;)
    3) Attempts to delete undeletable properties will throw (delete Object.prototype)
    4) Requires all property names in an object literal to be unique (var x = {x1: "1", x1: "2"})
    5) Forbids the with keyword
    6) eval in strict mode does not introduce new variables
    7) arguments.callee is not supported
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
* How can we add and remove data from local storage?
    1) localStorage.setItem(&ldquo;Key&rdquo;,&rdquo;Item&rdquo;);
    2) localStorage.getItem(&ldquo;Key&rdquo;);
* What is the lifetime of local storage?
    1) Local storage does not have a life time it will stay until either the user clear it from the browser or you remove it using JavaScript code.
## AngularJS


## Testing
* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?


## Performance
* How would you optimize a website's assets/resources?
* Traditionally, why has it been better to serve site assets from multiple domains?
* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.


## OOP
* What are the 4 major principles of Object Oriented Programming ?
    1) Encapsulation, Abstraction, Inheritance, Polymorphism
* How to achieve encapsulation in JavaScript?
    1) via closures, module pattern
* What is method overloading? Is it possible in JavaScript?
    1) There is no real function overloading in JavaScript. If you want to fake it, you have to check inside the function how many arguments have been passed and what type they are...
* How can you declare a class in Javascript?
	1) In javascript there's no classes like in Java, what we actually call a class is in reality a function simulating a class behaviour:
	2) using function as a constructor
	3) object literal notation
* How can you add a method to a class already defined?
	1) using prototype
	2) adding methods via prototype is the most inexpensive way in terms of performance since the method is tied to the prototype of the class. It means, for every new instance of class Person, you will have access to the prototype's walk() method. Now, if you declare walk() method inside the Person class, you will end up recreating the method for every new instance of Person.


## ES6 - Top Features
* Default Parameters
* Template Literals
* Multi-line Strings
* Destructuring Assignment
* Enhanced Object Literals
* Arrow Functions
* Promises
* Block-Scoped Constructs Let and Const
* Classes
* Modules


## Fun
* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?


## Coding Questions
* Question: How would you make this work?
	* add(2, 5); // 7
	* add(2)(5); // 7

* Question: What is the value of foo.length?
    1)
    ```javascript
    var foo = [];
    foo.push(1);
    foo.push(2);
    ```

* Question: Add up all the values in an array
* Question: Write a function that determines if a string starts with an upper-case letter A-Z
    1) var word = "Someword";
    2) console.log( /[A-Z]/.test( word[0]) );
    3) console.log( /^[A-Z]/.test( word) ); //regex
    4) console.log( word[0] === word[0].toUpperCase() );

* Question: What is the result of the following function
    1) function f() {
        return
            {
                a: 2
            }
        }
        f();
    //it is 'undefined' because of the ASI - automatic semicolon insertion



## BAD QUESTIONS
* Anything related to race, religion, gender, national origin, age, military service eligibility, veteran status, sexual orientation, or physical handicap!
* Don't ask if they have kids or if they are married ( This might give the impression that you think that people with kids aren’t going to devote enough time to their work or that they are going to run off and take maternity leave.)
* Basically, stick to questions which are completely relevant to the job for which they are interviewing.
* “impossible questions”


## SUGGESTIONS
* write immediate feedback after the interview
* If you’re having trouble deciding, there’s a very simple solution. NO HIRE!
* Look for passion. Smart people are passionate about the projects they work on. They get very excited talking about the subject. They talk quickly, and get animated. Being passionately negative can be just as good a sign.
* Bad candidates just don’t care and will not get enthusiastic at all during the interview. A really good sign that a candidate is passionate about something is that when they are talking about it, they will forget for a moment that they are in an interview.