# SNAKE_GAME
1. Game Setup
Uses the turtle module to create a graphical snake game.
The game window (wn) is 600x600 pixels with a white background.
The screen update (wn.tracer(0)) is turned off for smooth animation.

2. Game Elements
Snake Head (head) → White square, starts at the center (0,0).
Food (food) → Random color (red, green, black) and shape (square, triangle, circle).
Scoreboard (pen) → Displays the current score and high score.

3. Movement Controls
The snake moves with "WASD" keys:
W → Up
S → Down
A → Left
D → Right
The direction updates only if it's not opposite to prevent self-collision.

4. Game Logic
a) Boundary Collision
If the snake hits the wall, it resets to (0,0), and the score resets to 0.
The snake's body segments disappear after a collision.
b) Food Collision
If the snake touches the food:
Food moves to a random position.
A new segment is added to the snake's body.
Score increases by 10 points.
Delay decreases to make the game faster.
c) Self-Collision
If the snake hits its own body, the game resets.
All body segments are removed, and the score resets.

5. Game Loop (while True)
Continuously updates the screen.
Moves the snake in the direction set by the user.
Checks for collisions (with walls, food, or itself).
Uses time.sleep(delay) to control the game speed.

6. Infinite Loop & Main Event Handling
wn.listen() → Listens for keyboard input.
wn.mainloop() → Keeps the game running until manually closed.






