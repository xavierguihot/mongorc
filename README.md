## Overview


A simple .mongorc script which provides aliases and helpers for the MongoDB
shell.

Intended for MongoDB 3.

For instance typing "tree" in the mongodb shell would print the content of your
mongo instance:

	> tree
	 * 0.016GB-0.042GB-0.002GB (115721)              database_1
		* collection_A (27563)
		* collection_B (88158)
	 * 0.874GB-2.478GB-0.060GB (6888598)             database_2
		* collection_C (1162158)
		* collection_D (426384)
		* ...
	 * ...

Three aliases are available:

* tree: prints all databases and collections
* indexes: prints all databases, collections and indexes
* cleanCache(): drops cache collections (collections I named *_cache)


## Installation


Just download the .mongorc.js script and put it in your home folder:

	wget "https://raw.githubusercontent.com/XavierGuihot/mongorc/master/.mongorc.js" -O ~/.mongorc.js


## Quick Explanation


The MongoDB shell uses a javascript interpreter. In fact you can create scripts
in javascript which perform heavy MongoDB data transformations (not only for the
mongo shell), the same way you would do it with apis of other langages.

This script just contains a bunch of javascript functions, and since it's in
your home folder under the name .mongorc, then these functions are integrated by
mongo to your available mongo shell commands.
