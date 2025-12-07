# True Cost of a T-Shirt – Game Design

## Overview
* **Genre:** Educational mini-game series with world-map progression.
* **Levels:** 5 sequential stages unlocked one at a time.
* **Platform assumptions:** 2D tilemap navigation with sprite-based interactions and simple input (directional movement + button A/B).

## Core Loop
1. Navigate the world map tilemap to the next unlocked level icon.
2. Enter the level (press **A** while on icon).
3. Make choices that affect the **CO₂ bar**; avoid filling it.
4. Complete level objectives to unlock the next icon; automatically walk to it.
5. After Level 5, show end screen with cumulative results and restart option.

## Global Systems
* **CO₂ Bar:** Visible at the top of the screen in every level; rises or falls based on player actions. If the bar hits max, trigger **Game Over**.
* **Negative Feedback (bad choices):**
  * Brief screen shake.
  * Play a “bad sound” (buzz/low rumble).
  * Darken background with a moody overlay.
* **Positive Feedback (good choices):** Soft chime sound.
* **Level Completion:** After each level, present a text quote containing a CO₂ fact before returning to the world map.

## World Map
* Tilemap-based overworld with level icons.
* Only the next level is unlocked; others remain inactive.
* When a level is completed, the player sprite auto-moves to the next icon.
* Press **A** on the current icon to load its level.

## Level Specifications
### Level 1 – Materialer (Materials)
* **Environment:** Factory with fabric rolls; beige/textile tones.
* **Gameplay:** Catcher mechanic—good materials (cotton, recycled) and bad materials (polyester, chemicals) fall from above.
* **CO₂ Impact:** Catching good items lowers the bar; bad items raise it.

### Level 2 – Produktion (Production)
* **Environment:** Factory with machinery.
* **Gameplay:** Choose between three machine sprites via A/B button prompts.
* **CO₂ Impact:** Energy-efficient choices lower the bar; energy-heavy choices raise it.

### Level 3 – Transport
* **Environment:** World map with sea, clouds, land.
* **Gameplay:** Select transport mode: ship, truck, or plane.
* **CO₂ Impact:** Plane = large increase; truck = medium; ship = small.

### Level 4 – Brug (Use)
* **Environment:** Laundry room/bathroom.
* **Choices:**
  * Wash temperature: 30/40/60.
  * Drying method: air vs. tumble dry.
  * Detergent: mild vs. normal.
* **CO₂ Impact:** Each decision modifies the bar. T-shirt sprite visibly wears down as use increases.

### Level 5 – Affald (Waste)
* **Environment:** Recycling center.
* **Gameplay:** Five T-shirt sprites appear sequentially in various conditions. Stations: repair, upcycle, donate, recycle, trash. Player walks to a station and presses **A**.
* **CO₂ Impact:** Choice affects the bar based on T-shirt condition (trash is worst).

## Assets
* Sprites: player, falling materials, machine set, transport vehicles (truck/ship/plane), washing icons, T-shirt wear states, recycling stations, level icons.
* Backgrounds: factory (materials), factory/machines, world map, laundry room, recycling center.

## Audio & Effects
* **Positive:** Soft chime for good choices.
* **Negative:** Buzz/low rumble for bad choices, coupled with screen shake and darkened overlay.

## End Screen
* Display total CO₂ tally and feedback text with improvement tips.
* Prompt: “Press A to restart.”
