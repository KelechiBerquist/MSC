# Assignment
## Sokoban
This is a puzzle game based on a grid of cells. 

Each cell can be empty, a wall, or contain a box or the actor. 

The walls form a boundary, but there are usually some internal walls too. 

If there are N boxes (say, 6), then N non-wall tiles inside the boundary will be designated targets (say, 6). 

The aim of game is for the actor to push the boxes onto (any) of the targets. 

Only one box can be pushed at a time, and boxes cannot be pulled. 

If a box is pushed into certain cells, it will be impossible to push out (‘wall stuck’), and if it is pushed against one or more other boxes, it may also become stuck. 

In addition, it is possible for the actor to block themselves into a limited area of the game (deadlocked).

There are ninety standard levels for the game, called screens, and these will be provided to you. 

A screen file uses a text format to represent the game: 
- ‘#’ for a wall; 
- ‘$’ for a box; 
- ‘@’ for the actor; 
- ‘.’ for a target; 
- ‘+’ for the actor on a target; and 
- ‘*’ for a box on a target. 

As an example, Fig.1 shows the first standard screen.
Figure 1: Sokoban screen.1

Further discussion of Sokoban can be found on Wikipedia (https://en.wikipedia.org/wiki/Sokoban).

You have been supplied with code that implements Sokoban, including a random game player, and also a partially-implemented text-based user interface. 

The ninety standard screens are also included. 

The seven model classes are Sokoban, Cell, Occupant, Actor, Box, Wall and Direction (an enumeration); the
text UI is SokobanUI; the two player classes are Player (an interface) and RandomPlayer; plus, a
problem-specific exception class, SokobanException. 

The classes are illustrated in a UML class diagram
(Figure 2).


## The Tasks
The tasks you are to carry out are as follows:
- To complete the implementation of the text-based user interface to include the (as yet unimplemented) 
	- clear (i.e., reset the Sokoban game), 
	- undo (a single user move), 
	- save (the state of the game to a file) and 
	- load (the state of the game from file) methods. 
	You should only need to make changes to the main user interface class (SokobanUI) to achieve this.
- To design and implement a graphical user interface (GUI) for the Sokoban model code that allows the user to:
	- make moves, 
	- undo user entries, 
	- clear (reset) the game, 
	- save to, and 
	- load from file. 
- At all times, the user should be protected from making illegal moves (the model code guards against moves caused by getting stuck due to walls or other boxes), and so e.g., provided with feedback on the possible moves available to the actor. 
- The appearance of the interface is up to you, but an example is given in Figures 3 and 4. 
- You should keep the user informed through the use of e.g., a status box, and may also consider the use of dialogue boxes where appropriate (such as file location selection).
- Develop a test plan and test the functionality of your classes.
- Write a report including design, testing and reflection (see below). The report should not exceed 3000 words.


## Deliverables
### General Points
The development of your code is based on the object-oriented model, and you must make use of classes in developing your system. 

Each will have its own methods and properties though they could inherit from other
classes.

All interactions must be made via just the text-based UI or just the GUI alone. You may design the GUI as you see fit; see the example depicted above.

You might consider writing custom dialogue(s) to input the user’s preference and other information. This will require a little investigation on your part.

The program should consist of a number of classes each with well-defined functionality. 

There may be a driver class to set things going; GUI classes to provide the user interface; there may be additional classes for file handling.

The code you produce must adhere to the published course coding standards. Marks are awarded for code quality and appropriate defensive programming. 

Your code should be well commented and include Javadoc comments.

You will be expected to test parts of your program against a suitable set of situations. 

In your report you should describe your testing plan and results; also include your test results as screen shots as evidence.

### Design
You must produce design documentation. 
This will include:
- class diagram(s) for the system, 
- a short explanation as to the general purpose of each of the classes you have produced and 
- a justification for any design decisions you have made (including options you discarded and why).


### Implementation
You must provide complete Java source code for your program. 
The code must adhere to the object-oriented style standards as defined for the module. 
Do not use a GUI editor to generate your code, but develop it by hand using the Java Swing API.


### Testing
You are expected to test your code using the strategies studied during the module. 

It is not necessary to test the supplied code, although you may choose to do so.

The testing section of your documentation should indicate the approach you have taken to verifying and validating your system. 

Just as you should not convey the design of your system by presenting the code or even
listing the classes, you should not merely list the tests performed. 
Rather, discuss how tests were selected, why they are sufficient, why a reader should believe that no important tests were omitted, and why the reader should believe that the system will really operate as desired when in use.

You may not be able to create JUnit tests for all aspects of your classes, particularly the graphical user interface classes. It is sufficient to carry out well planned and documented manual testing.

- Strategy: 
	- An explanation of the overall strategy for testing: black box and/or white box, 
	- integration, 
	- kinds of test beds or test drivers used, 
	- sources of test data, test suites. 
	You might want to use different techniques (or combinations of techniques) in different parts of the program.  In each case, justify your decisions.
- Test Data: 
	- A set of tables showing the test data you used for each class, etc. 
	- The format of the test documentation should be as follows: for each test case in the tables,
		- a unique test ID
		- a brief description of the purpose of the test
		- the pre-conditions for running the test
		- the test data
		- the expected result

## Reflection
You must provide a final critical evaluation of your work. 
The reflection section is where you can generalise from specific failures or successes to rules that you or others can use in future software development. 
- What surprised you most? 
- What do you wish you knew when you started? 
- How could you have avoided problems that you encountered during development?

### Evaluation: 
What you regard as the successes and failures of the development: unresolved design problems, performance problems, etc. 

Identify which features of your design are the important ones. 

Point out design or implementation techniques that you are particularly proud of. 

Discuss what mistakes you made in your design, and the problems that they caused.

### Lessons: 
What lessons you learned from the experience: how you might do it differently a second time round, and how the faults of the design and implementation may be corrected. 

Describe factors that caused problems such as missed milestones or the known bugs and limitations.


### Known Bugs and Limitations: 
In what ways does your implementation fall short of the specification? Be
precise. 

Although you will lose points for bugs and missing features, you will receive partial credit for accurately identifying those errors, and the source of the problem.

This reflection should be one to two pages long.


## Deliverables
Submit a zip archive containing a complete BlueJ project for your program including Java source code with comments (this goes in the ‘Code’ portal).
A single document in pdf format (this goes in the ‘Report’ Turnitin portal) containing:
- design documentation as specified above;
- test documentation as specified above;
- your reflection report as specified above.
Two portals will be provided on the eLP (BlackBoard) for you to upload your work.