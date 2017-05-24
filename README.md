## Front Trends 2017
### May 24 - 26, Warsaw
My notes on [Front-Trends 2017](https://2017.front-trends.com/). Don't mind any spelling mistakes, and any potential misinterpretations are all mine :)

------------------------------------

**DAY ONE**
* [MACIEJ CEGŁOWSKI: Legends of the Ancient Web](#maciej) *The future of the web*
* [UNA KRAVETS: The Power of CSS](#una) *HTML, CSS*
* [VITALY FRIEDMAN: Smashing Magazine’s 2017 Relaunch](#vitaly) *Responsive design/HTML, CSS, UX*
* [SAM BELLEN: I didn't know the browser could do that!](#sam) *Browsers, APIs*
* [ADAM MORSE: The past and future of designing interfaces](#adam) *CSS*
* [MARCO CEDARO: Components, patterns and sh*t it’s hard to deal with](#marco) *Patterns*
* [STEFAN JUDIS: Watch your back, Browser! You're being observed.](#stefan) *Browsers, APIs*
* [ALLY LONG: Field-tested interfaces for the next billion](#ally) *UX*
* [NIELS LEENHEER: Monsters, mailboxes and other nonsense](#niels) *IoT*

**DAY TWO**
* [PATRICK HAMANN: The First Meaningful Paint](#patrick) *Performance*
* [ZOE MICKLEY GILLENWATER: Experimenting your way to a better product](#zoe) *A/B testing*
* [ADIM MAKEEV: I'm in IoT](#vadim) *IoT, APIs*
* [VAL HEAD: Motion In Design Systems: Animation, Style Guides, and the Design Process](#val) *Animation*
* [KIRUPA CHINNATHAMBI: Building a Progressive Web App](#kirupa) *PWAs*
* [LIN CLARK: A Cartoon Intro to React Fiber](#lin) *React*
* [JACK FRANKLIN: The How, What and Why of migrating to ReactJS](#) *React*
* [MIHAI CERNUSCA: Prevent Default — The future of authoring tools](#) *UX, mark-up, future of the web*

**DAY THREE**
* [KONRAD DZWINEL: Alternative Reality DevTools](#konrad) *Devtools*
* [OLA GASIDLO: Let's save the internet: How to make browsers compatible with the web](#ola) *Browsers*
* [IDA AALEN: Easy and affordable user-testing](#ida) *UX, testing*
* [MARTIN SPLITT: Rendering performance inside out](#martin) *Performance*
* [JENNA ZEIGEN: On How Your Brain is Conspiring Against You Making Good Software](#jenna) *Humans*
* [CHRIS WRIGHT: Changing the layout game](#chris) *HTML, CSS*
* [ROSIE CAMPBELL: Demystifying Deep Neural Networks](#rosie) *Machine learning*
* [PHIL HAWKSWORTH: Microservices - The FAAS and the Furious](#socks) *Microservices*


<a name="maciej"></a>
# Maciej Cegłowski: Legends of the ancient web

Let's reach into the past to see if we can find any insights. What has been will be again, there is nothing new under the sun. In the last couple of years, frontend development has become very complex: there are lots of technologies and frameworks to master. Computers move fast. It's happened before, and will happen again. It happens in backend too: what about virtual machines?

Maciej feels like standards have slipped a little: it's normal on the web things are as fast now as they were 10 years ago, it's normal that a web page is like 2mb. A render time of a second is acceptable, rather than instantaneously. Brittle and bloated sorcery: users haven't seen snappy websites in a long time, and this might actually be what they want.

Of course, the former generations don't tell the newer generations this happens again and again. Our generation will forget too. So let's talk about the web that came before the web. The internet is a powerful force that comes into your private home. And it's occupied by big business, just like radio. But just like the radio, the internet brings people closer. The idea that is hard to accept for us is that people that try to build good things, end up making stuff that ultimately ends up being used for evil. Think of the Rwanda genocide: those that created the radio could not foresee their invention being used to incite violence and genocide. Technology and human nature interact in interesting ways. It is very possible the things we build may be used for bad later on. This is a threat, and we need to take it seriously.

So many cool things are happening: AR, VR, and AI. But how is Google's AI trained? By mass surveillance. "Okay Goebbels". Our radios don't just talk anymore, they also listen and learn. They deliver targeted messages that we'll find persuasive. We can't unbuild the internet, but we can decide not to pay to spy on eachother.

Big takeaway: what you're working on, and who you're working for is very important. It's not about frameworks and libraries, it's about the direction the internet is taking. We need to learn from the history of radio and how it was used for evil, and try not to repeat these mistakes. This doesn't mean we have to stop being nerds, the utopian qualities of the internet are still there and can still be defended. But there is a fight going on. We have to make sure the powerful don't feel comfortable using our tools. Understanding people through alghoritms is dystopian, not utopian. We're pioneers in a field that changing the world, and the decisions that we make matter. We're not just tech workers, we're human beings.

<a name="una"></a>
# Una Kravets: The Power of CSS
Using CSS as a design tool. A lot of engineers have an aversion to CSS, which is partially based on frustration. They think you're not a real dev if you just write CSS and HTML. You can do amazing things with CSS though (plus it's Turing complete). You can use filter values to edit photos, just like in Photoshop. If you apply blend-modes on top of them, they get even more powerful. Like PS, you have Luminosity, Screen, Difference..(my note: Spotify does this well). You might just not need JS either. You can make an accordion with just HTML and CSS, using input labels (accessibility?) and adjacent sibling selectors. Tab groups are another element/component that you don't need JS for -- you can use radio buttons (since only one of them can be open at the same time).

Modals, lightboxes, tooltips, scroll indicators, carousels don't need JS either. Target, data attributes, siblings- and pseudo-selectors are very powerful.

These are still all kinda hacky and not completely W3C compliant. They might be bad for performance too. A CSS modal cannot be focused on. And if the content inside it is important, you'll want to use the ESC key to close it, which you can't do without JS. These things are great for prototyping, but using them in production has its specific issues. With great power comes great responsibility, and the real power of CSS is that it creates a common language for designers and developers (note: in an ideal world..). But: always test for accessibility, performance, and browser support.

CSS Grid is so hot right now <3 you can always use flexbox as a fall-back.

(Things to look up: content editable. Reload code on the fly? Diffee.me. Youmightnotneedjs.com)

<a name="vitaly"></a>
# Vitaly Friedman: Smashing Magazine's 2017 Relaunch
Lessons learned when redesigning Smashing Magazine (SM). SM was losing lots of revenue because of ad-blocking. Now, they've replaced membership for ad revenue, brought more focus to their paid products (books). Another impetus for the redesign was to unify the platform behind SM. It's a magazine, a CMS, a job board, an ecommmerce platform, et cetera. It was hard to see the big picture behind all these components. It took a lot of research.

We're too tied in to media queries. Defining the scope of breakpoints is almost impossible considering the huge amounts of devices and viewport sizes possible. You can't be sure your media queries cover everything. Avoid them as much as possible in the design process.

How do you scale up/down a UI component in an efficient way, without fiddling with width and height, and still keep proportions intact? Use rem for root components, and em for sub-parts. Then, by adjusting the font-size of the root, we adjust all size-related CSS properties of a component at once. Curves instead of straight lines. y = mx + b helps you avoid media queries. Plug your min and max font sizes in and the formula takes care of the rest (you can use px too).

Fluid behavior should also be able to be turned off, like in a fixed environment. That's all possible too.

(Things to look up: fluid sizing)

<a name="sam"></a>
# Sam Bellen: I didn't know the browser could do that!
Most of these APIs are supported in Chrome and partially in other browsers.

Speech API: the browser can also talk to you by converting text to spoken words. You need internet access for this, but setting up speech-recognition is not that hard. Other less well-known APIs are geolocation and notifications. Notifications need permission, and you can attach click handles to it. Another API is the Push API, which is sent from a backend (push) server, whereas notifications are sent from the frontend. Even if you're not on the website that pushes the notification, using the Push API, it can still push messages. Your window does not need to be open. A push notification needs a service worker. Once that's registered, you can subscribe to the pushManager and send the subscription to your push server. The service worker will then listen to push events, and do a bunch of things when one comes in.

Next one: the battery manager API. A web browser can get your battery's data! It can show data, and notify you when that data changes (for instance, when you unplug your charger).

Another cool one: the media recorder API. It records audio or video using your laptop's internal tools with just a few lines of JS.

By combining these APIs you can actually build your own little Siri. Using Tracking.js you can also kinda make Snapchat filters 😱 Note to self: do something with this!

<a name="adam"></a>
# Adam Morse: The past and future of designing interfaces
Very interesting, hard to summarize. Watch the video!

TL;DW: data is difficult and humans tend to make a lot of mistakes when working with data. We're not too good at it. A possible line of defense is modularity: breaking down a complex thin into understandable things might just help us avoid errors.

A simple component can have thousands of states. And that's what computers should be for: see these states. That's not a human task. Seeing and testing all possible states of components would make any developer's life easier.

<a name="marco"></a>
# Marco Cedaro: Components, patterns and sh*t it’s hard to deal with
Modular architecture, classes, components, modifiers, overrides -- it's a lot to deal with. Everyone has their own mental model of things. We've not been applying pattern libraries as a technique for a very long time in web development. When React was first released, most of us started building things in a modular way. But we're still struggling. When you actually try to apply a modular approach to your day to day work, it isn't simple -- not for design or development. It's like fitting a square peg in a round hole.

So what is a pattern library here? A common language to cross cultural boundaries. It contains all visual elements which can be swapped seamlessly. Note: this definition differs for everyone. But how do we manage our code without making them too rigid for day to day use? Tweaks and changes are a fact of life, and pattern libraries don't embrace this necessarily. It becomes a cage rather than a tool.

It's about modularity at its core, it's about modules' responsibilities, and about maintainability of the code. How do we re-use our patterns in slightly different cases? First, think about what problem you're trying to solve. Why the small change? How do we convey the meaning of an exception in our pattern library? Get involved early, talk to people (designers, PMs, not just devs), and remember that it's still a human problem and not hopeless.

<a name="stefan"></a>
# Stefan Judis: Watch your back, Browser! You're being observed.
Notes go here :D

<a name="niels"></a>
# Niels Leenheer: Monsters, mailboxes and other nonsense
Notes go here :D

<a name="ally"></a>
# Ally Long: Field-tested interfaces for the next billion


<a name="patrick"></a>
# Patrick Hamann: The First Meaningful Paint
Notes go here :D

<a name="zoe"></a>
# Zoe Mickley Gillenwater: Experimenting your way to a better product
Notes go here :D

<a name="adim"></a>
# Adim Makeev: I'm in IoT
Notes go here :D

<a name="val"></a>
# Val Head: Motion In Design Systems: Animation, Style Guides, and the Design Process
Notes go here :D

<a name="kirupa"></a>
# Kirupa Chinnathambi: Building a Progressive Web App
Notes go here :D

<a name="lin"></a>
# Lin Clark: A Cartoon Intro to React Fiber
Notes go here :D

<a name="jack"></a>
# Jack Franklin: The How, What and Why of migrating to ReactJS
Notes go here :D

<a name="mihai"></a>
# Mihai Cernusca: Prevent Default — The future of authoring tools
Notes go here :D

<a name="konrad"></a>
# Konrad Dzwinel: Alternative Reality DevTools
Notes go here :D

<a name="ola"></a>
# Ola Gasidlo: Let's save the internet: How to make browsers compatible with the web
Notes go here :D

<a name="ida"></a>
# Ida Aalen: Easy and affordable user-testing
Notes go here :D

<a name="martin"></a>
# Martin Splitt: Rendering performance inside out
Notes go here :D

<a name="jenna"></a>
# Jenna Zeigen: On How Your Brain is Conspiring Against You Making Good Software
Notes go here :D

<a name="chris"></a>
# Chris Wright: Changing the layout game
Notes go here :D

<a name="rosie"></a>
# Rosie Campbell: Demystifying Deep Neural Networks
Notes go here :D

<a name="socks"></a>
# Phil Hawksworth: Microservices - The FAAS and the Furious
Notes go here :D
