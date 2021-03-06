graphy
======

Graphy is a jQuery plugin/component which allows you to create easy pie charts.
Demo: http://mgachowski.pl/graphy/

## Instalation:

* Requires jQuery

<pre>
&lt;link href="style.css" rel="stylesheet"&gt;
</pre> 
in your head tag
<pre>
&lt;script src="graphy.js"&gt;&lt;/script&gt;
</pre> 
in your head tag (or at the bottom of the site)


## How to run:

Running *graphy* is very simple, you just need to create an element which will contain all the data, and then init it!

Example (fifty-fifty):
<pre>
&lt;!-- Create the main element - the ID is not nessesary or can be various, but the class *must be* .graphy --&gt;
<code>
&lt;div id="graphy" class="graphy"&gt;
  &lt;!-- insert data values, for this example 300 and 300, which gives us 50%:50% --&gt;
  &lt;div data-value="300"&gt;&lt;/div&gt;
  &lt;div data-value="300"&gt;&lt;/div&gt;
&lt;/div>
</code>
&lt;script&gt;
  $(document).ready(function() {
	/* Graphy init on the #graphy element */
  	$('#graphy').graphy();
  });
&lt;/script&gt;
</pre>

Thats all!

## Options:

Graphy takes some options when initialized:
* (string) valueDataset [default: 'data-value']
* (string) titleDataset [default: null]  *not yet supported*
* (array) colors        [default: ['#fd795b', '#bcf1ed', '#fdedd0', '#b76eb8']]
* (object) canvasSize	[default: {width: 200, height: 200}] *for IE 8 support*

Example:
<pre>
  $('#graphy').graphy({
      colors: ['red', 'blue', 'green', 'yellow'],
      valueDataset: 'data-mywhatever',
      titleDataset: 'data-mysupertitle',
      canvasSize:   {width: 220, height: 220}
  });
</pre>

## Browser support:

Graphy should be supported in every new web browser: 
* Firefox 
* Chrome
* Opera
* Safari
* IE 9/10
* IE 8 (canvas element with Google's excanvas library to work)


TODO:
* Rewrite core to be more readable. 

