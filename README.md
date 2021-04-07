# Scope and Closure Challenge

The module challenge is the afternoon project or assignment that students work through independently. This expands on the guided project completed earlier with the instructor.

## JavaScript Foundations

## Scope and Closures

## Objectives

- Explain function scope
- Describe what closure is, how closure is created in a program and why it is important to understand closures in JavaScript  

## Introduction

This challenge focuses on both scope and closures.

In this challenge you will be working to build a `scoreboard` (in the console) that takes randomly generated data and keeps track of a game's progress. If you're not familiar with the rules of baseball what you need to know is this: there are 9 innings and teams take turns "at-bat." Teams can only score while they are at bat. A team stops being at bat once they have gotten 3 `outs` by either striking out or through game play. You can read more about baseball rules [here](https://www.rulesofsport.com/sports/baseball.html).

A scoreboard in a major league stadium looks something like this. In fact, the scoreboard at Fenway Park in Boston is actually quite famous. 

![Fenway Scoreboard](https://storage.googleapis.com/afs-prod/media/media:e959506330fd4e5890023c93cfbaac55/800.jpeg)

There are layers upon layers of nested functions within the game of baseball. Your challenge today will be to work through tasks associated with these layers, and ultimately to produce a scoreboard that logs in the console.

## Instructions

### Task 1 - Set Up Project and Tests

1. Fork the repo
2. Clone your forked version of the repo
3. cd into your repo and create a branch with your first and last name
4. open the terminal in your vs code and type `npm install`
5. next type `npm run test:watch` in your terminal
6. Complete your work making regular commits, once you have all your tests passing and you are ready to submit your work please see canvas for instructions on how to submit

### Task 2a - MVP code

Find the file `index.js` and complete the tasks.

### Task 2b - Written questions

Edit the `ReadMe` file with your answers.

1. In your own words, define closure (1-2 sentences).

1a.) Closure is a function that accesses its lexical scope even executed outside of its lexical scope. (called a lexical environment)

2. Study the following code, then answer the questions below.

```js
function personalDice(name){
  return function(){
      // generate random number between 1 and 6
    const newRoll = Math.floor(Math.random() * 6);
    console.log(`${name} rolled a ${newRoll}`)
  }
}

const dansRoll = personalDice("Dan");

const zoesRoll = personalDice("Zoe");


dansRoll();
zoesRoll();

```

a. Where is closure used in this code? How can you tell?

~ personalDice fn, the var created inside the scope {}.

b. Compare and contrast calling `dansRoll` the first and second time. What is always the same? What could change?

~ console print will always show "Dan rolled a" and the integer changes based on the Math.random generator.

c. What is the lexical scope of `newRoll`?

~ "function()" aka an anonymous function.

### Task 3 - Stretch Goals

After you have completed the requirements, **create** a new file called `stretch.js` and practice more with closures. There are no tests for these problems.

See if you can complete one or more of the following challenges:

1. Write a function that would allow you to do this using a closure. (This is another interview question we've seen before - when you're ready for answers, view an explanation [here](https://www.coderbyte.com/algorithm/3-common-javascript-closure-questions)).

```js

var addSix = createBase(6);
addSix(10); // returns 16
addSix(21); // returns 27

```

2. Research the differences between functional programming and object oriented programming. Then, describe the pros and cons of functional programming vs object-oriented programming. This is a common interview question and great practice!

~ Both Functional programming and object-oriented programming uses a different method for storing and manipulating the data. In functional programming, data cannot be stored in objects and it can only be transformed by creating functions. In object-oriented programming, data is stored in objects.

Pros to Functional Programming: 

~ Supports the programming languages like Lisp, Clojure, Wolfram, Erlang, Haskell, F#, R, and other prominent and domain-specific languages. 

~ A great fit for data science work, and R is the popular language among data scientists.

~ FP languages can be translated well into an interactive environment, which makes the understanding of code easier.

~ Provides advantages like efficiency, lazy evaluation, nested functions, bug-free code, parallel programming. 

~ In simple language, functional programming is to write the function having statements to execute a particular task for the application.

~ The function can be easily invoked and reused at any point.  It also helps the code to be managed, and the same thing or statements does not need to write again and again.
Functional Programming based on different concepts is 1. High Order Functions (HOF). 2. Pure functions. 3. Recursion. 4. Strict and Non-strict Evaluation. 5. Type systems. 6. Referential Transparency. In functional programming, functions are referred to as first-class citizens.

Pro to OOP (Object-Oriented Programming):

~ Object-oriented programming based on the main features that are: 1. Abstraction: It helps in letting the useful information or relevant data to a user, increasing the program’s efficiency and making things simple. 2. Inheritance: It helps in inheriting the methods, functions, properties, and fields of a base class in the derived class. 3. Polymorphism: It helps in doing one task in many ways with the help of overloading and overriding, which is also known as compile-time and run-time polymorphism, respectively. 4. Encapsulation: It helps in hiding irrelevant data from a user and prevents the user from unauthorized access.

~ Object-oriented programming languages are C++, C#, Java, Python, Ruby, PHP, Perl, Objective-C, Swift, Dart, Lisp, etc. In an object-oriented application, objects can be easily reused in another application. New objects can be easily created for the same class, and code can be easily maintained and altered.

~ It also has the feature of memory management. It provides a great benefit in designing large programs, which can be easily divided into smaller parts and helps in distinguishing the components or phases that need to be executed or planned in a certain way.

## Resources

📚 [Scope and Closures Guide](https://css-tricks.com/javascript-scope-closures/)

🧠 ["I never Understood Closures" Blog](https://medium.com/dailyjs/i-never-understood-javascript-closures-9663703368e8)

## Submission Format

Please see Canvas for cohort specific submission instructions 
