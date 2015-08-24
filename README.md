# Hello-World
Dungeon game created for a college course



Project 3 Report (Minirogue)


•	How to play:
o	To win Minirogue, you must pick up the golden idol (&) that is placed randomly on dungeon level 5 without dying.

o	Movement: 
•	The arrow keys allow the player (@) to move around the dungeons. Each time the player moves, there is a 1 in 10 chance that the player will heal one life point. 
•	Attacking: To attack enemies, move into them as if you were going in that certain direction. Often times after killing an enemy, the enemy will drop a weapon or scroll.  
•	Picking up objects: To pick up an item, move the player over it and press ‘g’.
•	Checking inventory:
•	For Weapon: Press ‘w’ for wield and then press the letter for which weapon.
•	For scroll: Press ‘r’ for read and then press the letter for which scroll.
•	For just looking: Press ‘i’ for inventory.
•	To delete a weapon from the inventory, press ‘D’ while in inventory and then select the letter corresponding to the weapon. 
•	Going on to the next level: To advance player to the next level, move over the ‘>’ symbol and press ‘>’. 
 
o	Dungeons: 
•	Each dungeon/level has enemies, weapons and scrolls placed at random points. Each level, not including the 5th and final level, also has a staircase (>) that takes you to the next level. Each dungeon is unique and created randomly using a range of rooms and corridors by the computer. It is the player’s job to navigate each dungeon by killing enemies and using objects in order to pick up the golden idol on level 5.


