---
layout: post
title:  "Building Realtime Web Apps"
date:   2015-05-26
author: james_moore
---

<iframe width="630" height="354" src="https://www.youtube.com/embed/ZwyjDiikNKk"
frameborder="0" allowfullscreen></iframe>

In this tutorial screencast we’ll look at creating realtime web applications.

Creating realtime web applications has been possible for a while now, however up
until recently it’s been kind of a pain and required a big engineering effort.

I think this is largely because the tools haven’t provided exactly what we
needed to do realtime in a simple and painless way.

Luckily this has all changed, now it’s pretty easy to build realtime
applications and it’s my goal to prove that to you in this episode.

The best way to prove this is by showing you, so we’ll build a simple single
page application the uses realtime features from top to bottom.

The app we’ll build is a realtime question & feedback application that could be
used at a meetup. For example when people at the meetup have a question, they
could post their question and it would be immediately streamed to everyone using
the app.

At it’s core it’s just a simple crud application, except all interactions happen
in realtime.

Here is the technology stack we’ll use:

RethinkDB as our database
Node.js or IO.js server platform
Koajs a cool Node.js web framework
Socket.io a library for bi-directional communication between the server and the
client
AngularJs as our client side javascript framework
Let’s briefly look at each piece of the stack we’ll use in this tutorial:

RethinkDB which is a relatively new, open source, NoSQL database that stores
JSON documents. It’s fast, scalable, easy to administer and a Joy to program
with. 
Recently the folks at RethinkDB added some killer features for doing realtime. A
feature called changefeeds, that in my opinion fills a big gap and makes
implementing realtime features a breeze.

We’ll use node.js as our server platform which is a great choice for realtime
applications.

I chose to use Koajs as the web framework, as it is my favorite, but you could
also use express.js, hapi or pretty much any other nodejs web framework.

To communicate between the server and the browser in realtime we’ll be using
socket.io. For those of you who aren’t familiar, socket.io is a library that
creates a continuous connection between the server and the client, that allows
event based messages to be passed back and forth.

On the client-side we’ll be using Angularjs, a framework with some cool features
that can be helpful in writing well structured client-side JavaScript.

Don’t worry if your not fluent in Angular.js, I’ll provide just enough of an
overview for you to understand what is happening.

Lastly we’ll be using a fun experimental library I’m building called BindTable.
BindTable basically allows you to bind a client side object to a rethinkDB
query. When changes happen on the server, the changes are automatically
synchronized with the clientside object.

Source code for this episode can be found at:
https://github.com/knowthen/Episode-10-Building-realtime-web-applications

Reposted from knowthen.com
