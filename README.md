Enyo Captcha
=============

Not a truly secure captcha. If a developer has access to the JavaScript console they can figure out how to solve the captcha. A future enhancement with the seed and validation on the server side will be a bit more secure, but still decipherable. At any rate it's a start to slow down the robots.

# Enyo Kind for including a Captcha
This captcha is a simple graphical puzzle (puzzle is overstatement) requiring some shape dragging. 

This captcha provides two authentication modes: local and server. 

In local mode the captcha is very hackable by anyone with a JavaScript console (e.g. running Enyo in Chrome).

In server mode (TBD), the module makes a call to a server

## Example of local mode here:
http://jsfiddle.net/pcimino/VBNSM/

## NOTES
###Server Mode 
Server mode is planned, but not yet implemented.
###Text Mode
There are some fragments in the code suggesting a text input instead of the graphic puzzle. There is a future enhancement planned to give the user the option to input text instead of using the draggable UI.

## Settings
### Local
Set to true, runs in local mode, false runs in server mode.

### Server Host
Required if running in server mode.

### onPuzzleSolved
Subscribe to this event which gets bubbled up when the puzzle is solved.

## Validation
### Local mode
In local mode, the instance sets the "passed" attribute to true. onPuzzleSolved event gets generated. It's up to the client to allow/prevent form submission.

### Server mode (Future enhancement)
When the instance starts up it queries the server for image URLs to load. The server is responsible for the following actions:  
1. Select 4 (maybe configurable in the future) random numbers.  
2. Generate the expected result from these numbers and store the result in a secure location.  
3. Return the list of numbers which are used to generate the solution.  

# Implementing



# Text Puzzle Mode
Planned, in progress, some issues, so it's turned off.