o	Symbols:
•	@ - The player (user)
•	( - The symbol for a weapon
•	? - The symbol for a scroll
•	B, S, G, D, M - Bogeyman, Snakewomen, Goblin, Dragon, Mage 
•	> - Staircase to next level
•	& - Golden Idol
•	# - Wall
•	* - Infinity Blade (Rare weapon)
•	| - Deadly Katana (Rare weapon)

o	Statistics
•	Dungeon Level/Secret Level:
•	This stat shows what level you are currently on. Secret levels are levels post golden idol level (level 5). Levels go up to around 600.
•	Life Points: 
•	This stat shows the players current life points. The player starts with 20. Can be increased by scroll of health.
•	Armor: 
•	Armor is the player’s defense. When attacking an enemy, armor helps you take less damage. Can be increased by scroll of enhance armor.
•	Strength:
•	Strength is how much damage the player can do to enemies. The higher the strength, the more damage the player can deal to enemies. Can be increased by scroll of enhance strength. 
•	Dexterity:
•	Dexterity is the chances you will be hit by an enemy rather than missed as well as the chances you will hit enemies rather than missing. Can be increased by scroll of enhance dexterity. 

o	Enemies
•	Bogeyman: 
•	Smell Distance: 7
•	Health: 10 to 15
•	Weapon: Mace 
•	Armor: 2
•	Strength: 2 to 3
•	Dexterity: 2 to 3

•	Snakewomen:
•	Smell Distance: 6
•	Health: 5 to 8
•	Weapon: Magic Fangs
•	Armor: 2
•	Strength: 2 
•	Dexterity: 1

•	Dragon:
•	Smell Distance: 1
•	Health: 20 to 25
•	Weapon: Magic Axe
•	Armor: 4
•	Strength: 4
•	Dexterity: 4

•	Goblin:
•	Smell Distance: 18
•	Health: 20 to 25
•	Weapon: Short Sword
•	Armor: 1
•	Strength: 3
•	Dexterity: 1

•	Mage:
•	Smell Distance: 30
•	Health: 5 to 7
•	Weapon: Infinity Blade
•	Armor: 1
•	Strength: 1
•	Dexterity: 2

o	Game Objects (Scrolls and Weapons)
•	Weapons
•	Short Swords
o	Damage: 2
o	Dexterity: 0

•	Mace
o	Damage: 3
o	Dexterity: 1

•	Long Sword
o	Damage: 4
o	Dexterity: 2

•	Magic Axe
o	Damage: 5
o	Dexterity: 5

•	Magic Fangs
o	Damage: 2
o	Dexterity: 4
o	Sleeping Powers. Weapon has a 1 in 5 chance of putting an actor to sleep if actor is hit. 

•	Infinity Blade
o	Damage: 10
o	Dexterity: 10

•	Duel Infinity Blades (Weapon can be duel wielded if player holds 2 or more in his/her inventory)
o	Damage: 20
o	Dexterity: 20

•	Godly Katana
o	Damage: 5
o	Dexterity: 40

•	Duel Godly Katana (Weapon can be duel wielded if player holds 2 or more in his/her inventory)
o	Damage: 10
o	Dexterity: 80

•	Scrolls
•	Scroll of Teleportation
o	Moves player to a random spot on the dungeon.

•	Scroll of Enhance Armor
o	Increases player armor by 1 to 3.

•	Scroll of Strength
o	Increases player strength by 1 to 3.

•	Scroll of Enhance Health
o	Increases player health by 3 to 8.

•	Scroll of enhance Dexterity
o	Increases player dexterity by 1.

o	Cheats (MUHAHAHA)
•	The ‘c’
•	Pressing ‘c’ will give you a max health of 50 rather than 20 and will increase your strength to 9. 
•	Free Infinity Blade
•	Pressing ‘*’ will automatically give you the rare and powerful infinity blade. 
•	Free Godly Katana
•	Pressing ‘|’ will automatically give you the rare and effective godly katana. 
•	Guide to the Further (cheat for secret levels)
•	Pressing ‘$’ will bring up a prompt asking which level you want to teleport to. This gives you access to the secret levels beyond level 5. Secret levels get extremely hard and go up to around 600. 


•	My goblin movement function is not recursive. I was not able to successfully implement a recursive goblin search function that ran fast enough and flawlessly enough. 

•	Program Design: 
o	Actor Class:
•	My Actor class has all the functions that deal with the actors, which include all the monsters and the player. This class includes object and dungeon pointers, the move function, the attack function, the drop object function, the move monster function and many other small functions that deal with actors in the game. The Actor class is a base class with 6 derived classes. Each derived class is a different actor, including the player and 5 different monsters. 
o	Game Class:
•	My Game class has a constructor, destructor and play function. The constructor takes one argument, which is the goblin smell distance for the recursive algorithm. The play function is the function that actually runs the game and that is included in Game.cpp. My game class private members include a Dungeon pointer array, which has each level of dungeon that is used in the game, a current level integer and a smell integer that would be used by the goblin recursive function. 
o	Object Class:
•	My Object class deals with all the weapon and scroll implementations used by the game. This class includes constructors for weapons, scrolls and the idol, and has a large amount of accessors that return data about each weapon or scroll. The object class is a base class with 14 derived classes, which are the various objects in the game. Each derived class has a default constructor and a constructor that places the object on a particular spot in the dungeon. 
o	Dungeon Class:
•	My Dungeon class contains all the functions that make and control each dungeon that is made in the game. The dungeon class has pointers to the player and the monsters, which help connect the dungeon with the actors. The dungeon class makes the rooms and corridors, places the actors, places the objects and is responsible for making sure the game runs as desired with correct rules and physics. (Can’t walk through walls, through other actors, out of the map, etc) The dungeon class also places the idol on the last level of the game and ends the game if the idol is picked up. 



•	Non-trivial algorithms:
o	Bool Actor::move(char dir, string& act)
•	Checks if the movement is for the player or for a monster using the char dir argument. If it is a monster, call the movePlace function, which handles the monster movement. Depending on the char dir, check if moving that direction is doable. If the movement is doable, change the position of that actor. If there is a monster or player in that direction of move, call attack function. Return true if it is an attack and false otherwise. 
o	Void Actor::attack(int r, int c, string& at)
•	If the attacking spot contains the player, make a pointer to the player. Use the attack algorithm provided by the project info. If weapon is a magic fang, make it possible to put player to sleep. Display a message either saying hit or miss.
o	Bool Player::displayInvent(char key, string& str)
•	This function clears the screen and then displays the inventory if a ‘w’, ‘r’ or ‘i’ is pressed. It then creates an iterator that picks which object the user has chosen. This function also creates a message saying what the user chose and whether they it did anything or not. 
o	Void Player::attack(int r, int c, string& at)
•	This function is similar to the attack function for actor. If the attacking spot contains a monster, make a pointer to the monster. Use the attack algorithm provided by the project info. If weapon is a magic fang, make it possible to put monster to sleep. Display a message either saying hit or miss.
o	Void Game::play()
•	Create a player pointer and set message bools. Check for dead actors, heal the player, clear the screen and display the current dungeon display and current player or comp message. Get the keyboard input and either display the inventory, cheat, move the player or move the player to the next level. If q is pressed, quit the game. Decrement the sleeping turns of the player and actors and repeat while the player is alive. If game is over, let q quit the program. 
o	Bool Dungeon::makeRoom(int &row, int &col)
•	Create x and y dimensions and row and col spots for the room. Iterate through the room dimensions and see if the rooms fit. If they fit, make the rooms by making the characters at those spots ‘ ‘. Increment the number of rooms added and repeat until all the rooms are added. 
o	Void Dungeon::make()
•	While there aren’t enough rooms in the dungeon, make a room by calling the makeRoom function. If the most recent room fit and there are more than one room made, make a corridor between the rooms by using the coordinates of the previous and most recent rooms. Once all the rooms have been made, add the objects and add the monsters to the dungeon level. If this is the last level, place the idol, if not, place the stairs. 
	


•	Known Bugs
o	Did not implement the recursive goblin search
	
