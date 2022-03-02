# front-end-interview-questions

## 1. farmework vs library?

    -a library provides set of functions / objects / modules which your app code calls
    for specific functionality  ex:jquery & react

    -framework is an abstraction in which software providing a generic functionality can be selectively changed by addational user-written code this providoing app-specific software.

## **JS QUESTIONS**

## 1. Shallow vs Deep copy?

    2-Deep copy techniques depend on the three array types?
    -A deep copy means that all of the values of the new variable are copied  disconnected from the original variable.

    -A shallow copy means that certain (sub-)values are still connected to the original variable.

|                       | splice,slice,concat | json(parse,stringify) | $.extend,_.extend,_.cloneDeep |
| --------------------- | ------------------- | --------------------- | ----------------------------- |
| bool,num, strings     | deep                | deep                  | deep                          |
| arrays,objects        | shallow             | deep                  | deep                          |
| (array of funcations) | shallow             | shallow               | deep                          |

    From these elements we can create three types of arrays.

    // 1) Array of literal-values (boolean, number, string)
    const type1 = [true, 1, "true"];

    // 2) Array of literal-structures (array, object)
    const type2 = [[], {}];

    // 3) Array of prototype-objects (function)
    const type3 = [function () {}, function () {}];

## 2. What is the spread operator vs Object.assign in JavaScript?

    -The spread operator is a new addition to the set of operators in JavaScript ES6. It takes in an iterable (e.g an array) and expands it into individual elements.

    The spread operator is commonly used to make shallow copies of JS objects. Using this operator makes the code concise and enhances its readability.

    -Object.assign is in the official released and will also create a shallow copy of the object.

## 3. what is coffescript?

    -coffescript is lightweight programming language based on ruby & paython which complies into js.

## 4. what is callback function?

    -callback is a function passed into anthor function as an argument to be executed later.

## 5. what is promises?

    -is an object return value that you hope to receive in the future.
    -object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
    -Usually done by callbacks that are only used when doing I/O, e.g. downloading things, reading files, talking to databases

## 6. Describe what is the difference between Null and Undefined?

    Null is an object with no value.
    Undefined is a type.

    typeof null; // “object”
    typeof undefined; // “undefined”

## 7. Explain the difference between cookies, session storage, and local storage?

    Cookies allow applications to store data in a client’s browser.
    Session storage property allows applications to store data until the window is closed.
    Local storage property lets applications to store data without an end.

## 8. what is Event Delegation?

    -Event Delegation is basically a pattern to handle events efficiently. Instead of adding an event listener to each and every similar element, we can add an event listener to a parent element and call an event on a particular target using the . target property of the event object.

## 9. How can you increase page performance?

    I can increase the page performance by the following methods.

    Clean up the HTML document.
    Reduce external HTTP requests.
    Sprites, compressed images, smaller images.
    Incorporate JavaScript at the bottom of the page.
    Minify CSS, JavaScript, HTML.
    CDN and Caching.

## 10. What is Ajax?

    AJAX (Asynchronous JavaScript and XML) allows applications to transport data to/from a server asynchronously without refreshing the page. This means that it is likely to update parts of a web page, without reloading the entire page. For instance, your new Gmail messages arrive and are marked as new even if you have not refreshed the web page.

## 11. what is closure?

    A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

    -Closure is a local variable for function that kept in memo even after function is returned.
    -Closure’s conflicts happen when using for loop.

        function makeFunc() {
        var name = 'Mozilla';
        function displayName() {
        alert(name);
        }
        return displayName;
        }

        var myFunc = makeFunc();
        myFunc();

## 12. what is json?

    -(javascript object notation), is a lightweight format for storing and transportiong data from server to webpage.

## 13. Async vs sync?

    -Async operation you can move to other task before the pervious one is finished.
    -sync operation task is performd in sequence

## 14. what is Javascript?

    -JavaScript is a lightweight, cross-platform, and interpreted scripting language.

