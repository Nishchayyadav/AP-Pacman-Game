# Stick Hero - GUI Game

## Overview

This repository contains the implementation of the game Stick Hero as part of the AP Project. The game was developed by Group 94, consisting of Nishchay Yadav (2022332) and Shaurya Bajaj (2022474).

## Running the Game

To launch the game via the terminal, navigate to the `AP_Project_Stick_Hero` directory and run the following Maven command:

```bash
mvn clean javafx:run
```

## Main Game Implementation

Stick Hero is a game where players traverse platforms using extendable sticks. By holding the left mouse button, the player can extend a stick to bridge gaps between platforms. Players can collect cherries, which contribute to their score and can be used for revivals after collecting five cherries. The game also features a save functionality, allowing users to save their progress and high score.

## Design Patterns

### Singleton
- **Used in**: `ScoreManager` class
- **Purpose**: Ensures there is only one instance managing the score and high score in the game.

### Flyweight
- **Used in**: Game elements
- **Purpose**: Ensures that pillars of the same width are not repeatedly created during gameplay.

## JUnit Tests

JUnit tests are contained in the `TestInput` class, with the runner class being `RunnerClass`. The tests cover:
- Verification of `ScoreManager` as a singleton.
- Successful and unsuccessful collision detections.
- Proper implementation of the flyweight design pattern in pillars.

## Bonus Features

1. **Multithreading**
   - **Implemented in**: `AudioManager` class
   - **Purpose**: Ensures sounds are played correctly and at the appropriate times for each event.
   
2. **Bonus Feature**
   - **Description**: A monster is added to each level. The player must avoid the monster by flipping the character. Collision with a monster results in instant death, without the possibility of revival.

## Conclusion

This project provided valuable experience in game development, design patterns, and multithreading in Java. We hope you enjoy playing Stick Hero and exploring its features.
