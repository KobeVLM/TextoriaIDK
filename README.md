# Text-Based RPG

Welcome to the Text-Based RPG! This game is a console-based adventure inspired by classic text-based games and manga-style storytelling.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [How to Play](#how-to-play)
- [File Structure](#file-structure)
- [Dependencies](#dependencies)
- [Credits](#credits)

## Introduction
This project is a text-based RPG where players can embark on an epic adventure. The game includes rich storytelling, character development, quests, and various interactive elements.

## Features
- **Character Management**: Create and manage your hero.
- **Inventory System**: Collect and use items.
- **Combat System**: Engage in battles with enemies.
- **Quests and Achievements**: Complete quests and earn achievements.
- **Dialogue and Choices**: Interact with NPCs and make choices that affect the story.
- **Crafting System**: Craft items using collected materials.
- **Companion System**: Recruit and manage companions.
- **Dynamic Weather**: Experience changing weather conditions.
- **Lore and Collectibles**: Discover lore items and collectibles.
- **Mini-Games**: Enjoy fun mini-games for rewards.

## Installation
1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/text-based-rpg.git
    cd text-based-rpg
    ```
2. **Add dependencies**:
    - Download the following `.jar` files and place them in the `lib` directory:
      - [Gson](https://github.com/google/gson/releases)
      - [JUnit](https://junit.org/junit4/)
      - [Apache Commons IO](https://commons.apache.org/proper/commons-io/)

3. **Compile the project**:
    ```sh
    javac -d bin src/com/yourgame/**/*.java
    ```

4. **Run the game**:
    ```sh
    java -cp "bin:lib/*" com.yourgame.main.Game
    ```

## How to Play
1. **Start the Game**: Run the main class to start your adventure.
2. **Create a Hero**: Follow the prompts to create your hero.
3. **Explore**: Navigate the game world, interact with NPCs, and embark on quests.
4. **Combat**: Engage in battles and use your inventory items strategically.
5. **Progress**: Complete quests, level up, and uncover the story.

## File Structure
```plaintext
/src
  ├── main
  │   └── Game.java - Entry point of the game, initializes and starts the game.
  ├── characters
  │   ├── Character.java - Base class for all characters (common attributes and methods).
  │   ├── Hero.java - Subclass representing the player (specific attributes and methods for the hero).
  │   └── Enemy.java - Subclass representing enemies (specific attributes and methods for enemies).
  ├── items
  │   ├── Item.java - Base class for all items.
  │   ├── Weapon.java - Subclass for weapons (additional attributes like damage).
  │   ├── Armor.java - Subclass for armors (additional attributes like defense).
  │   └── Potion.java - Subclass for potions (additional attributes like healingAmount).
  ├── game
  │   ├── GameLogic.java - Manages core game mechanics and flow.
  │   ├── Combat.java - Handles combat mechanics.
  │   ├── LevelUpSystem.java - Manages leveling up and stat increases.
  │   ├── Shop.java - Manages buying and selling items.
  │   ├── EventManager.java - Handles random or scheduled in-game events.
  │   ├── Inventory.java - Manages player's inventory items.
  │   ├── Achievements.java - Tracks and manages player achievements.
  │   ├── NPC.java - Manages interactions with non-playable characters.
  │   ├── World.java - Manages the game world and locations.
  │   └── Map.java - Represents the game map for navigation.
  ├── quests
  │   ├── Quest.java - Represents a single quest.
  │   ├── QuestManager.java - Manages the list of quests and their status.
  │   └── QuestStatus.java - Enum for quest statuses (e.g., NOT_STARTED, IN_PROGRESS, COMPLETED).
  ├── dialogue
  │   ├── Dialogue.java - Represents a dialogue sequence.
  │   └── Choice.java - Represents a choice in a dialogue with an associated outcome.
  ├── constants
  │   ├── Paths.java - Defines static paths used in the game.
  │   ├── Messages.java - Holds static string messages.
  │   └── GameSettings.java - Stores various game settings and thresholds.
  ├── util
  │   └── FileManager.java - Handles loading and saving game data.
  ├── crafting
  │   └── CraftingSystem.java - Manages crafting recipes and processes.
  ├── world
  │   └── Weather.java - Manages weather conditions and effects on the game.
  ├── companions
  │   ├── Companion.java - Represents a companion character with unique abilities.
  │   └── CompanionManager.java - Manages recruiting and interactions with companions.
  ├── lore
  │   ├── LoreItem.java - Represents a lore item with historical significance.
  │   └── Collectible.java - Represents collectible items scattered throughout the game world.
  └── minigames
      ├── MiniGame.java - Base class for mini-games.
      └── CardGame.java - Example of a mini-game.
