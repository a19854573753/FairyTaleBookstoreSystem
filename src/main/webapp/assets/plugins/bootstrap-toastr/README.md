# 全目录

3000套系统，LW，复制到流浪器：www.yuque.com/wisebit/blog
# toastr
**toastr** is a Javascript library for non-blocking notifications. jQuery is required. The goal is to create a simple core library that can be customized and extended.

# Current Version
2.0.1

# Demo
- Demo can be found at codeseven.github.io/toastr/demo.html
- [Demo using FontAwesome icons with toastr](plnkr.co/edit/6W9URNyyp2ItO4aUWzBB?p=preview)

## CDNjs
Toastr is hosted at CDN JS

#### Debug
- [//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.1/js/toastr.js](//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.0/js/toastr.js)
- [//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.1/css/toastr.css](//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.0/css/toastr.css)

#### Minified
- [//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.1/js/toastr.min.js](//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.0/js/toastr.min.js) 
- [//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.1/css/toastr.min.css](//cdnjs.cloudflare.com/ajax/libs/toastr.js/2.0.0/css/toastr.min.css)

## NuGet Gallery
nuget.org/packages/toastr

## [Bower](bower.io/)
		bower install toastr


## Wiki and Change Log
[Wiki including Change Log](https://github.com/CodeSeven/toastr/wiki)

## Breaking Changes
 
####Animation Changes
The following animations options have been deprecated and should be replaced:
 
 - Replace `options.fadeIn` with `options.showDuration`
 - Replace `options.onFadeIn` with `options.onShown`
 - Replace `options.fadeOut` with `options.hideDuration`
 - Replace `options.onFadeOut` with `options.onHidden`

## Quick start

###3 Easy Steps
For other API calls, see the [demo](codeseven.github.io/toastr/demo.html).

1. Link to toastr.css `<link href="toastr.css" rel="stylesheet"/>`

2. Link to toastr.js `<script src="toastr.js"></script>`

3. use toastr to display a toast for info, success, warning or error

		// Display an info toast with no title
		toastr.info('Are you the 6 fingered man?')

### Other Options
	// Display a warning toast, with no title
	toastr.warning('My name is Inigo Montoya. You killed my father, prepare to die!')
	
	// Display a success toast, with a title
	toastr.success('Have fun storming the castle!', 'Miracle Max Says')
	
	// Display an error toast, with a title
	toastr.error('I do not think that word means what you think it means.', 'Inconceivable!')
		
	// Clears the current list of toasts
	toastr.clear()

### Close Button
Optionally enable a close button

    toastr.options.closeButton = true;

Optionally override the close button's HTML. 

    toastr.options.closeHtml = '<button><i class="icon-off"></i></button>';

You can also override the CSS/LESS for `#toast-container .toast-close-button`

### Display Sequence
Show newest toast at bottom (top is default)

	toastr.options.newestOnTop = false;

### Callbacks
	// Define a callback for when the toast is shown/hidden
	toastr.options.onShown = function() { console.log('hello'); }
	toastr.options.onHidden = function() { console.log('goodbye'); }

### Animation Options
Toastr will supply default animations, so you do not have to provide any of these settings. However you have the option to override the animations if you like.

####Easings
Optionally override the animation easing to show or hide the toasts. Default is swing. swing and linear are built into jQuery.

	toastr.options.showEasing = 'swing';
	toastr.options.hideEasing = 'linear';

Using the jQuery Easing plugin (www.gsgd.co.uk/sandbox/jquery/easing/)

	toastr.options.showEasing = 'easeOutBounce';
	toastr.options.hideEasing = 'easeInBack';

####Animation Method
Use the jQuery show/hide method of your choice. These default to fadeIn/fadeOut. The methods fadeIn/fadeOut, slideDown/slideUp, and show/hide are built into jQuery.

	toastr.options.showMethod = 'slideDown'; 
	toastr.options.hideMethod = 'slideUp'; 

## Building Toastr

To build the minified and css versions of Toastr you will need [node](nodejs.org) installed.

Install the [Grunt](gruntjs.com/) command line. This might require `sudo`.

```shell
npm install -g grunt-cli
```

Then, from the main project folder run this command. This should not require `sudo`.

```shell
npm install
```

At this point the dependencies have been installed and you can build Toastr

```shell
grunt
```

## Authors
**Hans Fjällemark**

+ twitter.com/hfjallemark

**John Papa**

+ twitter.com/John_Papa

## Credits
Inspired by https://github.com/Srirangan/notifer.js/.


## Copyright
Copyright © 2012 [Hans Fjällemark](twitter.com/hfjallemark) & [John Papa](twitter.com/John_Papa).
