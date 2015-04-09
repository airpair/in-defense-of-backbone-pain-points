Let me explain myself first. I like to build stuff out of wood and other materials as a hobby. More on that in a bit.

In 2012 I had the opportunity to choose between Angular, Backbone, and Ember. I chose Backbone for one, very naive, reason: I wanted less black magic and more control.

Today, I'm still thankful I made that decision.

When I discovered jQuery many many many years ago, it changed everything. I could build these little dinky scripts so much faster. Things worked on multiple browsers on the first try (for the most part, dang you IE6!!!). I learned how to use jQuery UI and create plugins that could do ANYTHING I wanted. The scripts got bigger, and eventually I was creating these tiny applications. I felt legit. I felt invincible.

Eventually the web apps started requiring actual computer-science-y stuff. The amount of 'data' (DOM nodes) I was processing started causing my "apps" to perform poorly. I would see other applications that just felt... better. Faster. More reliable.

I could build ANYTHING using jQuery, but my code was starting to have fewer and fewer lines that were relevant to anything jQuery handled. I had become a jQuery developer, I had learned the ins and outs of jQuery, but I thought I knew JavaScript.

I didn't know JavaScript. I was just starting to learn, and it was breaking up my marriage to jQuery.

Fast-forward some undisclosed and forgettable amount of time, enter Backbone. All of a sudden I have these objects that provide a little structure to what I'm doing, but they didn't beat me over the head w/ an opinion. It let me do things how I wanted, it helped me learn what I was doing wrong. I was able to pick and choose various pieces of my application based on the requirements. I could have this awesome foundation, regardless of the project, and build out whatever made the most sense. I was able to _research and learn_ about the tools and plugins and widgets I was implementing. I was able to grow. _I actually learned JavaScript_.

Let's go back to that "wood hobby" I mentioned. jQuery for me was a swiss army knife. You can do a lot with a multi-functional tool. You can use a screwdriver part to pry open a paint can, you can use the butt of the knife as a hammer, you can do all kinds of stuff the way you're actually suppsed to (like, using a screwdriver for screws). When I chose Backbone, it was like I was saying without knowing it...

"I'm going to start learning how tools work and then start using them. I'm going to buy a hammer. I'm going to buy a scrwedriver. I'm going to also buy a drill because the screwdriver takes too long. But sometimes, I'll still use the screwdriver. Wow, look, I can actually build my own CNC machine and other tools USING MY EXISTING TOOLS because I know how everything works!"

You learn so much from actually USING the tools, holding them in your hands, building things with them. _Somebody needs to know how to use the tools_.

Let's get back to technology.

Backbone is not the best solution every time. Nothing is. I spoke w/ the principal front-end whatevs dude from Yahoo a few months ago, asking what they were going to do since they dumped YUI and he said "Ember." I was really surprised until he said "I can't afford to have 1,000 front end engineers having 1,000 opinions about something." Makes sense. Ember has a strong opinion. I approve of this decision.

What if you have a team of back-end engineers (engirears? get it? no? okay.) who need the client-side app to function, but they don't want to spend all day in JavaScript land? Maybe they want to specify some (weird) `ng-whatevs` attributes on the HTML they're already sending to the client and watch the fireworks display when it all works together. Hey, Angular is a great solution for that. "IT EVEN HAS (forces?) TWO-WAY DATA BINDING! WOOOT!"

What if you want to actually learn JavaScript? Perhaps you should consider Backbone. But then, if you're considering Backbone, you're going to read about some of the pain points...
## Commonly mentioned "Pain Points"

"Backbone lacks support for two-way data binding, meaning you will have to write a lot of boilerplate to update the view whenever your model changes, and to update your model whenever the view changes."

"Views in Backbone manipulate the DOM directly, making them really hard to unit-test, more fragile and less reusable."

"There is a lot of boilerplate."
## OMGoodness come on!

Those are ridiculous statements. Let me make a couple of other, equally (and I promise, they are equal) ridiculous and not exactly accurate statements:

* All rectangles are squares
* All marriages end in divorce
* All event listeners set in jQuery are done using `$(selector).bind()`
* If you EVER write a line of code twice you DO NOT understand what DRY means and you are a bad developer and you should feel bad
* Two-way data binding is ALWAYS good and ALWAYS the best solution

Those statements are ridiculous, because they are only sometimes true. Some rectangles are squares. Some marriages last until death. Some event listeners in jquery are set with `on()` (don't use `bind()`, please). Sometimes you write a line of code twice, realize it, and refactor to make it DRY. And then there's two-way data binding...

## Refuting "Backbone Pain Points"

Two-way data binding is great. It solves a problem. It is one way to solve a problem. It does not solve every problem. In some circumstances at scale it actually IS a problem. So there's that.

To say "Backbone lacks support" for it is making the assumption that you NEED it every time, all the time, and you're missing out. I hear that type of stuff in commercials.

To say "Backbone lacks support" for it is making the assumption that Backbone lacks support for it. No it doesn't, it just doesn't come in the box. Build it yourself, learn how it works, so that when you're pulling your hair out trying to figure out why your magical "two-way data binding" supporting library isn't working like you think it should, you can fix the problem. (side note: building it yourself involved about... I don't know, 20 lines of code or so... and it's used everywhere I want it to be in my Backbone app, when I want it and when it makes sense.)

To say "Backbone views manipulate the DOM directly... hard to unit test... fragile... less reusable..." is flat out alien to what I've experienced. It's so easy to write unit tests for Backbone views! The view methods are right there to be unit tested! This argument MUST be talking about the template layer, which if you use Backbone, is up to you to define (check out React for amazing experiences). And even then, that's an integration test, not really a unit test... but I digress. Actually, I think I digress. I'm not 100% certain what digress means. But I digress.

Backbone views don't manipulate the DOM unless you tell them to. `Backbone.View.prototype.render()` is a noop that you have to define yourself, so... if you're manipulating the DOM, that's on you. Also, Backbone views are very testable unless you write them in some crazy way that isn't testable. Don't recommend you doing that.

To say "there is a lot of boilerplate with Backbone..." COME ON! You're (hopefully) an engineer! Or at least learning to be one! When you end up writing boilerplate, use your engineeringified brain to figure out a solution! It may actually be useful for you to see some boilerplate so that you can come up w/ a really good solution to fix it. Maybe the solution is Angular? Maybe it's something else? But knowing HOW something works, WHY it works, WHERE to improve it... is that not what makes us tick?

## Le conclusion

All of the frameworks out there right now have great support, great contributions, tons of thought, active development, communities, examples, best practices, etc. They're all really good at solving some very real, very big problems. Some of them solve more problems than others. I think they're all great.

I don't like all of them. I really like Backbone. I really like React. I really like how the Flux architecture works. I like building on to Backbone with really interesting things like `Schemar` (which I hope to open-source one day). I like using jQuery sometimes. I like to build wood projects. I like to learn.

_And I really, really, really love to coach._

\- Brian Blocker

## Code examples

Some code to back-up some of my arguments.

```javascript

```
