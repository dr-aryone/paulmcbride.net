---
path: "/pure-functions-functional-programming-javascript"
date: "2017-11-30T09:00:00.000Z"
title: "Pure Functions – Functional Programming in JavaScript"
featuredImage: "./images/pure-functions.jpg"
tags: ["javascript", "tools", "screencast", "code"]
---

In this episode of Functional Programming in JavaScript, we discuss pure functions.

You probably already use pure functions all the time and are unaware of what they are or what advantages they bring to your code base. Watch the video below to find out why pure functions are better and much more.

---

## Pure Functions - Functional Programming in JavaScript

`youtube: Jh_Uzqzz_wM`

---

## Video Transcript

Hello, my name is Paul McBride and you're watching this series on functional programming in JavaScript. This is the fourth episode in this series so if you've not even any the previous ones, you'll be able to find a link to them up here.

In this episode, we're gonna be talking about pure functions what they are and how to use them. So what is a pure function? For a function to be considered pure it has to follow two simple rules.

The first one is that it has to be deterministic. That means that given the same inputs it will always return the same output. Let's take a look at an example of a few deterministic and a few non-deterministic functions.

Okay, so in this example, we have a deterministic function. No matter how many times we call the square function if we pass in the same value we'll get the same result. So if we pass in 3 we will get 9 every single time we call that function. Now let's take a look at a non-deterministic function. This is one I wrote earlier I'm gonna paste it in. This function, similar the last one takes a number is an argument and multiplies it by a random number between 1 and 10.

Now, every time we call this function we have no way to guarantee what the value is going to be. This is a non-deterministic function. This is obviously a very simple example of what one is and there are more complicated more real-life scenarios, for example, a function which connects to an API or speaks to a database is a non-deterministic function because we can't guarantee the results of what they're going to return. The database might fail or the server that you're connecting to might not be online.

The second rule that pure functions must follow is that they can't have side-effects. Now, what this means is that a pure function isn't allowed to alter variables outside of its own scope. If the variable isn't passed in, the function shouldn't know about it and shouldn't operate on it in any way. Let's have a look at an example of what that means.

So here we have an example of an impure function. We have an array of animals here cat, dog and fish. We have a function which pushes a new animal into an array and then on line 8 we're calling that function and we're going to print out the results. We print out the new animals first and then the original animals.

Alright, as I said, this is an impure function. It has a side effect and it's probably not immediately obvious. So let's run the code and see what we get. They're both the same. What!? Essentially what's happening here is that this push function has side effects. It affects the original array. It doesn't create a new one and return a new value.

Let's have a look instead of how we could do this in a way that is pure and doesn't have any side effects. In this example, I've altered the code very slightly on line four. Instead of using `array.push` to add the horse into the new array, we're using the spread syntax. We create a new array, we add the animal, in this case, a horse to the start of that and then, we use spread to pluck each item out of this animals array and place it into this new array that we're returning.

So if we run this code we should find that the original animals array is no longer changed and the new animals array has horse pushed in. So, let's run that and see what we get. Awesome! So, as we've seen there, original animals remains unchanged.

Now that we know what pure functions are let's discuss a little bit about why we would use them and what kind of benefits they bring to your code base.

The first benefit is that pure functions are incredibly easy to reason about. It's easy to understand what the function does and given a certain set of inputs you'll always get the same result. This means that those functions can be passed around your application, used in different parts for that every whirring that it doesn't have a particular bit of state in your app somewhere that it needs to work properly.

Another advantage of pure functions is that they're really easy to test because pure functions don't rely on external state variables it's easy to mock up every part of what that function does.

Javascript is a multi-paradigm programming language. What this means is that it can be used for different programming approaches including functional programming or object-oriented programming in several other different types. As a result, it's not perfect at any one. When you're writing functional JavaScript there are a few gotchas you have to be aware of such as the push on the array object. There are a lot more. They're pretty easy to find online. So, there are just things you need to be aware of if you're trying to write functional code in JavaScript.

That brings us to the end of this episode of functional programming in JavaScript. Hopefully, you understand a little bit better about what pure functions are and how they fit into functional programming. If you have any questions get in touch with me I'll do my best answer. If you've enjoyed this episode then please feel free to subscribe to my channel or sign up to my email list and I will see you in the next episode.

Bye!
