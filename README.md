# 🚀 **Alien Invasion Defense** 🛸

##Star this repo

Welcome to **Alien Invasion Defense**, a fast-paced, space-themed shooting game! Defend your base from waves of relentless alien invaders and become the ultimate defender of the galaxy. 🌌 With sleek, modern UI, intuitive controls, and immersive gameplay, get ready for an epic battle. Use your powerful weapons to destroy alien ships, survive multiple waves, and protect your base with your three lives. 👾

---

## 🌟 **Features**

✨ **Alien Invasion Gameplay**: Defend against waves of attacking alien spaceships.
  
🎮 **Side Rules & Controls**: Easily restart the game, view your score, and track remaining lives on the side panel.

💥 **3 Lives to Survive**: Protect your base with only 3 chances!

🚀 **Smooth Firing Mechanics**: Enjoy accurate and responsive shooting to take down aliens.

🖥️ **Modern UI**: A visually appealing, easy-to-navigate game interface.

🔄 **Quick Restart Option**: Reset and replay the game in one click.

🏆 **Leaderboard Integration (Optional)**: Track your highest scores and compete with others.

---

## 🎮 **How to Play**

1. **Start the Game**: Press the "Start" button to launch the game and start your defense.
2. **Move and Shoot**: Use your keyboard or on-screen controls to maneuver your spaceship and fire at the approaching alien ships.
3. **Lives**: You have 3 lives to defend your base. Lose a life if an alien reaches your base or if your spaceship gets hit.
4. **Game Over**: The game ends when all 3 lives are lost. Press "Restart" to try again.
5. **Win**: Destroy all alien ships in a wave to proceed to the next level and rack up your score.

---

## 📜 **Game Rules**

- **Survive as long as possible** by shooting the alien invaders and defending your base.
- **You have 3 lives**. If an alien reaches your base or your ship gets hit 3 times, the game ends.
- **Restart anytime** using the "Restart" button.
- **Fire away** to destroy alien ships. Be precise to keep your base safe!
- **Earn points**: Each alien ship destroyed adds to your score. Aim for the highest score possible before you lose all lives!

---

## 🛠️ **Tech Stack**

This game is built using:

<a href="https://skillicons.dev">
    <img margin="8px" src="https://skillicons.dev/icons?i=html,css,js" />
</a>

---

## 🚀 **How to Run Locally**

To play the game on your local machine, follow these simple steps:

1. **Clone this repository** to your local machine:
   ```bash
   git clone https://github.com/YOUR_GITHUB_USERNAME/Alien-Invasion-Defense.git

2. Navigate to the project folder and open the `index.html` file in your browser.
3. Start defending your base against the alien invasion!

---

## 🔮 Future Enhancements

- **More Levels**: Introduce advanced levels with stronger and faster alien enemies.
- **Sound Effects**: Add background music and sound effects to enhance the game atmosphere.
- **Mobile Optimization**: Improve the gameplay experience for mobile users.

---

## 🤝 Contributing

We welcome all contributions to enhance the **Alien Invasion Defense** game! If you'd like to help out:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Open a pull request.

---

## explanation of key sections:

1. Element Selection

The game grabs several HTML elements using document.getElementById():

	•	canvas: The area where the game is drawn.
	•	ctx: The 2D context for drawing on the canvas.
	•	Other elements like scoreElement, levelElement, livesElement, and buttons for starting, pausing, and restarting the game.
	•	volumeSlider: A slider to control the background music volume.
	•	Audio elements like backgroundMusic and hitSound are also selected for background music and sound effects.

2. Classes for Game Objects

	•	Player: The player-controlled spaceship. It has methods to draw itself as a triangle, move based on keyboard inputs, and adjust its speed. It also handles shooting bullets.
	•	Alien: Represents the enemies. Aliens move down the screen and the game increases their speed based on the level. Each alien uses a preloaded image.
	•	Bullet: Represents the projectiles the player shoots. Bullets move upwards and can collide with aliens.
	•	Particle: Particles are created when an alien is destroyed. They have random properties for size, color, and speed to create an explosion effect.
	•	PowerUp: Power-ups are bonuses the player can collect. In this case, a power-up can temporarily boost the player’s speed.

3. Game Initialization (initGame)

	•	This function resets the game’s state and initializes key variables: score, level, lives, and arrays for aliens, bullets, particles, and powerUps.
	•	It calls spawnAliens() to create the initial set of alien enemies and sets up the volume control slider for background music.

4. Game Mechanics

	•	Movement: The player moves left and right based on key presses (ArrowLeft, ArrowRight, KeyA, KeyD), and aliens move down the screen.
	•	Shooting: The player can shoot bullets by pressing the spacebar or clicking. Bullets are added to an array and move upwards on the canvas.
	•	Collision Detection: The checkCollision() function is used to detect whether objects (like bullets and aliens, or the player and power-ups) overlap.
	•	Particles: When an alien is destroyed by a bullet, particles are created for a visual explosion effect.

5. Spawning Aliens and Power-Ups

	•	Aliens: Aliens are spawned in random positions using spawnAliens(). Their speed increases with the level.
	•	Power-Ups: Every 5 seconds, the spawnPowerUp() function creates a power-up that moves down the screen. If the player collects it, they gain a temporary speed boost.

6. Game Loop (update)

	•	The update() function is the core game loop. It:
	•	Clears the canvas.
	•	Moves and draws the player, aliens, bullets, and particles.
	•	Handles collisions between bullets and aliens, as well as between the player and power-ups.
	•	Adjusts the score and level, respawning aliens as needed.
	•	Continues updating the game as long as it is active and not paused.

7. Handling Game States

	•	Game Over: When the player loses all lives, the gameOver() function is called. It stops the game, displays a “game over” message, and checks if the player achieved a high score.
	•	Pause/Resume: The game can be paused by pressing the Escape key. The saveGameState() function stores the current game state, and restoreGameState() resumes it when unpaused.

8. Keyboard and Mouse Controls

	•	The player can move left and right using the keyboard, shoot bullets with the spacebar or mouse clicks, and swipe on mobile devices to move the player horizontally.
	•	The keydown and keyup event listeners handle continuous movement and shooting. Shooting is rate-limited to avoid firing too quickly.

9. Touch Controls for Mobile

	•	Touch events (touchstart and touchend) are added for mobile devices to allow the player to move the spaceship by swiping and shoot by tapping.

10. Volume Control

	•	The volumeSlider controls the volume of the background music in real-time. It listens for input changes and adjusts the backgroundMusic.volume property.

11. Start, Pause, and Restart Buttons

	•	Start: Clicking the “start” button begins the game, hides the start button, and starts the background music.
	•	Pause: Pausing the game saves the current game state, hides the pause button, and stops the background music.
	•	Restart: Clicking the “restart” button resets the game, hides the game-over screen, and resumes the game from the start.


### Made with ❤️ for all space defenders!
