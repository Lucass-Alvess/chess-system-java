# Chess System Java 
## Introduction
Project carried out and developed in the [Complete Java](https://www.udemy.com/course/java-curso-completo/) Course on the Udemy platform, taught by Prof. Dr. Nelio Alves.

This project consolidates the knowledge acquired so far in the course.

* Classes: default constructors, attributes, encapsulation, getters and setters, instance and class (static) methods, overloads, concrete and abstract classes.
* Project-oriented programming, logic, and organization: inheritance, polymorphism, method overriding, dependency injection, associations, encapsulation, enumeration, downcasting, upcasting, layering pattern, exception handling, lists, arrays, sequential structures, loops (for and while), and conditionals (if-else and ternaries), UML diagrams, version control, and clean code.

## Project design 

The project is divided into two layers: **Board layer and Chess layer**. The board is represented by a matrix, where each element may or may not contain a piece. However, the way we access this matrix differs between the layers. In the Board layer, we handle all the board control logic. The matrix indices are integer numbers corresponding to the indices of lists. The Position class represents a position in the matrix, while the abstract Piece class defines a piece in the matrix through Position and abstract methods for possible movements. The Board class physically describes the board and its state, and the BoardException class is used to handle board-related exceptions.

The Chess layer groups all the pieces on the board (King, Bishop, Knight, Pawn, Queen, Rook), which are entities (classes) derived from the abstract ChessPiece class, which in turn extends from the Piece class in the other layer. Each piece inherits attributes and methods from its superclasses and implements its own movement rules and special moves (if any). The game control logic (such as checkmate) is managed by the ChessMatch class, which also handles exceptions through the ChessException class, the Color enum, and the ChessPosition class. In this layer, matrix indices are accessed using a user-friendly notation, i.e., letters from a to h for columns and numbers from 1 to 8 for rows. Therefore, there is a need to convert between board coordinates and this notation.

Below is the UML diagram of the project course material credits:
![](https://github.com/Lucass-Alvess/chess-system-java/blob/main/assets/images/chess-system-design.png)

## Installation
1. Download and extract the project.
2. Recommended to use a terminal that supports color coding.
3. Navigate to the /bin directory of the project (command: cd bin).
4. Once in the directory, type java application/Program to run the application (Java needs to be version 17 or higher).
5. Have a great game!
