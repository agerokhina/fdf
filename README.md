# FdF (Fil de Fer) — 42 School Project

**FdF** is a graphical project developed as part of the 42 School curriculum. It visualizes height maps in 3D using wireframe rendering.

## Project Structure

```
.
├── src/          # Source code
├── include/      # Header files
├── lib/          # External libraries (including MLX42)
├── test_maps/    # Example map files for testing
├── Makefile      # Main Makefile for building the project
├── README.md     # Project documentation
└── .gitignore    # Git ignore rules
```

## About the Project

FdF reads a map file describing a 3D terrain and displays it as a wireframe model. The project demonstrates understanding of file I/O, data structures, 3D mathematics, and graphics programming.

## MLX42 Library

This project uses the [MLX42](https://github.com/codam-coding-college/MLX42) library as an external dependency for graphics rendering. MLX42 is a modern C graphics library based on GLFW and OpenGL, designed for 42 School projects.

### How MLX42 is Used
- All window creation, drawing, and event handling is done via MLX42.
- The library is included as a submodule or external folder in `lib/MLX42`.
- The project links against MLX42 during compilation (see `Makefile`).
- You do not need to install MLX42 system-wide; it is built and used locally within the project.

## Building the Project

1. Clone the repository **with submodules** (to include MLX42):
   ```sh
   git clone --recurse-submodules <https://github.com/agerokhina/FDF.git>
   cd fdf
   ```
   If you already cloned without `--recurse-submodules`, run:
   ```sh
   git submodule update --init --recursive
   ```
2. Build the project:
   ```sh
   make
   ```
   This will also build MLX42 if needed.

## Running FdF

Run the program with a map file:
```sh
./fdf <path_to_map_file>
```
Example:
```sh
./fdf test_maps/42.fdf
```

## Controls
- Arrow keys: Move the map
- +/-: Zoom in/out
- q/w, a/s, z/x: Rotation the map
- Return: Change the projection
- Space: Reset setting

## License
This project is for educational purposes at 42 School.

---

*For more details, see the source code and comments.*