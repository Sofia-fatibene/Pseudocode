# Pseudocode
 
 MIlestones:
1. Have an instructions screen, and game board with images, and hints Nov 9
2. Make the keys work to guess letters Nov 10
3. Have a working timer Nov 13
5. Sound effects / colours (final touches)  Nov 15



`Let screen = 1`
Let x, y

Function setup {
Createcanvas (windowwidth, windowheight) 
Background
}
function drawScreen (screen) {
	
	 //rectMode (CENTER);
	 //background (0);
   
  //START SCREEN 1
  if (screen == 1) { 
 		background (60, 93, 179);
 		fill (141, 162, 224)
		rect (400,50,600,500);   
  	fill (0);
  	
 // CREATE START BUTTON
		button = createButton('Click to play');
		button.size(400,60)
  	button.position(500, 400);
  	button.mousePressed(startGame);
  } else if (screen == 2){
    clear()
		createCanvas (400,400)
		background (60, 93, 179)


Function draw() {

Rect 
size(400, 400);
line(120, 80, 340, 300);
 }

let phrases = ["fox in a box", "dog at the park", "cat has a hat"];
let curPhrase;
let guess
let wrongGuesses;

function setup() {
	// Make the drawing canvase as big as the window
	createCanvas(windowWidth, windowHeight);
	
	// Set the RGB background colour
	background(250,250,250);
	
	// Set the frame rate
	frameRate(1);
	
	// initiate game
	selectRandomPhrase();
}

function selectRandomPhrase() {
	let index = Math.floor(random(0, phrases.length));
	print("index is ", index);
	curPhrase = phrases[index];
	guess = [];
	wrongGuesses = [];
	for(let i = 0; i < curPhrase.length; i++) {
		guess.push(curPhrase[i] == " " ? " " : "_"); 
		print(i, guess[i]);
	}
}

function draw() {
	clear();
	textSize(50);
	text(curPhrase, 100, 60);
	text(guess.join(" "), 100, 150);
	textSize(30);
	text(wrongGuesses, 100, 300);
		fill(255, 0, 0)
	
	
}

function keyPressed() {
	// print("key pressed is", key);
  if (key >= 'a' && key <= 'z') { 
		print("You guessed", key);
		
		// Find all instances of key in curPhrase
		let result = [];
		for(var i=0; i < curPhrase.length; i++) {
    	if (curPhrase[i] === key) {
				result.push(i);
				guess[i] = key;
			}
		}
		
		// Check results for matches
		if (result.length > 0) {
			// we found a match
			print("Found matches at indices", result);
		}
		else if (wrongGuesses.includes(key)) {
			print("no");
		}
		else {
		wrongGuesses.push(key);
				print("NO MATCH!");
  }
}
}
let phrases = ["fox in a box", "dog at the park", "cat has a hat"];
let curPhrase;
let guess
let wrongGuesses;

function setup() {
	// Make the drawing canvase as big as the window
	createCanvas(windowWidth, windowHeight);
	
	// Set the RGB background colour
	background(250,250,250);
	
	// Set the frame rate
	frameRate(1);
	
	// initiate game
	selectRandomPhrase();
}

function selectRandomPhrase() {
	let index = Math.floor(random(0, phrases.length));
	print("index is ", index);
	curPhrase = phrases[index];
	guess = [];
	wrongGuesses = [];
	for(let i = 0; i < curPhrase.length; i++) {
		guess.push(curPhrase[i] == " " ? " " : "_"); 
		print(i, guess[i]);
	}
}

function draw() {
	clear();
	textSize(50);
	text(curPhrase, 100, 60);
	text(guess.join(" "), 100, 150);
	textSize(30);
	text(wrongGuesses, 100, 300);
		fill(255, 0, 0)
	
	
}

function keyPressed() {
	// print("key pressed is", key);
  if (key >= 'a' && key <= 'z') { 
		print("You guessed", key);
		
		// Find all instances of key in curPhrase
		let result = [];
		for(var i=0; i < curPhrase.length; i++) {
    	if (curPhrase[i] === key) {
				result.push(i);
				guess[i] = key;
			}
		}
		
		// Check results for matches
		if (result.length > 0) {
			// we found a match
			print("Found matches at indices", result);
		}
		else if (wrongGuesses.includes(key)) {
			print("no");
		}
		else {
		wrongGuesses.push(key);
				print("NO MATCH!");
  }
}
}' 


