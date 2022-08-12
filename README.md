# MazeGameUpdated

Here are my notes on updates for MazeGame...

Improvements I made for the original MazeGame challenge:
- Separated the Update logic from the HandleCollision logic for the Actors and I see this was done in the updated version of the game as well.
- Added an FPS limiter to limit how often Draw is called (set to 60fps). Same thing for how often Actors are updated (set to once per second).

Issues with the updated version:
- Player movement logic could be broken out of some of the collision logic. This will be tricky since the collision logic handles hitting walls and not being able to move.
- Player can move through any door even w/o the key. Need to uncomment the part of Player.cpp that handles this.
- A new thread is created on the heap and isn't cleaned up. Need to delete this and assign nullptr when done.
- Escape key is not working.
