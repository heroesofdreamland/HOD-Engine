# HoD-Engine

Welcome to **HoD-Engine**, my custom-built game engine written entirely in Python for the open-source roguelike fantasy game *Heroes of Dreamland*. Designed to empower developers to create engaging 2D isometric games, HoD-Engine is a lightweight, flexible, and community-driven platform that prioritizes ease of use, extensibility, and creative freedom. Whether you're a beginner or a seasoned developer, this engine provides the tools to build your dream game without complexity or overhead.

## About HoD-Engine
I created *HoD-Engine* to serve as the backbone for *Heroes of Dreamland*, an open-source roguelike fantasy game. Written in Python, the engine leverages the language’s simplicity and readability to make game development accessible while delivering robust performance. It powers a wide range of features, from isometric map rendering and advanced enemy AI to a modular GUI system and efficient resource management. My goal was to craft an engine that’s not just a tool for my own project but a platform where anyone can experiment, learn, and contribute to game development.

### Key Features
- **Fully Python-Based**: Built from the ground up in Python, ensuring easy-to-read code and a gentle learning curve for developers.
- **Isometric Rendering**: Supports 2D isometric maps with smooth rendering via OpenGL, ideal for roguelike and RPG-style games.
- **Modular GUI System**: A flexible component-based system for creating dynamic and customizable user interfaces.
- **Advanced Enemy AI**: Includes A* pathfinding, line-of-sight checks, and path smoothing for intelligent NPC behavior.
- **Efficient Game Loop**: Manages updates, rendering, and lifecycle events for units, projectiles, and other game objects.
- **Resource Management**: Caches assets like images and sounds to optimize performance.
- **Extensible Architecture**: Designed with modularity in mind, allowing developers to add new mechanics, components, or systems easily.
- **Single-Player Focus**: Optimized for single-player experiences with no multiplayer overhead (at this stage).

The engine currently powers *Heroes of Dreamland*, achieving 100–120 FPS with 40–60 units on the map—a testament to its efficiency despite being written in Python.

## Engine Structure
HoD-Engine is organized into modular components, each handling specific aspects of game functionality. Below is an overview of the key directories and files that make up the engine, based on its core systems.

### Core Engine Components (`logic/core/`)
These files form the foundation of HoD-Engine, handling essential game mechanics and rendering:

- **`animated_object.py`**: Manages animated game objects, enabling sprite-based animations for units and effects.
- **`animation.py`**: Defines animation logic, including frame sequencing and timing for smooth visuals.
- **`background_sound.py`**: Handles ambient audio tracks for immersive game environments.
- **`camera.py`**: Implements a customizable camera system for tracking players or focusing on specific areas.
- **`db_service.py`**: Provides a lightweight database service for storing game data, such as progress or settings.
- **`draw_queue.py`**: Manages the rendering order of objects to ensure correct layering and performance.
- **`game_loop.py`**: The heart of the engine, orchestrating updates, input handling, and rendering in a performant loop.
- **`isometry.py`**: Handles isometric coordinate transformations for map rendering and object placement.
- **`lifecycle.py`**: Manages the lifecycle of game objects (e.g., creation, updates, destruction).
- **`lifecycle_group.py`**: Groups related objects for efficient lifecycle management.
- **`opengl.py`**: Interfaces with OpenGL for hardware-accelerated 2D rendering.
- **`resource_cache.py`**: Caches assets like textures and sounds to reduce loading times and memory usage.
- **`scene.py`**: Manages game scenes, including transitions and object organization.
- **`screen.py`**: Controls screen settings, such as resolution and display modes.
- **`sound.py`**: Handles sound effects for in-game actions and events.
- **`timer.py`**: Provides timing utilities for scheduling events and animations.

### GUI Components (`logic/core/render/components/`)
The GUI system is built on a component-based architecture, inspired by modern UI frameworks, allowing developers to create flexible and reusable interfaces:

