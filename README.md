# Sol's RNG Script for Roblox

Welcome to **Sol's RNG Script**, a robust and easy-to-use Random Number Generator designed specifically for Roblox developers. This script simplifies the process of adding randomness to your games, whether it's for random events, loot drops, procedural generation, or any feature that requires unpredictability.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Generating Random Numbers](#generating-random-numbers)
  - [Generating Random Integers](#generating-random-integers)
  - [Shuffling Lists](#shuffling-lists)
  - [Selecting Random Items](#selecting-random-items)
- [API Reference](#api-reference)
- [Examples](#examples)
  - [Example 1: Random Spawn Location](#example-1-random-spawn-location)
  - [Example 2: Random Loot Drop](#example-2-random-loot-drop)
  - [Example 3: Shuffling NPC Dialogues](#example-3-shuffling-npc-dialogues)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Easy Integration**: Plug-and-play script that works seamlessly with your existing Roblox projects.
- **Versatile Functions**: Provides a variety of randomization functions for different use cases.
- **Optimized Performance**: Lightweight and efficient to ensure minimal impact on game performance.
- **Secure Randomness**: Utilizes Roblox's `Random` object for high-quality random number generation.

## Installation

1. **Download the Script**: Obtain the `SolRNG.lua` script file from [this website](https://dreamophile.com/scripts/top-sols-rng-scripts-for-roblox-in-2024-for-mobile-pc-mac/) or copy the code directly.
2. **Add to Your Game**:
   - Insert a new **ModuleScript** in `ReplicatedStorage` or `ServerScriptService`.
   - Rename the ModuleScript to `SolRNG`.
   - Paste the script code into the ModuleScript.
3. **Require the Module**:
   - In any script where you need randomization, require the module:

     ```lua
     local RNG = require(game:GetService("ReplicatedStorage"):WaitForChild("SolRNG"))
     ```

## Usage

### Generating Random Numbers

Generate a random floating-point number between a minimum and maximum value.

```lua
local randomNumber = RNG:NextNumber(min, max)
```

- `min` *(number)*: The lower bound.
- `max` *(number)*: The upper bound.

### Generating Random Integers

Generate a random integer between a minimum and maximum value.

```lua
local randomInteger = RNG:NextInteger(min, max)
```

- `min` *(integer)*: The lower bound.
- `max` *(integer)*: The upper bound.

### Shuffling Lists

Shuffle the elements of a table.

```lua
local shuffledList = RNG:Shuffle(originalList)
```

- `originalList` *(table)*: The table to shuffle.

### Selecting Random Items

Select a random item from a table.

```lua
local randomItem = RNG:ChooseRandom(itemList)
```

- `itemList` *(table)*: The table from which to select an item.

## API Reference

- **RNG:NextNumber(min, max)**: Returns a random floating-point number between `min` and `max`.
- **RNG:NextInteger(min, max)**: Returns a random integer between `min` and `max`.
- **RNG:Shuffle(table)**: Returns a new table with the elements shuffled.
- **RNG:ChooseRandom(table)**: Returns a random element from the table.

## Examples

### Example 1: Random Spawn Location

```lua
local spawnLocations = {spawnPoint1, spawnPoint2, spawnPoint3}
local randomSpawn = RNG:ChooseRandom(spawnLocations)
player.Character.HumanoidRootPart.CFrame = randomSpawn.CFrame
```

### Example 2: Random Loot Drop

```lua
local lootTable = {"Gold", "Sword", "Shield", "Potion"}
local droppedItem = RNG:ChooseRandom(lootTable)
-- Code to give the item to the player
```

### Example 3: Shuffling NPC Dialogues

```lua
local dialogues = {
    "Hello, traveler!",
    "Good day to you!",
    "Need any assistance?",
    "Stay safe out there."
}
local shuffledDialogues = RNG:Shuffle(dialogues)
npc.Dialogue = shuffledDialogues[1]
```

## Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

**Disclaimer**: This script is provided as-is without any warranty. Use it at your own risk.
