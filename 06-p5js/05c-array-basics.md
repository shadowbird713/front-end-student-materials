# Arrays and Iteration

Most of the time, we interact with lists of things without even recognizing it. Accessing contact lists when we send texts, reading the chapters in a book, or watching a series of Snapchat stories are just a few examples. 

Any time we encounter a list, we do things in an ordered sequence. Going over each item in a list is called **iteration** and is a topic we'll discuss often in computer programming.

Let's examine a few examples and discuss how we can represent these processes in code.

![cat reading](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/cat-reading.gif)

Reading, might be one. It's happening so fast, but really you are looking at the first word, then the second, then the third, and so on. You keep doing this until the paragraph, book, tweet or whatever group of words you are looking at is finished.

Another might be your school day. You go to your first period class, and then second period, then third period, etc.  Your schedule, a list of what classes you have when, determines that first period is english, second is math and so on.

Or maybe you make to-do lists either in your head or on paper.  You **loop** over the list and check off a task if it's completed. Applying an action to an item in a list is known as **iteration**. 

What these all have in common is that in each case we are *looping through* a **list** of things.

As programmers, the way we represent lists of things, that is to say *groups* or *collections* of *elements* that have an **order** (first, second, third...), is with **Arrays**.

## Array Basics

The most important thing to know about Arrays is that htey *have an order*. Think: something we could loop through.

## Order (What's an Index)

Watch how an array is created, and then we'll break it down.

![create an array](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/create-array.gif)

As you can see to make an array you use square brackets and inside you put the items that make up the list separated by commas. Here's an example:

```javascript
var testScores = [89, 91, 95, 86, 79]
var students = ["Jasmine", "Edward", "Andre", "Maria"]
```

### Accessing Values

To get, or access, an item in arrays, We can ask what *position* we want to get the value of.

The number of the position within the array is called the **index** of the array.

We get the value at a certain index using square brackets written after the name of the array, like so:

```javascript
students[index]
```

Here's a list of countries from around the world:

```javascript
var countries = ["Algeria", "Brazil", "Canada", "Denmark"]
```

You might guess that writing `countries[1];` would give us back "Algeria" because it's the first item, or element, in the array.

Let's take a look

![index 1](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/index-1.gif)

Huh??? Last I checked `"Brazil"` was the *second* country in the list...

![wat](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/wat.png)

Before you put on your Darth Vader costume and grab the nearest Brita filter, watch this:

![indices](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/indices.gif)

Ooooo, we just learned something really important about arrays. The indexes **start at `0`**.  

Index `0` is the first element of the array, index `1` is the second, index `2` is the third and so on.

This also means the *last index* of any array is always *one less* than the total number of items in the array. The highest index in an array with 100 items would be `99`. Which brings us to the next array property, `length`.

## `length`

We can find out the length of any array by adding `.length` to the end of the array.

![length](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/length.gif)

Think about `for` loops for a moment, where might the `length` property be useful??

We'll get to that soon enough :)

## Manipulating Arrays with Functions
What are some of things, conceptually, you could do to a list?

Maybe add things to it, at the end or at the beginning, or remove things from it. Arrays have functions to do just that!

### `push()`

`push` adds a new element to the end of an array. Think of it as 'pushing' onto the end.

![push](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/push.gif)

It's a function so it takes an argument of the new element to add.

### `pop()`

`pop` is the opposite of `push`. It **removes** the last element of an array, whatever it is. It doesn't need any arguments but we can't forget to put the parentheses `()`.

![pop](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/pop.gif)

### `unshift()`

`unshift` adds an element to the *beginning* of an array. It's like the opposite of `push`.

Let's say we forgot to add the country starting with `'A'`. Unshift to the rescue!

![unshift](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/unshift.gif)

### `shift()`
`shift` is the opposite of `unshift`. It **removes** the first element of an array. Like `pop` no arguments are needed.

![shift](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/shift.gif)

### `splice()`

`splice` is used to remove elements from arrays at *any index*, it's a little bit trickier because it needs two arguments.

The first argument is the *index* where to start removing and the second argument is *how many elements to remove*.

![splice](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/splice.gif)

Bye Canada 🇨🇦 😢

## Mini-Challenge

That was a whirlwind introduction to Arrays, complete the exercises below then we'll move on to using arrays and loops in our bubble example.

To get some more practice with Arrays let's do this in the Chrome console. Copy this code which initializes a new array.

```javascript
var line = ["Armand", "Bianca", "Cecilia", "Dillon"]
```

The array represents a line at the grocery store. Translate the following series of events into code. Run the code in the console and at the end we'll check to see if your `line` looks right!

- Armand, the first in line, checks out (he should be removed from the front of the line)
- Evelyn joins the end of the line (don't forget the quotes around her name)
- While Bianca is searching for her Shopper's Club Card, Dillon remembers he forgot to buy Salsa and leaves the line.
- Farah and then Georgio join the line.
- Bianca and the next customer check out
- Actually, Bianca left her card at register and cuts to the front to grab it
- Hakim joins the end of the line
- Seems like Bianca will be a while, Hakim leaves the line and goes to another register

### Questions
*(Answers at the bottom)*

1. What is `line.length`?

2. What is the name of the second person in line? Write the code to access their name.

3. What is the name of the last person in the line? Write the code to access their name.

## Resources

- [JS Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [`push()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
- [`pop()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
- [`splice()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
- [`shift()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
- [`unshift()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)

## Answers

```
1 - 4
2 - "Evelyn" line[1]
3 - "Georgio" line[3] OR line[line.length - 1]
```