## 15. what is hoisting?

    -it mean a variable can be used before it has been declared.
    but in case const & let it will return reference error.

## 16. DOM vs BOM?

    DOM is a subset of BOM.
    -DOM Stands for Document Object Model:Defines a standard way to access and
    manipulate HTML documents.
    We can access any
    markup content via
    innerHTML,
    innerText, or
    textContent
    properties

    -BOM Stands for Browser Object Model:is the top level of
    the DOM hierarchy.
    ▻ navigator object,
    ▻ screen object,
    ▻ history object
    ▻ location object,
    ▻ document object

**For some reason, the Browser Object Model is generally not referred to by its proper name. More often, it's usually wrapped up with the DOM. Because no standards exist for the BOM, each browser has its own implementation.**

## 17. ES6 Features

    ▰ let + const
    ▰ Binary and Octal literals
    ▰ default Parameters
    ▰ Classes
    ▰ rest parameters
    ▰ iterators
    ▰ spread operator
    ▰ Generators
    ▰ Destructuring (array/object)
    ▰ Symbols
    ▰ Arrow Functions
    ▰ Proxies
    ▰ Enhanced object literals
    ▰ Modules
    ▰ Template strings
    ▰ Module loaders
    ▰ for..of
    ▰ Promises
    ▰ math API
    ▰ number API
    ▰ string API
    ▰ array API
    ▰ object API
    ▰ Data Structure/Collection
    ▻ map
    ▻ set
    ▻ weakmap
    ▻ weakset

    ▰ES6 represents block scope via let, const.
    ▻ Block starts by { and ends by }
    ▰ Variables declared with let and const don’t
    hoist.
    ▰ Variables defined by let can be reassigned
    ▰ Variable defined by const cant be reassigned

**Nowadays we can use let to overcome closure problem with loops**

## 18. what is (IIFE): JavaScript Immediately-invoked Function Expressions ?

    An Immediately-invoked Function Expression is a way to execute functions immediately, as soon as they are created. IIFEs are very useful because they don't pollute the global object, and they are a simple way to isolate variables declarations

## 19. what is Arrow Function?

    Arrow function is one of the features introduced in the ES6 version of JavaScript. It allows you to create functions in a cleaner way compared to regular functions.

    pros:
    - Arrow Function as an Expression
    - Arrow Function with One Argument
    - Arrow Function with no Argument
    - Multiline Arrow Functions

    cons:
    - You should not use arrow functions to create methods inside objects.
    - You cannot use an arrow function as a constructor.

## 20. what is rest Parameter?

    ▰Used in function definition and must be the last
    parameter in function definition.
    ▰It gathers all remaining arguments into an array
    element.

        function displayNames(p1, ...arr) {
        for (let i in arr) {
        console.log(arr[i])
        }
        }
        var fruits = ["apple", "strawberry",
        "banana", "orange", "mango"];
        displayNames(10, fruits)

## 21. what is spread operator?

    ▰Used in function invocation
    function dis(f, n) {
    console.log(f + "" + n)
    }
    var rest = ["ahmed", "ali"]
    dis(...rest)

    ▰Used also in Array
    var fruits = ["apple", "strawberry", "banana", "orange", "mango"];
    var newFruits = ["kiwi", ...fruits]
    // ["kiwi", "apple", "strawberry", "banana", "orange", "mango"]
    var anotherNewFruits = ["kiwi", ...fruits, "others"]
    // ["kiwi", "apple", "strawberry", "banana", "orange", "mango", "others"]

## 22. what is Destructuring Assignment?

    -object destructure:
        const user = {
        id: 42,
        isVerified: true
        };

        const {id, isVerified} = user; //id=42 , isVerified=true

    -Array Destructuring:
        let users = ["ali", "nour", "kareem"];
        let [a, b, c] = users;
        console.log( a, b, c );
        //a = users[0]
        //b = users[1]
        //c = users[2]

