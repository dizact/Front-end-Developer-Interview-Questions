#JOB INTERVIEW QUESTIONNAIRE

@version 1.0
 
##Contributors

@bentruyman (http://bentruyman.com/), @roger_raymond (http://twitter.com/iansym), @ajpiano (http://ajpiano.com/), @paul_irish (http://paulirish.com/), @SlexAxton (http://alexsexton.com/), @boazsender (http://boazsender.com/), @miketaylr (http://miketaylr.com/), @vladikoff (http://vladfilippov.com/), @gf3 (http://gf3.ca/), @jon_neal (http://twitter.com/jon_neal), @wookiehangover (http://wookiehangover.com/) and @darcy_clarke (http://darcyclarke.me)

## General Questions:

* Are you on Twitter? 
	* If so, who do you follow on Twitter?
 		* @dggodfrey - paul irish, chris coyier, jeffery way, smashing mag, nettuts, iandstewart, cameronmoll
* Are you on GitHub? 
	* If so, what are some examples of repos you follow  
 		* dizact - html5 boilerplate, nginx server config, front-end questions
* What blogs do you follow? 
	* nettuts, javascript weekly, hacker newsletter, thor newsletter
* What version control systems have you used? 
	* Git, svn, mercurial
* What is your preferred development environment? (OS, Editor, Browsers, Tools etc.) 
	* mac, submlime text 2, coda 2, chrome, weinry, node
* Can you describe your workflow when you create a web page?
	* Use print out to find common styles themes in the design, Find common aspects and create 'templates'. 
* Can you describe the difference between progressive enhancement and graceful degradation? 
	* Bonus points for the answer "no one can" 
	* Extra bonus points for describing feature detection  
 		* Graceful degredation is developing for newer browsers, but also letting older browsers will work with basic functionality. Example: using rounded corners on browsers that support it, but letting the corners be squre in <= IE8
   		* Progressive Enhancement is like Graceful degredation only backwards. Building for a specific level, and then using browser detection to load/do more.
* Explain what "Semantic HTML" means. 
	* Semantic HTML means to use items for what they are supposed to be used for. Tables are for data, not for layout. Using a definition list where appropriate, list items where appropriate...
* What does "minification" do? 
	* removes white space, removes comments, some minification techniques simplify the code to make it smaller
* Why is it better to serve site assets from multiple domains? 
	* How many resources will a browser download from a given domain at a time?  
 		* The resources can be downloaded faster and more at once. A broser will download 2 item simultaniously from a domain. (newer browsers can do more) More locations to download from, the faster/more that can be loaded at the same time.
* If you have 8 different stylesheets for a given design, how would you integrate them into the site? 
	* Looking for file concatenation.
	* Points off for `@import`, unless it works in conjunction with a build system.  
* If you jumped on a project and they used tabs and you used spaces, what would you do? 
	* `issue :retab! command`
* Write a simple slideshow page 
	* Bonus points if it does not use JS.  
* What tools do you use to test your code's performance? 
	* page speed, monitor tab
* If you could master one technology this year, what would it be? 
	* node or ruby
* Name 3 ways to decrease page load. (perceived or actual load time) 
	* Put javascript files at the bottom. Lazy load images, or load after rest of page has loaded, optimize images, decrease https requests
* Explain the importance of standards.  

## HTML-Specific Questions:

* What's a `doctype` do, and how many can you name? 
	* Doctype tells the browser what kind of document is being loaded - knows what to support. 1
* What's the difference between standards mode and quirks mode? 
	* CSS box model is rendered the old way (incorrectly)
* What are the limitations when serving XHTML pages? 
	* Are there any problems with serving pages as `application/xhtml+xml`?  
 		* page is rendered like xml which is more strict (no upper-case tags). IE7 and lower just render as html
* How do you serve a page with content in multiple languages? 
* Can you use XHTML syntax in HTML5? How do you use XML in HTML5? 
	* YEs, but you have to return as application/xml or applicaton/html+xml
* What are `data-` attributes good for? 
	* They are good for adding data to tags when not using standard attributes
* What are the content models in HTML4 and are they different in HTML5? 
	* Used to just be inline and block. Now there are more fine-grained: text-level, group, forms
* Consider HTML5 as an open web platform. What are the building blocks of HTML5? 
	* html4, 
* Describe the difference between cookies, sessionStorage and localStorage.  
	* cookie is stored in the browser, sessions are stored on the server, and local storage is a key pair value local storage by app

## JS-Specific Questions

* Which JavaScript libraries have you used? 
	* jquery, handlebars, knockoutjs
* How is JavaScript different from Java? 
	* smaller, simpler, relies on html (cannot stand alone)
* What are `undefined` and `undeclared` variables? 
	* undefined is when the value can be undefined, undeclared is the var was not created
* What is a closure, and how/why would you use one? 
	* Your favorite pattern used to create them? argyle (Only applicable to IIFEs)  
* What's a typical use case for anonymous functions? 
* Explain the "JavaScript module pattern" and when you'd use it. 
	* Bonus points for mentioning clean namespacing. 
	* What if your modules are namespace-less?  
* how do you organize your code? (module pattern, classical inheritance?) 
* What's the difference between host objects and native objects? 
* Difference between: 
```javascript
function Person(){} var person = Person() var person = new Person()
```
* What's the difference between `.call` and `.apply`? 
* explain `Function.prototype.bind`? 
* When do you optimize your code? 
* Can you explain how inheritance works in JavaScript? 
	* Bonus points for the funny answer: "no one can" 
	* Extra bonus points if they take a stab at explaining it  
* When would you use `document.write()`? 
	* Correct answer: 1999 - time to weed out the junior devs  
* What's the difference between feature detection, feature inference, and using the UA string 
* Explain AJAX in as much detail as possible 
* Explain how JSONP works (and how it's not really AJAX) 
* Have you ever used JavaScript templating, and if so, what/how? 
* Explain "hoisting". 
* What is FOUC? How do you avoid FOUC? 
* Describe event bubbling. 
* What's the difference between an "attribute" and a "property"? 
* Why is extending built in JavaScript objects not a good idea? 
* Why is extending built ins a good idea? 
* Difference between document load event and document ready event? 
* What is the difference between `==` and `===`? 
* Explain how you would get a query string parameter from the browser window's URL. 
* Explain the same-origin policy with regards to JavaScript. 
* Explain event delegation. 
* Describe inheritance patterns in JavaScript. 
* Make this work: 
```javascript
[1,2,3,4,5].duplicator(); // [1,2,3,4,5,1,2,3,4,5]
```
* Describe a strategy for memoization (avoiding calculation repetition) in JavaScript. 
* Why is it called a Ternary statement, what does the word "Ternary" indicate? 
* What is the arity of a function?  

## JS-Code Examples:

```javascript
>~~3.14
```
Question: What value is returned from the above statement? 
**Answer: 3** 

```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
Question: What value is returned from the above statement? 
**Answer: "goh angasal a m'i"** 

```javascript
( window.foo || ( window.foo = "bar" ) );
```
Question: What is the value of window.foo? 
**Answer: "bar"** 
only if window.foo was falsey otherwise it will retain its value.

```javascript
var foo = "Hello"; (function() { var bar = " World"; alert(foo + bar); })(); alert(foo + bar);
```
Question: What is the outcome of the two alerts above? 
**Answer: "Hello World" & ReferenceError: bar is not defined** 

## jQuery-Specific Questions:

* Explain "chaining". 
* What does `.end()` do? 
* How, and why, would you namespace a bound event handler? 
* What is the effects (or fx) queue? 
* What is the difference between `.get()`, `[]`, and `.eq()`? 
* What is the difference between `.bind()`, `.live()`, and `.delegate()`? 
* What is the difference between `$` and `$.fn`? Or just what is `$.fn`. 
* Optimize this selector: 
```javascript
$(".foo div#bar:eq(0)")
```

## CSS-Specific Questions:

* Describe what a "reset" CSS file does and how it's useful. 
* Describe Floats and how they work. 
* What are the various clearing techniques and which is appropriate for what context? 
* Explain CSS sprites, and how you would implement them on a page or site. 
* What are your favourite image replacement techniques and which do you use when? 
* CSS property hacks, conditionally included .css files, or... something else? 
* How do you serve your pages for feature-constrained browsers? 
	* What techniques/processes do you use?  
* What are the different ways to visually hide content (and make it available only for screen readers)? 
* Have you ever used a grid system, and if so, what do you prefer? 
* Have you used or implement media queries or mobile specific layouts/CSS? 
* Any familiarity with styling SVG? 
* How do you optimize your webpages for print? 
* What are some of the "gotchas" for writing efficient CSS? 
* Do you use CSS preprocessors? 
	* If so, describe what you like and dislike about the CSS preprocessors you have used. 
* How would you implement a web design comp that uses non-standard fonts? (avoid mentioning webfonts so they can figure it out) 
* Explain how a browser determines what elements match a CSS selector?  

## Optional fun Questions:

* What's the coolest thing you've ever coded, what are you most proud of? 
* Do you know the HTML5 gang sign? 
* Are you now, or have you ever been, on a boat. 
* Tell me your favorite parts about Firebug / Webkit Inspector. 
* Do you have any pet projects? What kind? 
* Explain the significance of "cornify". 
* On a piece of paper, write down the letters A B C D E vertically. Now put these in descending order without writing one line of code. 
	* Wait and see if they turn the paper upside down
* This should make the laugh and is a fine way to relieve some tension at the end of the interview.  
* Pirate or Ninja? 
	* Bonus if it's a combo and a good reason was given (+2 for zombie monkey pirate ninjas) 
* If not Web Development what would you be doing? 
* Where in the world is Carmen Sandiego? (hint: their answer is always wrong) 
* What's your favorite feature of Internet Explorer?
* Complete this sentence: Brendan Eich and Doug Crockford are the __________ of javascript.
* jQuery: a great library or the greatest library? Discuss.