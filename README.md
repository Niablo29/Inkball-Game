# **Inkball Game**

## **Overview**
Inkball is a Java-based game developed as part of an assignment for INFO1113 / COMP9003. It uses the **Processing** library for graphics and **Gradle** as a dependency manager. The goal of the game is to direct balls into holes of the same color by drawing lines, while avoiding incorrect matches that reduce the score. Once all balls are successfully captured, the player wins the level.

---

## **Features**
- **Dynamic Gameplay**:
  - Balls spawn with random trajectories and can change color by hitting specific walls.
  - Player-drawn lines direct balls and disappear after a collision.
  - Holes attract balls of the same color, shrinking them until captured.

- **Level Mechanics**:
  - Levels are defined by configuration files and a map layout file.
  - Multiple types of tiles: walls, spawners, holes, and empty spaces.
  - Time limits and score modifiers for additional challenge.

- **Player Controls**:
  - Draw lines with the left mouse button.
  - Remove lines with the right mouse button.
  - Pause the game with the `spacebar`.
  - Restart levels with the `r` key.

---

## **Setup Instructions**

### **Prerequisites**
- **Java 8** (or compatible version)
- **Gradle**
- An IDE such as IntelliJ IDEA or VS Code, or a terminal with Gradle support.

### **Getting Started**
1. Clone the repository:
   ```bash
   git clone https://github.com/Niablo29/Inkball-Game.git
   cd Inkball-Game
   ```
2. Build the project with Gradle:
   ```bash
   gradle build
   ```
3. Run the game:
   ```bash
   gradle run
   ```

---

## **Gameplay Details**
1. **Objective**: Guide balls into holes of the same color by drawing lines.
2. **Game Entities**:
   - **Balls**: Spawn from spawners and move in random directions.
   - **Walls**: Reflect balls; certain walls change their colors.
   - **Holes**: Attract balls of matching color.
   - **Player-Drawn Lines**: Temporarily redirect balls when collided.
3. **Scoring**:
   - Gain points for successfully matching balls with holes.
   - Lose points for incorrect matches.

---

## **Configuration**
The game uses a `config.json` file to manage level properties:
- **layout**: Defines the map layout.
- **time**: Level duration.
- **spawn_interval**: Time between ball spawns.
- **score modifiers**: Adjust score gains and penalties.

---

## **Extensions**
This project implements a modular design that allows adding extensions such as:
- **One-Way Walls**: Allow balls to pass in one direction only.
- **Color-Restricting Walls**: Permit only specific-colored balls.
- **Timed Tiles**: Gradually fade over time.

---

## **Testing**
- Test cases are implemented using **JUnit** to verify game mechanics.
- Use `gradle test` to run all tests.
- A coverage report is generated with JaCoCo using:
  ```bash
  gradle jacocoTestReport
  ```

---

## **How to Play**
1. Launch the game using Gradle.
2. Use the mouse to draw and remove lines:
   - Left click to draw.
   - Right click to erase.
3. Match balls with holes of the same color.
4. Press `spacebar` to pause or `r` to restart.

---

## **Project Structure**
- **`src/main/java`**: Game source code.
- **`src/main/resources`**: Game assets (images, sprites).
- **`src/test/java`**: Unit tests for the game.
- **`build.gradle`**: Gradle configuration file.
- **`config.json`**: Level and gameplay configuration.

---

## **References**
- [Processing Library Documentation](https://processing.github.io/processing-javadocs/core/)
