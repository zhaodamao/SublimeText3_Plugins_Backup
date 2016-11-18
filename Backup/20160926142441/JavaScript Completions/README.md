<h1>JavaScript Completions</h1>

[![Sublime Text](https://img.shields.io/badge/Sublime%20Text-2%20%2F%203-brightgreen.svg)](https://www.sublimetext.com/)
[![Package Control](https://img.shields.io/packagecontrol/dt/JavaScript%20Completions.svg)](https://packagecontrol.io/packages/JavaScript%20Completions) 
[![Package Control](https://img.shields.io/packagecontrol/dd/JavaScript%20Completions.svg)](https://packagecontrol.io/packages/JavaScript%20Completions)

JavaScript Completions for sublime text

It helps you to write your scripts more quickly with hints and completions.

<strong>jQuery</strong> and <strong>NativeScript</strong> completions disabled by default!
You can enable them on Preferences -> Package Settings -> JavaScript Completions.

<h2>Usage</h2>

To try it, just write.

Examples:

<img src="https://media.giphy.com/media/l0MYypWg9s9exQ0xi/giphy.gif" alt="example #1 of JavaScript Completions"/>

<img src="https://media.giphy.com/media/d31wQpJ2iCyGtS0M/giphy.gif" alt="example #2 of JavaScript Completions"/>

<code>description-Name_of_function/property/method</code> shows to you the explanation of the function/property/method and its syntax.

Information about the description of function/property/method has been taken on this sites:

- [http://html5index.org/index.html](http://html5index.org/index.html)
- [https://html.spec.whatwg.org/](https://html.spec.whatwg.org/)
- [http://www.ecma-international.org/ecma-262/5.1/](http://www.ecma-international.org/ecma-262/5.1/)
- [https://www.w3.org](https://www.w3.org)
- [http://api.jquery.com/](http://api.jquery.com/)
- [https://docs.nativescript.org/api-reference/globals.html](https://docs.nativescript.org/api-reference/globals.html)

<h3>"Find JavaScript Description" Feature</h3>

<strong>Supported only by Sublime Text 3</strong>

<strong>key-map</strong> of this feature disabled by default!

You can check the description of function/property/method by selecting the word (or, in case, it will take the first word near the blinking cursor) you want find. "right-click" on your mouse and click on "Find JavaScript Description".

It will show a popup with the list of possible descriptions or, in some case, the direct description. 

In case, you can also use "key-map"! Just go to Preferences -> Package Settings -> JavaScript Completions and enable it.

<img src="https://s17.postimg.io/stsylwwn3/Schermata_2016_09_18_alle_17_41_17.png" alt="example #1 Find JavaScript Description Feature"> 

<img src="https://s17.postimg.io/pyfvf1sn3/Schermata_2016_09_18_alle_17_40_28.png" alt="example #2 Find JavaScript Description Feature"> 

<h3>"Evaluate JavaScript" Feature</h3>

<strong>Supported only by Sublime Text 3</strong>

This feature uses node.js (v6.6.0) executable.

You can change the node version on Preferences -> Package Settings -> Evaluate JavaScript settings

It will download automaticaly the binary for your OS.

A message will appear on the "status bar" of Sublime Text.

<strong>context menu option</strong> of this feature disabled by default!

<strong>key-map</strong> of this feature disabled by default!

You can evaluate the entire text selection or the current line! 
If you select a text region and evaluate it, in the gutter of the editor will appear 2 white dots.
The first white dot represents the start of the region and the second white dot represents the end of the region.
You can eventually modify the region and, without reselect the same region, you can evaluate it again! 
If you want hide this 2 dots, there is an entry on the context menu "Evaluate JavaScript".

When you evaluate code, this plugin will prepend <code>"use strict";</code> automaticaly!

There are two main mode to evaluate code:
- [eval](https://nodejs.org/dist/latest-v6.x/docs/api/cli.html#cli_e_eval_script)
- [print](https://nodejs.org/dist/latest-v6.x/docs/api/cli.html#cli_p_print_script)

To enable this feature on context menu, go to Preferences -> Package Settings -> Evaluate JavaScript and enable it.

In case, you can also use "key-map"! Just go to Preferences -> Package Settings -> Evaluate JavaScript and enable it.

<img src="https://s17.postimg.io/c7becu3pb/Schermata_2016_09_18_alle_18_07_00.png" alt="example #1 Evaluate JavaScript Feature"> 

<img src="https://s17.postimg.io/fs79w288v/Schermata_2016_09_18_alle_18_08_55.png" alt="example #2 Evaluate JavaScript Feature"> 

<h3>ENABLE or DISABLE completions</h3>

You can ENABLE or DISABLE completions! Just go to Preferences -> Package Settings -> JavaScript Completions

<h3>Other Context menu options</h3>

Context menu options:
- <a href="#surround-with">Surround With</a>
- <a href="#delete-surround">Delete Surrounded</a>
- <a href="#create-class-from-object-literal">Create Class from object literal</a>
- <a href="#sort-array">Sort array</a>

<h4 id="surround-with">Surround With</h4>

You MUST first select text to "enable" these options.

You can surround code with:
- if statement
- if else statement (this works only if you selected 2 regions, see <a href="#context-menu-option-example-2">example</a>)
- while statement
- do while statement
- for statement
- try catch statement
- try catch finally statement
- Multi-line comment
- Single-line comment

This options works also on multiple selections at once.

<h4 id="delete-surround">Delete Surrounded</h4>

Options are:
- Delete multi-line comment
- Delete single-line comment
- Strip quoted string

This options works also on multiple selections at once.

<h4 id="create-class-from-object-literal">Create Class from object literal</h4>

This option create a JavaScript Class from an object literal (Constructor with all setter and getter for each field).

You can set default values or use the string <code>"required"</code> to say that a field hasn't a default value.

To work properly, you MUST declare a variable and assign an object literal to it, like this example:

```javascript
var Person = {
  name: "required",
  surname: "required",
  email: "",
  age: 18
}
```

This options works also on multiple selections at once.

<h4 id="sort-array">Sort array</h4>

Just put the cursor between brackets and will appear a menu with this options:
- Sort array ASC ( compare function: <code>function(x,y){return x-y;}</code> )
- Sort array DESC ( compare function: <code>function(x,y){return y-x;}</code> )
- Sort array alphabetically ASC
- Sort array alphabetically DESC

This options works also on multiple selections at once.

Examples of usage:

<img src="https://media.giphy.com/media/3o7TKOwWEYUGPX4G6Q/giphy.gif" alt="example #1 Other Context menu option"> 

<img id="context-menu-option-example-2" src="https://media.giphy.com/media/l3vR1DjPDWRFfl3LG/giphy.gif" alt="example #2 Other Context menu option"> 

<i>MIT License</i>