## 23. what is Object shorthand literal creation?

<!-- BEFORE -->

**BEFORE**

    var User = function (id, firstName, lastName) {
    return {
    id: id,
    firstName: firstName,
    lastName: lastName
    };
    }

<!-- AFTER -->

**AFTER**

    var User = function (id, firstName, lastName) {
    return {
    id,
    firstName,
    lastName
    };
    }

## 24. what is Template strings?

    Template strings are string literals allowing embedded expressions using `` and ${}

## 25. what is prototypal inheritance?

    -Inheritance in JavaScript works through something called prototypes and this form of inheritance is often called prototypal inheritance

## 25. what is virtual dom?

    A virtual DOM is a lightweight JavaScript representation of the DOM used in declarative web frameworks such as React, Vue.js, and Elm.[1] Updating the virtual DOM is comparatively faster than updating the actual DOM (via js). Thus, the framework is free to make unnecessary changes to the virtual DOM relatively cheaply.

## 26. what is seo?

    SEO stands for “search engine optimization.” In simple terms, it means the process of improving your site to increase its visibility when people search for products or services related to your business in Google, Bing, and other search engines.

## 26. what is premtives and none premtives?

- Primitives are the most basic kinds of data types and they directly contain values (numbers - string - boolean - undefind - null - symbol - bigint).
- premtive types are stored in call stack (js engine)

- Non primitive data types are called reference types in Java and they refer to an object. They are created by the programmer and are not defined by Java like primitives are. A reference type references a memory location where the data is stored rather than directly containing a value. (object literals - arrays - funcations - many more)
- reference types are stored in HEAP (js engine)

## 27. ts vs js function overloading?

    If a class has multiple methods having same name but different in parameters, it is known as Method Overloading.

    If we have to perform only one operation, having same name of the methods increases the readability of the program.

## 28. Why Would You Use POST Instead of GET for a Read Operation??

#### Security reasons

    When a get GET request is received, many servers log information about the incoming request. Most of them will log the whole requested URL including query parameters, which might include sensitive
    information.

#### URL length

    Browsers and HTTP servers can have a maximum URL length. For example Microsoft Internet Explorer is limited to 2,048 characters, and Apache HTTP Server can handle up to 4,000 characters in a URL. In our case, given that a telephone number might have a maximum length of 9 characters, there would be no reason to use POST instead of GET.

## 29. what is solid?

- SOLID stands for:
  S - Single-responsiblity Principle: A class should have one and only one reason to change, meaning that a class should have only one job.

  O - Open-closed Principle: Objects or entities should be open for extension but closed for modification.

  L - Liskov Substitution Principle: This means that every subclass or derived class should be substitutable for their base or parent class.

   - Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.

  I - Interface Segregation Principle: A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.

  D - Dependency Inversion Principle: Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.

## 30. set vs array in js?

    -Array:
    -is type of structure representing block of data (numbers, objects, etc…) allocated in consecutive memory.
    -elements in Array can be duplicate (unless you tell it not to be)
    -Array is considered as “indexed collection” type of data


    -Set:
    -more familiar as a Math concept, is an abstract data type which contains only distinct elements/objects without the need of being allocated orderly by index.
    -elements just can’t be duplicate of arrays this is the main use case of set (regardless what you decide).
    -Set is considered as “keyed collection”.
    -it's element are unique, order is irrelevent.
    -no  need to geeting out values of set, all you need from set to check if it has certain value of no with (has())
    - sets are also iterables
        for(const order of orderSet) console.log(order)
    -convertion from set to array :
    const staff = ['nada','ayman','nada']
    const staffUniqueArray =[... new Set(staff)] to convert it to array

## 31. different ways to  import files in js?
- `https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import`

    import './files' >> lazy loading file
    import x from './files'
    import {x} './files'

