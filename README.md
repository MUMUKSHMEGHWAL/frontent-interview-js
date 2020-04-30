# frontent-interview-js
# javascript interview Questions

# NOTE:  Please go through https://javascript.info/ for in depth knowledge of javascript first.


- Type conversions https://javascript.info/type-conversions
	* Number + Number -> Addition
	* Boolean + Number -> Addition
	* Boolean + Number -> Addition
	* Number + String -> Concatenation
	* String + Boolean -> Concatenation
	* String + String -> Concatenation
- Scopes in javascript
	- Global
	- Functional
	- Block(es6)
- var Let cost. Explain let using var. 
- Arrow function and its es5 implementation
-  static variable  —> using function
	ans : function foo() {

                  if( typeof foo.counter == ‘undefined’ ) {
                        foo.counter = 0;
                    }
                     foo.counter++;
                     document.write(foo.counter+”<br />”); 
                 }
- private   variable :
	function MyClass() {
		var name  = 'Hello'; // this be private variable 
		this.getName = function() { return name;}; /// this will be public variable
	}
- Define event bubbling/capturing
- hoisting
- closure https://blog.bitsrc.io/a-beginners-guide-to-closures-in-javascript-97d372284dda
- Currying
	- 	sum(1)(2)(3)(4)(5)……(n) 
	- sum(1,2)(3), sum(1,2,3)
	- Try to solve 4-5 question of currying
- Shadow dom
- inheritance -> Classical and prototypical inheritance (difference, use cases and what to use when?)  
- -what is prototype and __proto__and their difference.
- Design Pattern : [4 JavaScript Design Patterns You Should Know ― Scotch.io](https://scotch.io/bar-talk/4-javascript-design-patterns-you-should-know#undefined) 
	-  PubSub models and singleton are important 
- Object creation methods : 
	1) “object constructor” 
	2) “object literal” syntax
	3)  Object.create 
	Difference between above 3. 
