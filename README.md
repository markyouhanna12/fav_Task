# fav_Task
Design a C++ program to simulate a fight between Batman and the Joker using OOP principles.

# Superhero Battle Game

This project is a console-based game that simulates a battle between two superheroes: Batman and Joker. Each superhero has a set of weapons and shields, and they take turns attacking and defending until one of them runs out of health.

## Classes

### 1. `Super_hero`
This class represents a superhero with the following attributes:
- **`sup_Name`**: Name of the superhero.
- **`sup_Health`**: Health points of the superhero (initially set to 100).
- **`sup_Energy`**: Energy points of the superhero (initially set to 500).

### 2. `Superhero_Weapons`
This class represents a weapon used by a superhero with the following attributes:
- **`weapon_Name`**: Name of the weapon.
- **`consumed_Energy`**: Amount of energy consumed when the weapon is used.
- **`weapons_damage`**: Damage points inflicted by the weapon.
- **`weapons_Use`**: The number of times the weapon can be used.

### 3. `Superhero_Shield`
This class represents a shield used by a superhero with the following attributes:
- **`Shield_Name`**: Name of the shield.
- **`Shield_Energy`**: Amount of energy consumed when the shield is used.
- **`Shield_Save`**: Percentage of damage reduced by the shield.
- **`Shield_Use`**: The number of times the shield can be used.

## Game Flow

1. **Initialization**:
   - Two superheroes are created: Batman and Joker.
   - Each superhero is assigned a set of weapons and shields with their respective attributes.

2. **Starting the Game**:
   - The user chooses which superhero will start the game.
   - The game alternates turns between the chosen superheroes (Batman and Joker) until one of them runs out of health (`sup_Health <= 0`).

3. **Attack Phase**:
   - The active superhero (the one whose turn it is) chooses a weapon to attack.
   - The weapon's usage count (`weapons_Use`) is decreased by 1, and the energy (`sup_Energy`) is reduced by the amount specified by `consumed_Energy`.
   - If the superhero runs out of energy or weapon usage, they are prompted to choose another weapon.

4. **Defense Phase**:
   - The defending superhero chooses a shield to reduce the incoming damage.
   - The shield's usage count (`Shield_Use`) is decreased by 1, and energy (`sup_Energy`) is reduced by the amount specified by `Shield_Energy`.
   - The incoming damage is calculated based on the weapon's damage and the shield's saving factor (`Shield_Save`).

5. **Turn Switching**:
   - Once the attack and defense phases are completed, the turn switches to the other superhero.

## Important Parts of the Code

- **Lines 5-22**: Definition of the `Super_hero` class that initializes the attributes of the superheroes.
- **Lines 24-34**: Definition of the `Superhero_Weapons` class that represents the weapons of the superheroes.
- **Lines 36-46**: Definition of the `Superhero_Shield` class that represents the shields of the superheroes.
- **Lines 48-61**: Initialization of the superheroes, Batman and Joker, with their respective health and energy levels.
- **Lines 64-106**: Initialization of Batman's weapons and shields with their respective properties.
- **Lines 108-152**: Initialization of Joker's weapons and shields with their respective properties.
- **Lines 154-160**: User input for selecting the starting superhero (Batman or Joker).
- **Lines 162-391**: Main game loop that alternates turns between Batman and Joker, allowing them to attack and defend.
  - **Lines 169-303**: Batman's turn to attack and Joker's turn to defend.
  - **Lines 308-391**: Joker's turn to attack and Batman's turn to defend.
- **Lines 393 and beyond**: Repeat the loop until one superhero's health reaches zero.

## How to Run

1. Compile the code using any C++ compiler.
2. Run the executable file.
3. Follow the prompts to choose which superhero starts the game and select the weapons and shields during the gameplay.

## Notes

- The game ends when either Batman or Joker's health reaches zero.
- The player can keep track of the remaining health and energy of each superhero, as well as the usage count of weapons and shields.

