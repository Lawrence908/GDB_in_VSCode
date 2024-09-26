# GDB - VS Code
## How to set up gdb debugger in VS Code for c / C++ assignment debugging

---

1. Install C/C++ Extension in VS Code.

2. Ensure that the path to gdb is correct and that gdb is installed on your system. ( good to go on CSCI servers)

	    which gdb

- Ensure the output matches /usr/bin/gdb. If not, update the miDebuggerPath in launch.json.
- If there's no output from the which gdb command, this indicates that gdb is not installed on your system. You can install gdb using the following command:

	    sudo apt-get install gdb

3. Copy all 4 '.json' config files into a folder called /.vscode inside your assignment folder.

4. Ensure line 11 of launch.json points to the correct program name for the binary file..              
        
        "program": "${workspaceFolder}/bin/sudoku_checker",
- Replace 'sudoku_checker' with whatever program name is being used for the current assignment.
- I am working on a more generic option that will simply read the first file in the bin folder and append it to the program path, but no success yet.

5. Set a breakpoint at the desired location in your code, or start on the int main() line to test

6. Run the debug using F5 key or from the Run and Debug section with Ctl + Shift + D.