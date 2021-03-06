# brain

brain is a javascript neural network library. An example, training the XOR bitwise operation:
	var net = new NeuralNetwork();
	net.train([{input: [0, 0], output: [0]},
	           {input: [0, 1], output: [1]},
	           {input: [1, 0], output: [1]},
	           {input: [1, 1], output: [0]}]);
	
	var output = net.run([1, 0]);

The output will be `[0.987]` or something close like that. There's no reason to use a neural network to figure out XOR, but it's a small example (-:

# using in the browser
Download the latest [brain.js](http://github.com/harthur/brain/downloads). If you can you should train the network offline (or on a Worker thread) and use the `toFunction()` or `toJSON()` options to plug the trained network in to your website.

# using as a commonJS package
To use this as a commonJS package (node/narwhal) checkout or download the code, it is a commonJS package. If you have [node](http://nodejs.org/) and [npm](http://github.com/isaacs/npm) you can:

	npm install brain@latest

then:

	var brain = require("brain");
	var net = new brain.NeuralNetwork();
	
If you didn't install with npm, you can specify the path to the brain.js file, like "./lib/brain".

# API
[http://harthur.github.com/brain#api](http://harthur.github.com/brain#api)

# tests
Running the tests requires [node.js](http://nodejs.org/):

	node test/runtests.js

# todo
There are many things to be done: [wiki todo list](http://wiki.github.com/harthur/brain/todo)

