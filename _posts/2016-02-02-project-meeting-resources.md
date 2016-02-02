---
layout: post
title:  "First Project Meeting Resources"
date:   2016-02-02
author: Raphael
category: feed
tags: [feed]
---

Hey, everyone! We have a lot to do in tonight's project meeting.

### Today's project: n-Grams Markov Chains

Beacuse we haven't had a proper lecture session this semester yet, so I thought we could use this meeting to make something simple that can be finished tonight.
What better "warm-up" project than a Markov Chain? We talked quite a bit about NLP last semester, so we can put that knowledge to good use!

Markov Chains are a very simple data structure that are capable of generating a sequence based on probability.
For instance, suppose you just read the letter 'a', 'g', 'e', 'n'. Your brain knows that there's a good chance the next letter is a 'c', then a 'y'.
Similarly, Markov Chains learn these probabilities from a corpus of text, and keep them stored, so they know that, if the current letter is 'n', the probability of 'c' is 0.3, and of 'a' is 0.2, etc.

![An example of Markov Chains](http://guizzetti.ca/blogs/lenny/wp-content/uploads/2012/04/3state_markov.jpg)

The cool part is that we can use MCs to generate text: given the letter 'g', take a sample from the probability distribution of next letters.
If this prediction is the letter 'e', ask what letter it will predict given that it just saw 'e'. Then, if is says the letter 'n', ask what the next one will be, and so on ad infinitum.
This is called a "random walk". "Random" because the prediction is random (but follows the probability distribution).
If you didn't know, btw, this is how [SubredditSimulator](https://www.reddit.com/r/subredditsimulator) works.

An nGram Markov Chain is a Markov Chain like any other, except each 'state', is composed of multiple letters (or *tokens*, which can be words too).
So instead of asking "what letter will come after this the letter 'e'?", you ask, "what letter will come after age?", then if it predicts 'n', ask what letter comes after 'gen', etc. (this example is a 3-Gram Chain).

I know this is a lot of information for a short post, but don't worry too much about the details. We're here to learn by doing!
If you want to read more about it in advance, though, you can [start here](http://www.onthelambda.com/2014/02/20/how-to-fake-a-sophisticated-knowledge-of-wine-with-markov-chains/) and [here](http://setosa.io/blog/2014/07/26/markov-chains/).

I set up a [repo](https://github.com/gtagency/warmup-markov-chains) for us to play with, already with a [corpus](http://lexically.net/wordsmith/support/shakespeare.html) of text for us to train the Markov Chain with.
Later on, we can use other corpora for generating text. Maybe even call reddit's API and make our own SubredditSimulator!

### Getting everyone set up

Guys, we want to be able to reach out to everyone. So please join the [email list](https://docs.google.com/forms/d/1SqYfolQ_c_e_gNINMtI1DxQhLzIC_y_ff_bqt7e5LNo/viewform?c=0&w=1). We will also discuss whether we want to set up a slack. It's a great way group chat service!
As always, you can get the latest announcements on the [feed](http://gtagency.github.io/Feed), or on [facebook](https://facebook.com/gtagency). We also have a [twitter](https://twitter.com/theagencygt) and [instagram](https://instagram.com/theagencygt) for bragging about the cool stuff we do.

A lot of people in the club were here last semester, but we have a number of new people and we need to get them set up.
This means that while some of you will be working on Markov Chains, the rest can get a quick crash course on git/github!

If you don't already have git, please [install it](http://git-scm.com/).

If you want to learn more about how git/github works, I suggest reading [this]().

Finally, we have a lot of cool talks planned for this semester, including some on Deep Learning using tensorflow. So I highly recomment everyone to [install python](https://www.python.org/downloads/) if you haven't already and get familiar with it (looking at you, java team). [Here's](https://www.python.org/about/gettingstarted/) a great intro to the language. 

### Decisions...

The last thing we have to discuss is the main project for this semester. We heard a lot of good ideas last meeting, so I wanted to ask you guys for your final preferences. If you have any ideas, you can still send them [here](https://docs.google.com/forms/d/1PgGHrPelmNhcaUKDKd-XraBcs2uT9bezC54MgqYHYBQ/viewform?c=0&w=1).
Hopefully we can decide on this soon :)
