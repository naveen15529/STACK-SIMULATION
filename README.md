Overview

This C program demonstrates the implementation of a stack using arrays and provides a menu-driven interface for performing stack operations. Additionally, it includes an application that evaluates postfix (Reverse Polish Notation) expressions using the stack.

Features
Stack Operations

Push – Insert an integer into the stack

Pop – Remove the top element

Peek – View the current top element

Display – Show all elements from top to bottom

Postfix Evaluation

Evaluates postfix expressions with:

Single-digit operands (0–9)

Operators: +, -, *, /

Expressions may contain optional spaces

Detects errors such as:

Division by zero

Invalid expressions

Stack underflow/overflow

How It Works

The program uses a structure-based stack containing:

arr[MAX] → array to store elements

top → index of the current top element

The postfix evaluator scans each character:

If it’s a digit → push it

If it’s an operator → pop two values, apply the operator, push result

Final remaining value → result of the expression

Example Postfix Expression
23*54*+9-


Meaning:
2×3 + 5×4 − 9 = 6 + 20 − 9 = 17

How to Run

Compile the file:

gcc program.c -o stack


Run:

./stack


Use the interactive menu to perform operations or evaluate postfix expressions.

Menu Options
1. Push
2. Pop
3. Peek
4. Display Stack
5. Evaluate Postfix Expression
6. Exit

Notes

Supports only single-digit operands for postfix evaluation.

Stack size is limited to MAX = 100.

Uses isdigit() for safe operand detection.
