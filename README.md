# Java Calculator 🧮

A simple calculator app for your computer, built in Java. It looks and works a bit like the Phone Calculator app.

This is a great project for anyone learning Java — it shows how to build a real, working desktop app with buttons and a screen you can click on.

## What This App Can Do

- Add, subtract, multiply, and divide numbers
- Flip a number between positive and negative (`+/-`)
- Turn a number into a percentage (`%`)
- Type decimal numbers (like `3.14`)
- Clear everything and start over (`AC`)

## Screenshot

<img width="346" height="533" alt="cphoto" src="https://github.com/user-attachments/assets/830284c6-20b6-47a2-8311-44568bd15345" />

## What You Need Before You Start

You need Java installed on your computer. To check if you already have it:

1. Open your terminal (Mac/Linux) or Command Prompt (Windows)
2. Type this and press Enter:
   ```bash
   java -version
   ```
3. If you see a version number, you're good to go! If not, download Java here: https://www.oracle.com/java/technologies/downloads/

You don't need anything fancy — no special libraries or tools. Everything used in this project comes built into Java already.

## How to Run This App

### Option 1: Using an IDE (easiest for beginners)

An IDE is just a program that makes writing and running code easier. Two popular free ones are:
- [IntelliJ IDEA (Community Edition)](https://www.jetbrains.com/idea/download/)
- [Eclipse](https://www.eclipse.org/downloads/)

Steps:
1. Open the IDE
2. Open this project folder
3. Find the file `Calculator.java`
4. Right-click it and choose "Run"

### Option 2: Using the terminal

1. Open your terminal and go to the folder with `Calculator.java`:
   ```bash
   cd path/to/this/folder
   ```
2. Turn the code into something Java can run:
   ```bash
   javac Calculator.java
   ```
3. Since this file doesn't have a `main` method yet, you'll need a tiny extra file to actually launch the app. Create a new file called `Main.java` in the same folder with this inside:
   ```java
   public class Main {
       public static void main(String[] args) {
           new Calculator();
       }
   }
   ```
4. Compile and run everything:
   ```bash
   javac Calculator.java Main.java
   java Main
   ```

## How the Code Works 

If you're learning Java, here's a walkthrough of what's happening inside `Calculator.java`:

- **The window**: `JFrame` is the actual window you see on your screen.
- **The screen**: `displayLabel` is the text at the top showing the numbers — it's just a label, like a sticky note that updates.
- **The buttons**: Each button (`0`-`9`, `+`, `-`, etc.) is created in a loop from a list called `buttonValues`, and colored based on what type of button it is (number, operator, or top function).
- **What happens when you click a button**: Every button has a listener attached to it (`addActionListener`) — this is code that "listens" for a click and decides what to do:
  - If you click a number, it gets added to the display.
  - If you click an operator like `+`, the app remembers your first number and waits for the second one.
  - If you click `=`, it does the math and shows the answer.
  - If you click `AC`, everything resets back to zero.

## A Few Things to Watch Out For (Learning Opportunities!)

If you keep working on this project, here are some things worth fixing as you learn more:

- **Comparing text with `==`**: The code compares strings like `buttonValue == "+"` using `==`. In Java, you're usually supposed to use `.equals()` instead (like `buttonValue.equals("+")`) — `==` happens to work here, but it's not the safe way to do it.
- **The `√` (square root) button doesn't do anything yet** — a fun next step would be to add that feature yourself!
- **Dividing by zero isn't handled** — try dividing a number by 0 and see what happens, then think about how you'd fix it.
- **You can't chain calculations** — like typing `2 + 3 + 4` in a row.
- **No keyboard support** — right now you can only click the buttons with your mouse.

