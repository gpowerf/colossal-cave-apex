# colossal-cave-apex
Colossal Cave APEX: Classic Adventure with an AI Twist

This project aims to recreate the iconic *Colossal Cave Adventure* in Oracle APEX — but with a modern edge: natural language input powered by an LLM like DeepSeek or GPT.

The goal is to **stay true to the original structure and logic of the game**, while enabling users to interact using free-text input. The LLM interprets their intent and returns structured commands for APEX to process.

---

## Project Vision

- **Classic gameplay**, modern interface
- **Text input powered by LLMs** (DeepSeek, GPT, or others)
- Structured **PL/SQL game engine** behind the scenes
- Optional AI-powered **narration or hints**
- Modular design — start simple, evolve over time

---

## Planned Architecture

1. **Oracle APEX UI**
   - Game text window
   - Free-text input
   - Optional command buttons for testing

2. **Backend Game Engine (PL/SQL)**
   - Tables for rooms, items, and player state
   - Core game logic (movement, inventory, puzzles)

3. **LLM Integration**
   - REST call to external model (e.g., DeepSeek API)
   - LLM parses natural language into JSON commands
   - APEX processes JSON with game engine

4. **Example AI Prompt (WIP)**

```plaintext
You are the command interpreter for a classic text adventure game.

Game State:
- Room: Hall of the Mountain King
- Exits: [north, south, west]
- Items: [golden egg, torch]
- Inventory: [brass lantern, map]

Player Input: "Grab the egg and go west."

Output:
[
  { "command": "take", "target": "golden egg" },
  { "command": "move", "direction": "west" }
]
