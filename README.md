Conway's Game of Life

Conway's Game of Life is a cellular automaton that simulates the evolution of a grid of cells over time. The rules of the game are simple:

    1.Any live cell with fewer than two live neighbors dies, as if by underpopulation.
    2.Any live cell with two or three live neighbors lives on to the next generation.
    3.Any live cell with more than three live neighbors dies, as if by overpopulation.
    4.Any dead cell with exactly three live neighbors becomes a live cell, as if by reproduction.

This program uses Python and numpy to simulate Conway's Game of Life, and matplotlib to visualize the grid of cells over time.
Instructions

    Clone or download the repository to your local machine.

    Make sure you have Python and the required libraries (numpy and matplotlib) installed.

    Open a terminal or command prompt and navigate to the directory containing the program files.

    Run the program by executing the following command:

python game_of_life.py

This will run the program with default settings, which will create a grid of 100x100 cells and run the simulation for 10 frames.

You can modify the program settings by using command line arguments. Here are the available options:

    --grid-size: Sets the size of the grid (default: 100).
    --mov-file: Saves the simulation as a movie file with the specified filename (example: --mov-file="my_movie.mp4").
    --interval: Sets the time interval between frames in milliseconds (default: 50).
    --glider: Adds a glider to the grid at the start of the simulation.
    --gosper: Adds a Gosper glider gun to the grid at the start of the simulation.

To use a command line argument, add it to the python game_of_life.py command with a space, like this:

css

    python game_of_life.py --grid-size=50 --mov-file="my_movie.mp4" --interval=100 --glider

    Once the program is running, a window will open with the initial grid of cells. The simulation will begin running automatically. You can pause and resume the simulation by clicking the pause button in the window toolbar. You can also close the window to stop the simulation.

    If you specified a movie file with the --mov-file option, the program will save the simulation as a movie file in the same directory as the program files.

Explanation

The program starts by defining two constants: ON and OFF, which represent the two possible states of each cell in the grid. The program also defines a list of values (vals) that can be used to randomly initialize the grid.

The randomGrid function generates a random grid of cells with size N using the numpy.random.choice method. The addGlider function adds a glider pattern to the grid at position (i, j).

The update function is the heart of the program. It takes four arguments: frameNum (the current frame number), img (the image object to be updated), grid (the current grid of cells), and N (the size of the grid). The function first creates a new grid newGrid by copying the current grid. It then iterates over each cell in the grid and applies the rules of Conway's Game of Life to determine whether the cell should be turned on or off in the new grid. Once the new grid
