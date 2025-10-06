# Godot Tactical Shooter Player Template


This repository provides a ready-to-use player implementation for Godot 4.5. The entire controller and supporting resources are self-contained in the `Scenes/Player` folder and can be copied directly into your own Godot projects.

## Features

- Player movement and aiming
- Shooting input and basic weapon example
- Camera helper (camera shake)
- Example textures and imports included in `godot-prototype-texture`
- Easy integration: simply copy the `Scenes/Player` folder into your project

## Quick Start / Setup

1. Copy the Player Folder

	- The `Scenes/Player` folder contains everything you need for the player (scene, scripts, textures).
	- Copy the entire `Player` folder into your own Godot project's `Scenes` folder (keep the folder structure).


2. Add the Player Scene to Your World

	- In your main scene, instance `player.tscn` from `Scenes/Player` and position it in the world.

3. Input Map Setup

	- The following input actions are required (already set in this template's `project.godot`):
	  - `forward` (default: W)
	  - `backward` (default: S)
	  - `left` (default: A)
	  - `right` (default: D)
	  - `shoot` (default: Left mouse button)
	  - `leanLeft` (default: Q)
	  - `leanRight` (default: E)

	- If you copy the controller into a new project, make sure to add these actions in Project > Project Settings > Input Map.

4. Test the Player

	- Open the project in Godot 4.5, instance the player scene into your world, press Play. Use WASD to move and left mouse to shoot.

## How It Works

- The player scene is `player.tscn` and the main script is `Player.gd` (attached to the root player node).
- Movement and input are read from the Input Map actions listed above.
- Camera shake is implemented in `cameraShake.gd` and used by the player when appropriate.
- The included textures are in `godot-prototype-texture` and should be copied along with the Player folder if used.

## Folder Structure

```
Scenes/
  Player/
	 Player.gd         # Main controller script
	 player.tscn       # Player scene (instance this into your world)
	 cameraShake.gd    # Camera shake helper
	 textures/         # Example textures used by the player
godot-prototype-texture/
  PNG/               # Prototype textures
  Vector/            # Vector textures
project.godot        # Project settings (input map + folder color)
```

## Customization

- Movement speeds, aim sensitivity, and camera shake parameters are exposed as exported variables in `Player.gd` and `cameraShake.gd`. Tweak them in the Inspector to match your game feel.
- You can replace the sample weapon logic with your own weapon system; `player.tscn` already demonstrates basic shooting input.

## Credits

Created by [RasyaDevansyah](https://github.com/RasyaDevansyah)
Pistol Model by [j_albert05](https://www.instagram.com/j_albert05)
---

Feel free to copy this `Scenes/Player` folder into your own Godot projects and adapt it.
