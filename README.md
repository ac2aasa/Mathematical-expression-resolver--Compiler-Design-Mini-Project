# Mathematical Expression Resolver

This is a compiler design project for resolving mathematical expressions. The project is designed to take input in the form of an arithmetic expression, parse it, and evaluate it. The project uses the Lex and Yacc tools for lexical analysis and parsing.

## Tools Used
1. Lex - a lexical analyzer generator that receives a set of user-defined patterns and scans the source code to return tokens.
2. Yacc - a parser generator that receives user grammar and generates C source code for the parser.

## File Structure
- `expr.l` - Lexical analyzer file
- `expr.y` - Syntax analyzer file
- `Makefile` - Makefile for compilation
- `README.md` - Readme file
- `app.exe` - Compiled executable file

## How to Run
To run the program, follow the steps below:
1. Compile the lexical analyzer file by running the command `lex expr.l`
2. Compile the syntax analyzer file by running the command `yacc -d expr.y`
3. Compile the executable file by running the command `gcc lex.yy.c y.tab.c`
4. Run the program by running the command `./app.exe`
5. Terminate the program with `CTRL+D`

Alternatively, you can simply run the command `make` to compile and run the program.

## Sample Test Cases
1. Input: `5-2*6+7`
   - Result: Success
   - Output: `0`

2. Input: `5-6/0+7`
   - Result: Error (divide by zero)
   - Output: `ERROR: Invalid Arithmetic Expression`

3. Input: `a-7+5`
   - Result: Error (unrecognized token)
   - Output: `ERROR: Invalid Arithmetic Expression`

4. Input: `2-5*7/3+4-9/2`
   - Result: Success
   - Output: `-8`

## Conclusion
This project demonstrates the use of Lex and Yacc tools in designing a mathematical expression resolver. The program can parse and evaluate simple arithmetic expressions and handle errors gracefully.