- **`animated_image.py`**: Renders animated images for dynamic UI elements.
- **`grid.py`**: Implements a grid layout for organizing UI components in a structured manner.
- **`hstack.py`**: A horizontal stack layout for arranging UI elements side by side.
- **`margin.py`**: Adds spacing around UI components for clean layouts.
- **`opacity.py`**: Controls the transparency of UI elements for visual effects.
- **`rect.py`**: Draws rectangular shapes for UI backgrounds or borders.
- **`static_image.py`**: Renders static images for icons, backgrounds, or other UI assets.
- **`text.py`**: Manages text rendering with customizable fonts and styles.
- **`vstack.py`**: A vertical stack layout for stacking UI elements top to bottom.
- **`zstack.py`**: A depth-based stack for layering UI elements.
- **`color.py`**: Defines color utilities for consistent UI styling.
- **`component.py`**: The base class for all UI components, enabling modularity.
- **`font.py`**: Manages font loading and rendering for text-based UI.
- **`surface.py`**: Provides a rendering surface for compositing UI elements.
- **`types.py`**: Defines data types and structures used across the GUI system.

### Enemy AI (`logic/core/unit_ai/`)
The AI system powers intelligent enemy behavior, making *Heroes of Dreamland* engaging and challenging:

- **`astar_pathfinder.py`**: Implements the A* pathfinding algorithm for efficient navigation around obstacles.
- **`line_of_sight_checker.py`**: Checks whether enemies have a clear line of sight to the player or other targets.
- **`path_smoother.py`**: Smooths AI movement paths for natural and fluid motion.
- **`types.py`**: Defines data types specific to the AI system, such as pathfinding nodes.

### Data Structures (`logic/core/structures/`)
These utilities support the engine’s performance and logic:

- **`priority_queue.py`**: A priority queue implementation for tasks like pathfinding or event scheduling.
- **`queue.py`**: A standard queue for managing ordered tasks or events.

## Why Python?
I chose Python for *HoD-Engine* because of its simplicity, readability, and vast ecosystem of libraries. While Python is not traditionally used for game engines due to performance concerns, I optimized HoD-Engine to achieve high performance (100–120 FPS with 40–60 units) by leveraging OpenGL for rendering and efficient resource management. Python’s accessibility makes it ideal for community contributions, allowing developers of all skill levels to jump in, experiment, and learn without steep barriers.

## Getting Started
To use *HoD-Engine* for your own project or to contribute to *Heroes of Dreamland*, follow these setup instructions.

### Prerequisites
- **Python 3.12**: Ensure Python 3.12 is installed on your system.
- A compatible operating system (macOS, Windows, or Linux).
- Git installed for cloning the repository.

Report any issues on GitHub to help improve the engine!

## How to Contribute
I welcome contributions to *HoD-Engine* and *Heroes of Dreamland*! Here’s how you can get involved:
1. **Code Contributions**: Add new features, fix bugs, or optimize existing systems. Focus areas include new GUI components, AI behaviors, or engine optimizations.
2. **Testing**: Test the engine and report performance issues or bugs.
3. **Documentation**: Improve this README or add in-code documentation for better usability.
4. **Assets**: Contribute sprites, textures, or sounds (ensure they’re open-source or original).

To contribute:
1. Fork the repository.
2. Create a branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m "Add your feature"`).
4. Push to your branch (`git push origin feature/your-feature`).
5. Open a pull request to the `main` or `chaos` branch.

Check my Trello board [Trello](https://trello.com/b/dRa1dr9j/heroes-of-dreamland) for task ideas.

## Development Branches
- **main**: Stable branch for production-ready code. PRs must maintain performance and avoid malicious code.
- **chaos**: Experimental branch for creative or risky features (e.g., anime-style bosses or performance-heavy mechanics). No malicious code allowed.
- **modes**: Planned for custom game modes built on HoD-Engine (details to come).

## Future Plans
I’m working on:
- A website to distribute pre-built versions of *Heroes of Dreamland*.
- A learning program for new developers to get started with *HoD-Engine*.
- Expanding the `modes` branch for custom game modes.
- Further optimizing performance for larger maps and more units.

## Contact
Join my community on [Trello](https://trello.com/b/dRa1dr9j/heroes-of-dreamland) or [X.com](https://x.com/H_o_Dreamland) to discuss ideas, report issues, or collaborate. Let’s build amazing games together with *HoD-Engine*!
