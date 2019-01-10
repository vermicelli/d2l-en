
Until recently, nearly all of the computer programs
thay we interacted with every day were those
that we could code up from first principles.
Say that we wanted to write an application to manage an e-commerce platform.
After huddling around a whiteboard for a few hours to ponder the problem,
we could come up with the broad strokes of a working solution.
It would likely look somehting like this:
the core application would interact with a relational database and an interface.
The database would store all relevant data
about our customers, inventory and transactions.
Customers would select actions via their interactions with the interface.



<!--
We'd likely maintain
tables to represent each of the businesses primary entities:
customers,
products, orders, and associative entities like shopping carts.-->

We could step
through each use case that we'd be likely to encounter,
and write up the
appropriate business logic.
Each time a customer clicks to add an item to their
shopping cart,
we add an entry to the shopping cart database table,
associating
that user's ID with the requested product’s ID.
While it might take a few test
runs to work out all the kinks,
for the most part, we could write such a
program from first principles
and confidently launch it before ever seeing a
real customer.
When it's this easy to write an application *you should not be
using machine learning*.

Fortunately—for the community of ML scientists—for
many problems, solutions aren’t so easy.
Take for example the burgeoning
industry of personal assistants
that run in most smartphones and home speakers,
(think Amazon Echo, Google Home, Apple HomePod, etc).
The first step in any
interaction with these devices typically
involves triggering them with a "wake
word" like “Alexa”, “Okay, Google” or “Siri”.


![Estimating the length of a
foot](../img/wake-word.png)

Before we worry about any of the more advanced
functionality of these sytems,
just imagine trying to code up a program to
recognize the *wake word*
in a room by yourself with nothing but a computer and
a code editor.
How would you write such a program from first principles?
Think
about it. This is *not* a trick question. It's a hard problem.

Every second,
the microphone collects roughly 44,000 samples.
What simple rule can reliably
map distinguish whether snippet of raw audio
contains the wake word vs. any of
the nearly infinite other audio patterns?
If you’re stuck, don’t worry.
We
don’t know how to write such a program from scratch either.
That’s why we use
machine learning.


Here’s the high level idea: Often, even when we don’t know
how
to tell a computer explicitly how to map from inputs to outputs,
we are
nonetheless capable of performing the cognitive feat ourselves.
In other words,
even if we don’t know how to program a computer
to recognize the word “Alexa”,
we ourselves are able to recognize the word “Alexa”.
Armed with this ability,
we can collect a huge *dataset* containing examples of audio
and label those
that do and that do not contain the wake word.

In the machine learning
approach, we do not attempt straight away
to design a system explicitly for
recognizing wake words.
Instead, we define a flexible program called a model.
This book focuses on *deep learning*, an approach in which
the model's behavior
is defined by a large number of parameters.
These are knobs that we can tune to
change the behavior of the program.
Using our dataset
