#ScrollMagic [![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif "Shut up and take my money!")](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=8BJC8B58XHKLL "Shut up and take my money!")

###The jQuery plugin for magical scroll interactions.

ScrollMagic is a jQuery plugin which essentially lets you use the scrollbar like a playback scrub control.  
It's the plugin for you, if you want to ...
* ... start an animation at a specific scroll position.
* ... synchronize an animation to the scrollbar movement.
* ... pin an element at a specific scroll position (sticky elements).
* ... pin an element for a limited amount of scroll progress (sticky elements).
* ... easily add a parallax effect to your website.
* ... create an inifinitely scrolling page (ajax load of additional content).
* ... call functions when the user hits certain scroll positions or react in any other way to the current scroll position.

Check out [the demo page](http://janpaepke.github.com/ScrollMagic), browse [the examples](http://janpaepke.github.com/ScrollMagic/examples/index.html) or read [the documentation](http://janpaepke.github.com/ScrollMagic/docs/index.html) to get started.

##About the Plugin

ScrollMagic is a complete rewrite of its predecessor [Superscrollorama](https://github.com/johnpolacek/superscrollorama) by [John Polacek](http://johnpolacek.com).  
Like Superscrollorama it relies on the [Greensock Animation Platform (GSAP)](http://www.greensock.com/gsap-js/) to build animations, but was developed with specific regard to former shortcomings.

The major perks of using ScrollMagic include:
* optimized performance
* flexibility
* mobile compatibility
* ready for responsive webdesign
* object oriented programming and object chaining
* event management
* support for both scroll directions (even different on one page)
* support for scrolling inside div containers (even multiple on one page)
* extensive debugging and logging capabilities

ScrollMagic takes an object oriented approach using a controller for each scroll container and multiple "scroll scenes" to define what should happen at what point in time.  
While this offers a great deal of control it might be a little confusing if you're just starting out with javascript.  
If you don't really care about any of the points above and are just looking for a simple solution to implement basic css animations I would strongly recommend taking a look at [skrollr](http://prinzhorn.github.io/skrollr/) which almost solely relys on element attributes.

## Installation
Aside from [jQuery](http://jquery.com/) make sure you have loaded the [Greensock Animation Plattform (TweenMax)](http://www.greensock.com/gsap-js/).  
To use ScrollMagic in your project simply include the plugin js file in the head section of your HTML file:
```html
<script type="text/javascript" src="js/jquery.scrollmagic.js"></script>
```

For deployment use the minified version __instead__:
```html
<script type="text/javascript" src="js/jquery.scrollmagic.min.js"></script>
```
_**NOTE:** The logging feature is removed in the minified version for obvious file size considerations._

To have access to the debugging extension during development, include this file __additionally__:
```html
<script type="text/javascript" src="js/jquery.scrollmagic.debug.js"></script>
```
You can remove the debugging extension for actual deployment.

## Usage

```javascript
// init controller
var controller = new ScrollMagic();

// assign handler "scene" and add it to Controller
var scene = new ScrollScene({duration: 100})
				.addTo(controller);

// add multiple scenes at once
var scene2;
controller.addScene([
	scene, // add above defined scene
	scene2 = new ScrollScene({duration: 200}), // add scene and assign handler "scene2"
	new ScrollScene({offset: 20}) // add anonymous scene
]);
```
Check out the [examples](http://janpaepke.github.com/ScrollMagic/examples/index.html) or the [documentation](http://janpaepke.github.com/ScrollMagic/docs/index.html) for full reference.
##Help
To get help please read the [support guidelines](https://github.com/janpaepke/ScrollMagic/blob/master/CONTRIBUTING.md).  
If you still can't figure it out, please post your questions in the [project's issues section](https://github.com/janpaepke/ScrollMagic/issues).

##Browser Support

ScrollMagic aims to support all major browsers in recent versions:  
Firefox 26+, Chrome 30+, Safari 6+, Opera 19+, IE 9+

##About the Author

I am a freelance Art Director based in Lausanne, Switzerland.  
I started this project to intensify my knowledge of javascript.

[Check out my website](http://www.janpaepke.de) or [Follow me on Twitter](http://twitter.com/janpaepke)

##License

ScrollMagic is dual licensed under the MIT license and GPL.  
For more information click [here](https://github.com/janpaepke/ScrollMagic/blob/master/LICENSE.md).  
Click [here](http://www.greensock.com/licensing/) to get more information on greensock licensing.