## 32. abstract class vs interface?

    ***************************Abstract class*****************************
    1) Abstract class can have abstract and non-abstract methods.
    2) Abstract class doesn't support multiple inheritance.
    3) Abstract class can have final, non-final, static and non-static variables.
    4) Abstract class can provide the implementation of interface.
    5) The abstract keyword is used to declare abstract class.
    6) An abstract class can extend another Java class and implement multiple Java interfaces.
    7) An abstract class can be extended using keyword "extends".
    8) A Java abstract class can have class members like private, protected, etc.
    9)Example:
    public abstract class Shape{
    public abstract void draw();
    }


    *****************************Interface********************************
    1) Interface can have only abstract methods. Since Java 8, it can have default and static methods also.
    2) Interface supports multiple inheritance.
    3) Interface has only static and final variable
    4) Interface can't provide the implementation of abstract class.
    5) The interface keyword is used to declare interface.
    6) An interface can extend another Java interface only.
    7) An interface can be implemented using keyword "implements".
    8) Members of a Java interface are public by default.
    9) Example:
    public interface Drawable{
    void draw();
    }

## **Angular Questions**

## 1. what is Directives?

    Directives are classes that add additional behavior to elements in your Angular applications.

    types:
    Attribute Directives
    Component Directives
    Structural Directives

## 2.What is the AOT vs JIT?

    JIT(Just-in-Time) compilation: The application compiles inside the browser during runtime
    AOT(Ahead-of-Time) compilation: The application compiles during the build time.

## 3. what is SPA?

    In the SPA, the whole page is not reloaded every time, only every time the view will be change.

    So when you load the application for the first time, not all the pages from the server will be rendered... It's only index.html that loads when you load the application.

    Advantages of SPA:

    -No page flicker. Native application feel.

    -Client-side routing and data rendering on the client side.

    -Data from server is in JSON format.

## 4. Why prioritize TypeScript over JavaScript in Angular?

    TypeScript is a superset of Javascript as it is Javascript + Types or extra features like typecasting for variables, annotations, variable scope and much more. The typescript is designed in a way to overcome Javascript shortcomings like typecasting of variables, classes, decorators, variable scope and many more. Moreover, Typescript is purely object-oriented programming that offers a "Compiler" that can convert to Javascript-equivalent code.

## 5.Question: Describe the MVVM architecture?

( Model- View - ViewModel )
The architecture allows the children to have reference through observables and not directly to their parents.

    Model: It represents the data and the business logic of an application, or we may say it contains the structure of an entity.

    View: View is a visual layer of the application, and so consists of the UI Code(in Angular- HTML template of a component.). It sends the user action to the ViewModel but does not get the response back directly. It has to subscribe to the observables which ViewModel exposes to it to get the response.

    ViewModel: It is an abstract layer of the application and acts as a bridge between the View and Model(business logic).  View and ViewModel are connected with data-binding so, any change in the View the ViewModel takes note and changes the data inside the Model.

## 6. What are Lifecycle hooks in Angular? Explain some life cycles hooks?

    -ngOnChanges( ): This method is called whenever one or more input properties of the component changes. The hook receives a SimpleChanges object containing the previous and current values of the property.

    -ngOnInit( ): This hook gets called once, after the ngOnChanges hook.

    It initializes the component and sets the input properties of the component.

    -ngDoCheck( ): It gets called after ngOnChanges and ngOnInit and is used to detect and act on changes that cannot be detected by Angular.

    We can implement our change detection algorithm in this hook.

    -ngAfterContentInit( ): It gets called after the first ngDoCheck hook. This hook responds after the content gets projected inside the component.

    -ngAfterContentChecked( ): It gets called after ngAfterContentInit and every subsequent ngDoCheck. It responds after the projected content is checked.

    -ngAfterViewInit( ): It responds after a component's view, or a child component's view is initialized.

    -ngAfterViewChecked( ): It gets called after ngAfterViewInit, and it responds after the component's view, or the child component's view is checked.

    -ngOnDestroy( ): It gets called just before Angular destroys the component. This hook can be used to clean up the code and detach event handlers.

