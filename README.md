# Snake Game Using HTML Canvas and Pure JS
 [DEMO](https://s3.ap-south-1.amazonaws.com/www.experiencethered.in/snake.html)

 There are 3 main components of the game:
 1. The play area - canvas
 2. The snake
 3. The food for the snake
 
 We have to take care of few edge cases or the basic know-how of the game:
 1. The snake should be able to move in all directions -left,right,bottom and up
 2. The food should be present at random positions but not on snake.
 3. The snake should grow as it eats the food.
 4. On any collision the game should end.
 
 ## Playarea
 I have used HTML5 Canvas([HTML5 Canvas](https://www.w3schools.com/graphics/canvas_intro.asp)) for creating the game area.
 
 ## Drawing the snake
 Instead of using one rectangle for creating the snake,I have used 5 small blocks of (10px,10px) each for the snake
 
 ## Moving the snake
 For moving the snake, we need to increase or decrease (depending on the direction) the position.
 For instance,
 * if right key is pressed increase the x-coordinate by 10px(it could be anything, just decide on a displacement).
 * if left key is pressed decrease the x-coordinate by 10px
 * if up arrow key is pressed decrease the y-coordinate by 10px
 * if down arrow key is pressed increase the y-coordinate by 10px
 
 ## Generating Food
 Use Math.random() to generate any(x,y) positions inside the canvas.
 
 ## Growing the snake
  If the x and y coordinates of the snake head equals the x and y coordinates of food, that means snake has eaten the food.So at this point do not pop out the snake part(refer code).
  
 ## Collision
 There could be 2 types of collision-
 1. Self: possible only if the snake has more than 3 parts.We can check of coordinates of any part collides with the head part of the snake.If it does, game ends.
 2. Collision with the walls: check if the snake collides with the boundary.If it does, game ends