- Read about *this*.
	solve ques [Object methods, “this”](https://javascript.info/object-methods)
- https://blog.usejournal.com/implement-your-own-call-apply-and-bind-method-in-javascript-42cc85dba1b
- [Implementation of Native JavaScript Methods (forEach, Map, Filter, Reduce, Every, Some) · GitHub](https://gist.github.com/alexhawkins/28aaf610a3e76d8b8264)
- event loop, call stack —> [ECMAScript® 2020 Language Specification](https://tc39.es/ecma262/#sec-executable-code-and-execution-contexts)
- async await, promise, generator functions (What is relationship between these)
	- Create your own runner function for generator function
	- async await polyfill 
	- Promise polypill
		- https://brunoscopelliti.com/lets-write-a-promise-polyfill/
		- [Master the JavaScript Interview: What is a Promise?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)
		- [ES6 Promise polyfill · GitHub](https://gist.github.com/Rich-Harris/11010768)	
		- [How to escape Promise Hell - Ronald Chen - Medium](https://medium.com/@pyrolistical/how-to-get-out-of-promise-hell-8c20e0ab0513)
	- Compare Async/Await and Generators usage to achieve same functionality
- Promise, observables, their  differences and when to use what .
- [HTMLScriptElement - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement) Read about attributes of script
- Read about storages (local storage, session storage, indexed DB, service worker)
	- SESSION
	* The sessionStorage exists only within the current browser tab.
	* Another tab with the same page will have a different storage.
	* But it is shared between iframes in the same tab (assuming they come from the same origin).
	* The data survives page refresh, but not closing/opening the tab.
- Splice and slice diff
- Async and defer
 Two way binding implementation : [Vanilla Two-Way Binding in JavaScript - Better Programming - Medium](https://medium.com/better-programming/js-vanilla-two-way-binding-5a29bc86c787)
- Performance
	- First know how to check peformance
	- Read about critical rendering path [Understanding the critical rendering path, rendering pages in 1 second](https://medium.com/@luisvieira_gmr/understanding-the-critical-rendering-path-rendering-pages-in-1-second-735c6e45b47a)
	- Perload, prefetch(link-prefetch, dns-prefetch, pre-rendering), preconnect 
Below are point to improve performance: 
	* chunking -> route based chunking and component based chunking
	* Redux chunking (If using redux)
	* Caching policy using cache header/E-tag
	* Async loading of JS files
	* Lazy loading the JS/images/CSS
	* Reduce redirects
	* Improve server response time(SRT), optimal SRT is 200ms
	* Enable compression, compress css/html/js via gzip for files that are larger than 150B. There is brotly compression from google. Read about that.
	* Minimizing the bundles (uglifying minifying
	* Serving all assets through CDN
	* Pre-fetching or preloading scripts for make early connection (DNS-prefetch)
	* Use case dependent things like virtualization
	* Using passive listeners for scroll events etc.
	* Virtualization - only load which is to be kept at Dom, store in memory
	* Use CSS sprites to create a template for images that you use frequently on your site like buttons and icons. CSS sprites combine your images into one large image that loads all at once (which means fewer HTTP requests) and then display only the sections that you want to show. This means that you are saving load time by not making users wait for multiple images to load.

- Service worker discussion, its uses in browser.
	- caching techniques
	- offline
	- push notification
  - web worker
- PWA
	- https://scotch.io/tutorials/how-to-make-your-existing-react-app-progressive-in-10-minutes
	- [How to add a Web App Manifest and mobile-proof your site](https://medium.com/dev-channel/how-to-add-a-web-app-manifest-and-mobile-proof-your-site-450e6e485638)
- Website rendering in browsers [DOM creation and CSSOM]
- read about caching in browser and what to cache and how to cache
- Http 
	- Methods -> read their difference
	- https
	- 	https1. and https2 differences
	- websockets
	- SSE
- CORS
- - Memory management in JS
	-  [How JavaScript works: memory management + how to handle 4 common memory leaks](https://blog.sessionstack.com/how-javascript-works-memory-management-how-to-handle-4-common-memory-leaks-3f28b94cfbec)
	- [Beyond Memory Leaks in JavaScript - OutSystems Experts - Medium](https://medium.com/outsystems-experts/beyond-memory-leaks-in-javascript-d27fd48ae67e)
-  Knowledge of modern authorization mechanisms, such as JSON Web Token 
- Read about webpack and try to setup webpack for an app. 
- Read little about npm 
	






# Links/ Questions :
- synchronise a sequence of async functions : You have array of async function and you need to call them in sync manner
- How to clone an object in Javascript?
- JSON.stringify polypill
- implement watcher for object keys  
- Implement SetTimeInterval using setTimeout
	function interval(cb, ms){
  var a = {
    clear : function(){
      clearTimeout(a.timer)
    }
  };
  (function run(){
    cb();
    a.timer = setTimeout(run, ms);
  })();
  
  return a;
}
- Thennable function
class Thenable {
  constructor(num) {
    this.num = num;
  }
  then(resolve, reject) {
    alert(resolve);
    // resolve with this.num*2 after 1000ms
    setTimeout(() => resolve(this.num * 2), 1000); // (*)
  }
}
-   Create array.map/filter functionalities Using reduce: 
	FILTER : Array.reduce((accum, o, i) => {
  			return (o.id === id) ? [{...o, name: input}] : accum;
		}, []);
	MAP:  Array.reduce((accum, o, i) => {
   			return […accum,  (o.id === id) ? {...o, name: input} : o];
		}, []);
- Fatten using reduce
	var flattened = function(arr) { 
		return arr.reduce((a,b) => {
			if(Array.isArray(b)) { 
				return a.concat(flattened(b))
			} else { 
				return a.concat(b)
			}
		},[])
	};
It could be asked not to sue reduce so please try to solve in that way also.
- flat object 
function flattenObject(ob) {
    var toReturn = {};

    for (var i in ob) {
        if (!ob.hasOwnProperty(i)) continue;

        if ((typeof ob[i]) == 'object' && ob[i] !== null) {
            var flatObject = flattenObject(ob[i]);
            for (var x in flatObject) {
                if (!flatObject.hasOwnProperty(x)) continue;

                toReturn[i + '.' + x] = flatObject[x];
            }
        } else {
            toReturn[i] = ob[i];
        }
    }
    return toReturn;
}
- LRU cache implementation
- https://gist.github.com/gs-ysingh/733832f9b23de5dabe7bc6c921d22abc (important link for JS preparation)
-  React Questions : [GitHub - sudheerj/reactjs-interview-questions: List of top 500 ReactJS Interview Questions & Answers….Coding exercise questions are coming soon!!](https://github.com/sudheerj/reactjs-interview-questions)

-  Javascript basics: [GitHub - ganqqwerty/123-Essential-JavaScript-Interview-Questions: JavaScript interview Questions](https://github.com/ganqqwerty/123-Essential-JavaScript-Interview-Questions)
- For Performance : 
	- Plural sight -> profiling course
	- Udacity -> CRP 


# SYSTEM DESIGN
Read about this about this. What is system designing? 
	- Design warehouse management system
	- Snakes and ladder problem
	- design a type-ahead
	- design a food app
	- design Instagram

# DS/ALGO: 
You will only be able to solve DS algo questions if you will practice.

- Sorting
- Searching/traversing
- [50+ Data Structure and Algorithms Interview Questions for Programmers - By Javin Paul](https://hackernoon.com/50-data-structure-and-algorithms-interview-questions-for-programmers-b4b1ac61f5b0)