## 7.Question: Explain Dependency Injection?

    Dependency injection is an application design pattern that is implemented by Angular and forms the core concepts of Angular.

    Dependencies in Angular are services which have a functionality. Various components and directives in an application can need these functionalities of the service. Angular provides a smooth mechanism by which these dependencies are injected into components and directives.

## 8. what is Observables?

    observable is a stream that allows passing of more than one event. A callback is made for each event in an observable.

## 9.Question: What is SPA (Single Page Application) in Angular? Contrast SPA technology with traditional web technology?

    Answer: In the SPA technology, only a single page, which is index.HTML, is maintained although the URL keeps on changing. Unlike traditional web technology, SPA technology is faster and easy to develop as well.

    In conventional web technology, as soon as a client requests a webpage, the server sends the resource. However, when again the client requests for another page, the server responds again with sending the requested resource. The problem with this technology is that it requires a lot of time.

## 10. What is the process called by which TypeScript code is converted into JavaScript code?

    Answer: It is called Transpiling. Even though TypeScript is used for writing code in Angular applications, it gets internally transpiled into equivalent JavaScript.

## 11. What is ViewEncapsulation and how many ways are there do to do it in Angular?

    ViewEncapsulation determines whether the styles defined in a particular component will affect the entire application or not. Angular supports 3 types of ViewEncapsulation:

    Emulated – Styles used in other HTML spread to the component
    Native – Styles used in other HTML doesn’t spread to the component
    None – Styles defined in a component are visible to all components of the application

## 12. Why prioritize TypeScript over JavaScript in Angular?

     TypeScript is a superset of Javascript as it is Javascript + Types or extra features like typecasting for variables, annotations, variable scope and much more.
     The typescript is designed in a way to overcome Javascript shortcomings like typecasting of variables, classes, decorators, variable scope and many more. Moreover, Typescript is purely object-oriented programming that offers a "Compiler" that can convert to Javascript-equivalent code.

## 13. Question: State some advantages of Angular over other frameworks.

    Out of box Features: Several built-in features like routing, state management, rxjs library, and HTTP services are straight out of the box services provided by Angular. So, one does not need to look for the above-stated features separately.

    Declarative UI: Angular uses HTML to render the UI of an application as it is a declarative language and is much easier to use than JavaScript.

    Long-term Google Support: Google plans to stick with Angular and further scale up its ecosystem as it has offered its long term support to Angular.

## 14.what is ivy?

    Ivy is the standard engine for rendering your content.

    With Ivy, you can compile components more independently of each other. This improves development times since recompiling an application will only involve compiling the components that changed.

## 15.what is angular universal?

    There are three main reasons to create a Universal version of your application (Server-Side Rendering).
    -Facilitate web crawlers through search engine optimization (SEO)
    -Improve performance on mobile and low-powered devices
    -Show the first page quickly with a first-contentful paint (FCP)

## 16. what is PWA or service worker?

    the Angular service worker follows these guidelines:

    -Caching an application is like installing a native application. The application is cached as one unit, and all files update together.

    -A running application continues to run with the same version of all files. It does not suddenly start
    receiving cached files from a newer version, which are likely incompatible.

    -When users refresh the application, they see the latest fully cached version. New tabs load the latest cached code.

    -Updates happen in the background, relatively quickly after changes are published. The previous version of the application is served until an update is installed and ready.
    The service worker conserves bandwidth when possible. Resources are only downloaded if they've changed.

## 17. what is Interceptors?

- Angular provides many built-in tools to help scale out large JavaScript applications. Interceptors are one of the built-in tools for specifically handling HTTP requests at a global application level.

Often we want to enforce or apply behavior when receiving or sending HTTP requests within our application. Interceptors are a unique type of Angular Service that we can implement. Interceptors allow us to intercept incoming or outgoing HTTP requests using the HttpClient. By intercepting the HTTP request, we can modify or change the value of the request.

