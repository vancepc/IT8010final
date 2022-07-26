
# Project Title

Astronaut Geometry

A hodgepodge game about learning Maths


## Demo and controls

Unpack the "IT Final Build.zip" file and run the executable 

Controls are as follows:

A/D, leftarrow/rightarrow: linear movement

Space: Jump (and double jump)

E: interact with NPCs and objects

Z: optional infinite jump mode 

## Design Document History

This section will explain the history of this document

**Version 0.5**

Initial construction of document in preparation for peer feedback

**Version 1.0**

Finalization of document after peer feedback and finished construction of game

## Development History
This section will outline the design process and changes to the overall game due to iterative development and feedback

**Version 0.1.0**

Initial design concept for the game
1.	Created low fidelity prototype for level design
2.	Created low fidelity prototype for UI infrastructure
3.	Began to design level concepts for the three levels
**Version 0.1.1**

Scaled back on initial design concept after receiving peer/teacher feedback
1.	UI concepts simplified to reduce clutter
2.	Simplified and streamlined gameplay elements including pickup quests and level puzzles
3.	Scaled back overall scope for pre-alpha preparation from four levels to one
**Version 0.2.0**
Initial game construction
1.	Designed basic level architecture 
2.	Added player controller and playercontroller scripts
3.	Scripted UI elements and pickup objects
 

**Version 0.3.0**

Adding full elements to first level
1.	Added NPCs with dynamic text
2.	Added scripts for resolving clues
3.	Added debug mode for testing
4.	Imported objects used for interacting with level
**Version 0.3.1**

Fiddling with colliders, physics materials, and linear drag
1.	Considered scrapping entire project over physics issues
a.	How can 2 colliders possibly act so poorly together
b.	Created a custom physics material and modified standard player physics to bypass physics issues

**Version 0.5.0**

Finalization of core scripts and completed rough design of first level
1.	Having all scripts in place will exponentially speed up further development
2.	This version marks ‘Rough Draft’ content release

**Version 0.6.0**

Complete refactoring of base code to integrate multiple levels
1.	Rebuilt most scripts from the ground up to allocate for dynamic entries on each level, removing the need for most level-specific scripts. Increased scalability
2.	Completed a mockup of level 2 with basic functionality
**Version 0.7.0**

Addition of transition screens
1.	Added transition screens with level summary and math for levels 1, 2, and (unfinished) 3
2.	Added some small music to differentiate levels
**Version 0.9.0**

Finalization level 3 and reworking of scripts/levels to prepare for release
1.	Final level implemented and ‘full’ build available
2.	Preparing for user feedback, sending to friends for beta test of full release
**Version 1.0.0**

Final design for submission
1.	Tweaked physics and some dialogue after receiving peer feedback
2.	This version marks ‘Final Draft’ content release



## Overview

Astronaut Geometry (otherwise known as AG) is an educational game made for students between grades six and ten with a primary focus on teaching geometric concepts. The overall model for the game is scoped as an action/adventure platformer where the player controls a moveable astronaut and navigates individual levels to find clues, culminating in a level end that tells a geometric formula or illustrates the solution to a geometric equation.

Visually, AG is designed such that individual level objects and platforms, when possible, maintain a consistent theme representing a specific geometric shape. The first level, for example, is comprised entirely of square tiles that are square (blocky) in nature, with square pickups and a square puzzle to interact with. The player will retain their individual astronaut character throughout levels, and in some cases objects or NPCs will break theme to maintain scope and feasibility.

**The primary purpose of the game is education to satisfy the following learning objectives:**

•	Introducing young students to geometric concepts

•	Providing geometric facts to enhance knowledge

•	Showing geometric formulas through understandable visual constructs

•	Drawing parallels between world design and underlying geometry

## Problem Statement
Current educational games that facilitate learning geometry through play only cover basic overviews and identification of shapes and do not delve into middle-school educational requirements for geometry, such as geometric formulae and calculations. 

## Project Purpose
This project aims to create an intermediate-level experience to challenge middle-school students to continue their geometry education through an active adventure platformer-style game. The game will be comparatively more challenging and engaging than current geometry games designed for younger children.

## Gameplay
The overall game is subdivided into individual levels; in a given level, a player must complete two to four tasks. After completing a task, the player is given a clue (mathematical fact) that will help them learn about a given shape or geometric formula. Tasks include but are not limited to the following:

•	Interacting with NPCs

•	Gathering collectible objects

•	Interacting with objects multiple times

•	‘Push-Pull’ puzzles

•	Navigating an area within a time limit

When a player has collected all clues for a given level, they will navigate to the level-end NPC and interact with them. The NPC will then provide dialogue answering the challenge for the level.
Tasks and puzzles will take on a variety of the above-listed forms, but generally be thematically related to the level’s geometric shape architecture.

## Mechanics and Interface
The player is placed within a bounded world which is defined and constrained by a level-based tileset. Default unity physics apply for gravity; the player is able to jump or double-jump to reach higher elevation to navigate and complete levels. To compensate for oddities with the Unity physics engine, tiles are supplied with a custom 2d physics object that provides 0 friction, giving a ‘sliding’ locomotion feel, and slowed by linear drag on the player character.

