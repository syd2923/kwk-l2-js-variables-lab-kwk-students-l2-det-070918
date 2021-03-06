# Variables Lab

## Objectives

1. Practice using the `const` and `let` variables in JavaScript

## Instructions

Ok, so this is your first JavaScript lab! You'll notice a few new things in this
lesson that we haven't encountered before. Don't worry, we'll walk you through
them.

### Tests...

The first new thing you'll notice is tests. When we want to run an experiment,
we need to develop a hypothesis and we need to test it. In programming, we run
tests serve as our experiment to verify that programs behave the way we think
they do. Tests help us identify bugs, and they give us a sense of the health of
our applications.

Here, we use tests as teaching tools. Just like in a normal coding environment,
we use tests to describe the program's behavior. You are in charge of getting
the tests to pass.

Tests in the JavaScript section can by run by typing `learn` in your console.
When run, `learn` handles a few things at once:

+ It makes sure any necessary support 'packages' are installed. The testing
suite itself is a 'package' - a collection of downloadable code, boxed up
conveniently, that integrates with our files, able to read the customized tests
that are written in the `/test` folder.

+ It runs the tests.  In the in-browser IDE, it provides a link that looks
something like:

```
http://192.241.157.192:47996
```

Clicking this will open up an HTML page that displays what tests are passing and
failing. It also actively _reruns_ the tests every time you make a change to
`index.js`.  This means that, as you write your solutions, you can flip back to
this HTML page and see it live update.  If you're using the stand alone Learn
IDE, the HTML page will open automatically.

+ Once you've solved the lab, it registers with learn.co that you've passed the
local tests, toggling the green light.

### Structure

The structure of this lab — where its files and folders are located — looks
roughly like the following:

```
├── CONTRIBUTING.md
├── LICENSE.md
├── README.md
├── index.js
├── node_modules/
├── package.json
└── test
    └── indexTest.js
```

All labs will more or less have the same structure. (And non-lab lessons, for
that matter, will still have CONTRIBUTING.md, LICENSE.md, and README.md files.)

### Code-along

For now, open up `index.js` in your text editor. If you're using the Learn IDE,
click the blue "Open", or "Open IDE", button in the top right hand corner of the
lesson. If you open up that `js-basics-variables-lab/` directory, you'll see a
list of files (along with a `test/` directory). Click `index.js`, and it will
open in the editor.

In `index.js`, you should see, well, nothing. We'll fix that soon.

Now open up `test/indexTest.js`. Hey, there's something! What's all of this
stuff doing?

**Note: The `test/indexTest.js` has great info that we want to look at, but do
not edit this file otherwise you may have extra difficulty passing this lab.**

A few lines down in the `test/indexTest.js` file you will see:

```js
describe('index.js', function () {
  // there's code in here, too
});
```

`describe` is a function provided by our test library, Mocha. The word is
basically used to hold our tests. You can see that after the word `describe` is
a description about our tests. Tests are used as a way to document the behavior
of a function to developers, and you can see that examples of that after the
words `describe`. For example, the next word `describe` is followed by the word
`companyName` name. Here the test is telling us that the tests that come after
words will be about `companyName`. Then comes the word `it`, where you see the
following:

```js
it('is set as Scuber', function () {
  // tests are here
});
```

So this is telling us that the `companyName` should be set to `Scuber`. Finally,
filling in the missing part of the `it` code, we see:

```js
it('is set as Scuber', function () {
  expect(companyName).to.equal('Scuber');
});
```

Here, we can see that it expects `companyName` to equal `Scuber`. That `expect`
and `to.equal` are essentially doing the same thing as `companyName ==
'Scuber'`. In other words, `expect(companyName).to.equal('Scuber')` is running
code that will have this first test pass if `companyName` equals `Scuber` and
fail if it does not.

Don't worry too much yet if it's hard to understand what is happening inside of
the `test/indexTest.js` file. But it's a good idea to open up the file, and
gather the information that you can. We will also provide instructions in the
`README.md` file that will allow you to complete the lab (as we do in this lab
below).

## Running the tests

To run the tests, simply type `learn` in the terminal part of the Learn IDE.
(The terminal is the part below where you've been coding.)

As mentioned, running the `learn` command will open up a new tab on your browser
or provide a link in your console to an IP address, showing the current status
of the tests. For the moment, all of the tests fail. Let's figure out how to get
one of them passing! (The rest will be up to you.)

To get our first test to pass, we can open up our `index.js` file, and write the
following:

```js
let companyName = 'Scuber';
```

Great, our first test is now passing. Except the second test is also about
`companyName` and it is not. It's not passing because, it expects a change to
`companyName` to throw a `TypeError`. It sounds like it wants `companyName` to
be declared using a different keyword than the `let` keyword - it needs a
keyword that is used for variables that can't be changed...

Ok, so we'll let you work through the problems below. But in summary here is
your workflow for a lab:

1. Run `learn`.

2. Read the errors; vocalize what they're asking you to do.

3. Write code; repeat steps 1 and 2 often until a test passes.

4. Repeat as needed for further tests.

5. Run `learn submit` when finished!

## Working Through the Problems

If you open up `test/indexTest.js`, you will see the tasks in front of you:

+ `companyName` - Inside the `test/indexTest.js` file, look inside of the word
`describe` where the tests are trying to indicate that this test is describing
the `companyName` variable. The `it` word that comes afterwards, tells us the
features of `companyName`. In the first `it` function call, it says that `it`
(companyName) `is set as Scuber`. In the next line, you can see that the test
checks to make sure this occurs by seeing if `companyName` equals `Scuber`. So
this means that you need to go to your `index.js` file and declare a variable
named `companyName` and set it equal to `Scuber`. Once you do that, if `learn`
is running, you will see the first test in this lab as passing.

In the next `it` function call, we are still describing `companyName`. This
time, it says it `raises error if the companyName is changed`. The next line of
code tests this. It's ok if some of the code in that line is confusing. Just
know that the code attempts to change `companyName` to a different value, and
that this reassignment should throw an error. So you need to make sure that you
are using the correct type of variable declaration such that attempting to
reassign the variable throws an error.

+ `mostProfitableNeighborhood` - Here we need to declare another variable,
`mostProfitableNeighborhood` and assign to it the string `'Chelsea'`. In the
next `it` function call, you can see that our tests ensure that
`mostProfitableNeighborhood` does not throw an error when reassigned. So you
need to make sure that you are using the correct type of variable declaration
such that assigning a new value to `mostProfitableNeighborhood` doesn't throw an
error.

+ `companyCeo` - Here, we are getting more practice with declaring variables.
Once again, a reassignment should not throw an error.

## Resources

- [MDN: Let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
- [MDN: Const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