In this post, we cover three different Interceptor implementations:

- Handling HTTP Headers
- HTTP Response Formatting
- HTTP Error Handling

## **RXJS**

## 1.What is RxJS?

    "Reactive Extensions for JavaScript", a library for reactive Streams which can be used to deal with asynchronous data streams and events.

    RxJS uses JavaScript reactive programming.

## 2.Q: What is Stream?

    "A stream refers to values of data overtime"

## 3.What is Observable?

    "Observable represents the idea of an invokable collection of future values or events."

    In RxJS, you model asynchronous data streams using observable sequences Or just called observables, too.
    An Observable is an object that over time and asynchronously emits multiple data values (data stream).

## 4.What is the difference between an observable and a promise?

    Promise:
    A Promise emits a single event at the completion or failure of an async operation.
    promise emits a single value
    A promise is Not Lazy A Promise cannot be cancelled

    Observable:
    An observer is like a stream and allows you to pass at least zero or more events where the callback is needed for each event.
    Observable is favored over Promise, it can emits multiple values over a time.
    The "Observable" is cold. It's not called until we're registered to it.
    You may cancel an Observable with the unsubscribe() method
    Observable provides a lot of efficient operators like map, foreach, filter, reduce, retry, retryWhen etc.

## 5. What is Observers and Subscriptions?

    Observers:

    Observer is a set of callbacks that know how to listen to the values of the Observable.
    Observers are also referred to as listeners (or consumers)
    Observers may listen or subscribe to the data being observed.

<!--  -->

    Subscription:

    Subscription is an observable execution
    Subscriptions are objects returned when an Observable is subscribed.
    Subscription is useful mainly to cancel the execution

## 6. What is Subject?

    Subjects are special types of Observers, so you can also subscribe to other Observables and listen to published data

## 7.What are different types of Subject?

    There are two types of Subjects : BehaviorSubject and ReplaySubject.

## 8.What are different between of Subject, BehaviorSubject and ReplaySubject?

## **DEVOPS QUESTIONS**

## 1. What is Devops?

    -Devops is not a technology, tool or framework.

    Devops is a cultural movement , mindest , philosophy to coordinate produce better, morw reliable products.

**by automating infrastructure, workflow and continousuly measuring application performance for which they use a lot of tools**

## 2. What Devops lifecycle?

    you can visualize a dvops process as an infinite loop.

    Dev: code - build -plan -test
    ops: release - deploy - operate - monitor

## 3. what to learn about the tools used?

    1-doocker
    2-kubernetes

## 4. what is docker?

    Docker is a tool designed to make it easier to create, deploy and run applications by using containers.

## 5. How does docker work?

    docker packages an application and all its dependencies in a virtual container that can run on linux server.

    each container runs as an isolated process in the user space and take up less space than regular vms due to thier layered architecture.
    so it will always work the same regardless of its environment.

## 6. what is kubernetes ?

    kubernetes is an open source container orchestration platform that automates deploying, managing and scaling containerization apps.

## 7. What is difference between Continuous Deployment and Continuous Delivery?

    Continuous Deployment and Continuous Delivery are two different processes.

    Continuous Deployment - refers a system that allows deployment of every new changes that comes in source code from a developer.
    Continuous Delivery - refers the automation of entire software release process.

## **Unit Testing QUESTIONS**

## 1. Benfits of Unit Testing?

- guard against breaking changes
- Analyze code behavior (expected and unexpected)
- Reveal design mistakes
- it helps you to catch defects before releasing your software.
- increase you productivity and go faster

## 2. types of tests?

- unit tests : test a component in isolation, without external resources (e.g. file system, database, API enpoints)
  - Easiest to write.
  - super fast
  - Don't give us much confidence
- integration tests: test a component with external resources (e.g file system, database, API endpoints )
- end to end: test the entire application as a whole.
  - More confidence
  - very slow
  - very fragile
