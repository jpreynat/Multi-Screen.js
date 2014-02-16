Multi-Screen.js
===============

A simple, lightweight, and easy to use jQuery plugin which turns a single page into a collection of screens with animated naviagion.

SETUP YOUR PAGE:
- Divide up the <body> of your HTML into <div> elements, giving them all the ms-container class (the plugin needs at least two to run), and build each screen inside. 
- Give the element you want as your default screen the class ms-default. If no default is specified, the top ms-container will be used, and if more than one default is found the top ms-default will be used.
- To facilitate navigation between screens, each one requires a unique id attribute.

BUILD NAVIGATION:
- To switch from one screen to another, simply give the class ms-nav-link to anything you can click on, and specify which screen to swap in for the current one by setting the data-ms-target attribute equal to its id.
- You can specify the enter and exit animations using the data-ms-enter and data-ms-exit attributes. The valid commands are fade, top, topright, right, bottomright, bottom, bottomleft, left, topleft, fadetop, fadetopright, faderight, fadebottomright, fadebottom, fadebottomleft, fadeleft, and fadetopleft. The default is fade.
- You can also specify the animation time in miliseconds using the data-ms-enter-time and data-ms-exit-time attributes, which take in a valid integer value, and specify if the animations should occur synchronously or in sequence with the data-ms-delay attribute, which takes in true or false. The defaults are 500 miliseconds and false (no delay).

SETTING DEFAULTS:
- Multi-Screen.js makes it easy to change the defaults for the animations, their times, and the delay, through the jQuery functions below.
- Each function returns a boolean (true if default was succesfully changed or false if not).

- $.multi_screen.set_default_animation(String type, String command); takes in the animation type ('enter' or 'exit') and the animation command (must be valid).
- $.multi_screen.set_default_animation_time(String type, Int time); takes in the animation type ('enter' or 'exit') and the animation time (must be a valid integer).
- $.multi_screen.set_default_animation_delay(Boolean delay); takes in true or false to set the delay.

INSTALLATION:
- Download the latest version from GitHub (documentation available) and extract the Multi-Screen JS and CSS files.
- Link the JS and CSS files in the <head> tag of your page (or copy and paste the styles into your own stylesheet).
