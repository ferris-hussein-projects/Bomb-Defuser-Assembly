# Bomb-Defuser

## Overview
This project features **Dr. Evil's Insidious Bomb, Version 1.1**, a challenge designed to test reverse engineering, debugging, and problem-solving skills. The bomb consists of **nine phases**, each requiring a specific input to defuse successfully. Incorrect inputs will trigger an "explosion."

## Files
- **`bomb.c`** - The source code of the bomb program.
- **`solution.txt`** - The correct inputs needed to defuse the bomb, obtained through reverse engineering.

## How the Bomb Was Defused
Defusing this bomb required **analyzing its disassembled assembly code**, examining **registers, memory operations, and conditional jumps** to determine the expected inputs at each phase. The correct solutions were extracted by:
- Running the program inside a **debugger** (e.g., `gdb`).
- Inspecting **register values** and **stack contents** at key points.
- Identifying comparison instructions (`cmp`, `test`, `jne`, `je`) to infer the required input values.
- Tracing function calls and loops to understand pattern-based inputs.

## How to Run
1. **Compile the bomb**:
   ```sh
   gcc -o bomb bomb.c
   ```
2. **Run the bomb**:
   ```sh
   ./bomb
   ```
   - Alternatively, provide the solved input:
     ```sh
     ./bomb solution.txt
     ```

## Objective
The challenge was to **reverse-engineer the bomb’s logic** and **extract the correct sequence of inputs** required to defuse it, without access to the original source code. The solutions in `solution.txt` were determined through careful assembly analysis and checkpointing.
