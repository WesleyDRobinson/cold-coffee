## Host a webpage in seconds

<!--Alternate Titles-->
<!--Get your web dev sandbox up in seconds-->
<!--Test your web page “in the real world”-->

Alright, to get setup will take you, like, no time at all, probably 5 min.

Open Terminal, actually [go get iTerm2](https://www.iterm2.com/index.html) if you haven’t yet. If you’re on a Windows 10 machine, no worries, you can now [run native Bash on Ubuntu on Windows](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)!

`mkdir enlightenment && cd enlightenment` 

If you’ve achieved this already, you know you can just misspell it slightly or add some characters and it will make a similar folder that’s just as empty.

Get [http-server, a simple zero-configuration command-line http server](https://github.com/indexzero/http-server); it’s amazing.
Use npm and install globally:
`npm install http-server -g` 

If that step doesn’t make sense to you, stop here. Go ahead and [read about npm installation here](http://blog.npmjs.org/post/85484771375/how-to-install-npm).

Now, maybe you don’t like to admit it, but we all `touch index.html`  file from time to time. Now’s the time for you to go ahead and do it. I’ll wait here….
While we are feeling touchy, go ahead and `touch index.js` , do it! You know you want to.... yeah, I’ll wait.

Ok, now, open the index.html file in your favorite [text editor](https://en.wikipedia.org/wiki/Text_editor) and craft yourself an HTML5 document. 
Did you know [HTML5 was only published in October 2014](https://en.wikipedia.org/wiki/HTML5)? Started in 2004, and sometime around 2010ish, people started talking about it a lot.
You better believe The Hippest Executive Around (tm) only wants HTML5 Ninjas on his team from now on. I'm not talking to candidates who have less than 2 years experience with HTML5 moving forward.
So everyone added it to their LinkedIn profiles; problem solved! Now we can get back to looking for the next AJAX framework; nope, [Phoenix Framework! learning Elixir & Erlang](http://www.phoenixframework.org/docs/learning-elixir-and-erlang) is the future. You know [JS is exhausting and busted](https://segment.com/blog/the-deep-roots-of-js-fatigue/), some have already [abandoned node.js](https://medium.com/@tjholowaychuk/farewell-node-js-4ba9e7f3e52b#.b22ao4r2t) and the [best and next best of the past](https://www.toptal.com/scala/why-should-i-learn-scala) for the [greener pastures of golang](http://jimplush.com/talk/2015/12/19/moving-a-team-from-scala-to-golang/). Dear God, what were we even talking about?

HTML5, since it introduces all kinds of new possibility for the web! New, useful APIs like web storage, drag and drop, audio and canvas. We have <import>, [\#include for the web](http://www.html5rocks.com/en/tutorials/webcomponents/imports/)! Very exciting stuff.

But a basic outline could look like:

```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>My Site</title>
    
    </head>
    <body>
    
    <h1> Important Note: </h1>
    
    <!-- [with HTML5, any element can be editable](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_Editable), whaaaaa?! :hearteyes: -->
    <p id="message" contentEditable=true> Remember those less fortunate than you.</p>
    <button id="button">Press, Tap or Click Here</button>
    
    <!-- let there be javascript -->
    <script src="index.js"></script>
    
    </body>
    </html>
```

If you have something like the above, you’re ready to serve.

`http-server -o`

O yea! Look at this:
![] (https://cldup.com/zep4UIz0rv.png)

You have a lot of environment here. Open up the console and play around with the page in a live way.

![] (https://cldup.com/aECDgqzGGD.png)
I guess the answer was “yes”.

### What do I do now?
Great question! [learnyoujavascript, HTML5, CSS and the DOM web development with MDN](https://developer.mozilla.org/en-US/docs/Web), that's what!

Read some [info about web components](http://webcomponents.org/).

Try dropping the following in your index.js and see how that feels:

```
(function () {
    var parsed = performance.now();

    window.onload = function () {
        var loaded = performance.now();
        var text = document.createTextNode(`Your browser parsed the page in ${parsed} ms, and then executed this onload function at ${loaded} ms`);
        document.querySelector('#test-area').appendChild(text);
    }
}());
```

Do you know what these things are?

Want to know a little about me?

I moved to SF in 2015 after giving up my promising career in the NYC beer industry to pursue my passion for #delusions of technology.

I consolidated years of exposure to coding, logic, math and HTML/ CSS frustrated learning. Taught myself some Javascript, then attended Grace Hopper Academy, which saved my life. 
It’s an all women, immersive, tuition-deferred web developmenet accelerator! I actually went to Fullstack Academy since I’m a man, and I attended in March 2015.

By training, I’m an analytical chemist, published even, 😏 🤓 
For a while, I taught at Missouri State University, Ozarks Technical Community College, and conducted R&D with a team of ~10 on electroactive polymers at a now defunct division of Crosslink USA. The asserted applications of our research were in capacitors with superfast-charging and slow, controlled release; medical devices; and aerospace sensors. 

Now I work and learn at Segment.com solving problems for web developers. If you want a to understand customers and associates so you can delight them, add analytics to your site! 
Use Segment’s platform because you can be up and running in hours instead of days. Check out the `analytics.js` Quickstart Guide. You’ll be up in hours; not days.

I grew up on a cattle farm; a hillbilly in the Ozark Mountains of Arkansas.
