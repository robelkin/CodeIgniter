################
Inflector Helper
################

The Inflector Helper file contains functions that permits you to change
words to plural, singular, camel case, etc.

.. contents:: Page Contents

Loading this Helper
===================

This helper is loaded using the following code

::

	$this->load->helper('inflector');

The following functions are available:

singular()
==========

Changes a plural word to singular. Example

::

	$word = "dogs";
	echo singular($word); // Returns "dog"

plural()
========

Changes a singular word to plural. Example

::

	$word = "dog";
	echo plural($word); // Returns "dogs"

To force a word to end with "es" use a second "true" argument.

::

	$word = "pass";
	echo plural($word, TRUE); // Returns "passes"

camelize()
==========

Changes a string of words separated by spaces or underscores to camel
case. Example

::

	$word = "my_dog_spot";
	echo camelize($word); // Returns "myDogSpot"

underscore()
============

Takes multiple words separated by spaces and underscores them. Example

::

	$word = "my dog spot";
	echo underscore($word); // Returns "my_dog_spot"

humanize()
==========

Takes multiple words separated by underscores and adds spaces between
them. Each word is capitalized. Example

::

	$word = "my_dog_spot";
	echo humanize($word); // Returns "My Dog Spot"

resolve_case()
==========

Takes a singular word and a count, and returns the word in the sigular or plural form based on the count
Optionally, will return the string including the count supplied appended to the start. Example

::

	$time = 2;
	echo resolve_case( 'second', $time, true ); // Returns "2 seconds"