A main staple of player interaction is the interact key (E), which serves composite functions of talking to NPCs, interacting with objects, and picking up objects for push-pull interactions.

As they do not fit the scope of this game, there is no inherent economy, and combat does not exist in any form.

The main camera is centered on the player and does not dynamically move. The UI is also statically anchored to the main camera and drawn in front of all other objects. The UI displays a current timer for the level, what clues have been collected, and progress on pickup collection for that level.

Various interactive objects are placed in the levels. Currently, the following objects exist:

•	Four distinct NPCs to talk to

•	A television that can be freely pushed using rigidbody physics architecture

•	Two doors that allow teleportation to and from an auxiliary level add-on

•	A square used for the first level’s puzzle that fills in with smaller squares to demonstrate area

The game is instanced and will restart upon loading the game executable. Saving will not be an option or feature in the current design scope. Currently, there are no transitionary level screens or options menus. 
Future iterations will include the following:

•	An options menu that pauses the game timer including the listed options

o	Volume sliders for SFX and music

o	Quit to desktop

•	A ‘help’ submenu

•	Keyboard display as input reminders for movement and actions

•	A pause button (P) 

•	A start menu that displays before the first level

A debug mode is included in the current game – the player can press Z to toggle an infinite jumps mode. Currently, this debug mode is listed by the first NPC 

## Story, Narrative and Backstory

In the initial design of the game, story and individual character development was forsaken over functionality and gameplay. Future iterations would include a small, unobtrusive overarching storyline tying the levels together, with a few repeat characters including the initial ‘help’ NPC and the level-end NPC. The characters will have a light backstory of generically trying to help the player achieve their goals for altruistic purposes and/or a general love of Mathematics.
Levels

The current game iteration is comprised of a singular ‘Level 1’ which is also considered the training level as it introduces the control scheme and general constructs of the game world/objectives. The goal of level 1 is to ultimately find the formula to calculate the area of a square. Along the way, the player picks up the following clues:

•	A square has four sides

•	All side lengths of a square are the same

•	You only need one side measurement to find the area.

Movement with WASD keys is assumed as prior knowledge by the player, but will be iterated into a static sign at the start of level 1. The player interacts with a NPC near their spawn point to learn about collecting clues, learn about the Z toggle for jumps, and learn about the amount of clues for level 1.
Clues are earned in the following ways:

•	Speaking to an NPC for a ‘free’ clue

•	Collecting 9 neon squares placed around the game map

•	Teleporting to an offshoot puzzle room and completing a simple puzzle by pressing E 9 times

The level itself is fairly open-ended within the tile constraints and there is not a singular defined path that the player needs to follow. As long as all three tasks are completed, the player may end the level at any time. Tasks may be completed in any order.

There is one NPC in the level that serves simply as dialogue and a false flag to discourage the player from entering the puzzle room; the player needs to ignore this false flag and proceed to collect a clue.

Level two continues the geometric theme and serves as an introduction to circles. Unlike the first level, level two is focused more on linear sideways movement with less focus on jumping up and down. The free clue and collection clue are both present in this level; the level puzzle focuses on finding a circle with the correct radius based on existing knowledge and revealed clues.

The final level is set in a giant pyramid and focuses almost entirely on upward and downward player navigation. It is relatively freeform with the order a player may collect the collectible triangles. There is a free clue present. For the level puzzle, as a break for the player’s brain to transition toward the end of the game, the puzzle has focused more on ‘fun’ and is a race-to-the-finish style navigation puzzle. The user is presented with a winding linear path around a diamond.

## Development and Major Programming Concepts

This project was developed in Unity using their 2d engine for ease of object and UI creation. 
Custom coding in C# was used to create thirteen different scripts to control game function including but not limited to player movement, dynamic text options for individual NPCs, transition modes between individual levels and sublevels, and individual puzzle programming. Scripts were designed with the specific focus of being malleable and able to be fluidly applied between levels, increasing initial scripting time but reducing the amount of required recoding going forward. 

Prefabs were used in some instances where repeated object iteration would be expected, such as collection puzzles and story puzzles.

This project demonstrates enumeration, encapsulation, access of object parameters through other objects, object instantiation, and polymorphism.
## Project Constraints and Other issues

As this is a one-person project, there are some deficiencies in overall look and feel of the artistic direction for the game. 

In addition, the use of non-professional tilesets with the current movement scheme can lead to rare bugs where the player character can become stuck in an unwinnable state. A ‘reset player location’ function was considered, but ultimately was not included in the final release; instead, level changes were made focusing on reducing the amount of unwinnable states a player could arrive in to a manageable, mitigated level.

## Continued Development

This project is currently in a complete form ready for final release for the purposes of IT Project course. In addition to peer and instructor feedback, future development would aim to accomplish the following additional goals:

•	Construction of a fourth and fifth level

•	Introduction of a basic, unobtrusive storyline

•	Improving physics on movement and dropping

•	Addition of a title menu

•	Custom free music for level backgrounds (currently borrowed from other games)

•	Increase in congruence (when possible) of art direction for entire game (would need paid artists)

•	Introduction of full options menu controlling sound, controls, and help text

