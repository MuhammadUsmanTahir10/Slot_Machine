# Slot_Machine
A simple slot machine game developed on Python using Pycharm. (Just for Fun)

I have built a simple slot machine game that takes amount as input and ask user to select the number of lines to bet and also the amount for betting, then based on random character generation it produces the slot machine results.

Let's dive into the logic of the slot machine game in detail:

1. **Importing the `random` Module:**
   import random

   - This line imports the `random` module, which is used for generating random numbers and shuffling symbols on the slot machine reels.

3. **Game Configuration Constants:**
   MAX_LINES = 3
   MAX_BET = 100
   MIN_BET = 1
   
   - `MAX_LINES`, `MAX_BET`, and `MIN_BET` are constants that define the game's parameters.
   - `MAX_LINES` sets the maximum number of lines a player can bet on (in this case, 3).
   - `MAX_BET` and `MIN_BET` define the allowable betting range with a maximum of $100 and a minimum of $1.

5. **Symbol Definitions:**
   symbol_count = {
       "A": 2,
       "B": 4,
       "C": 6,
       "D": 8
   }

   symbol_value = {
       "A": 5,
       "B": 4,
       "C": 3,
       "D": 2
   }
   
   - These dictionaries define the symbols on the slot machine and their properties.
   - `symbol_count` specifies how many times each symbol ("A," "B," "C," "D") appears on the reels.
   - `symbol_value` assigns a payout value to each symbol, determining how much the player wins when matching symbols appear on a payline.

7. **`check_winnings()` Function:**
   def check_winnings(columns, lines, bet, values):
       # Function code here
   
   - This function calculates the winnings for a given spin.
   - It takes as input the current state of the slot machine (`columns`), the number of lines bet on (`lines`), the bet amount (`bet`), and the symbol values (`values`).
   - The function checks each line for matching symbols, and if all symbols on a line match, it calculates the winnings based on the bet amount and symbol values.
   - The function returns the total winnings and a list of winning lines.

9. **`get_slot_machine_spin()` Function:**
   def get_slot_machine_spin(rows, cols, symbols):

   - This function generates a random spin of the slot machine's reels.
   - It takes the number of rows (`rows`), columns (`cols`), and symbol configuration (`symbols`) as input.
   - The function creates an empty list of `columns` and fills it with randomly selected symbols based on the symbol configuration.
   - The result is a 2D list representing the current state of the slot machine.

10. **`print_slot_machine()` Function:**
   def print_slot_machine(columns):
    
   - This function prints the current state of the slot machine.
   - It takes the 2D list of `columns` as input and displays the symbols in a grid format on the console.

11. **User Deposit Function (`deposit()`):**
   def deposit():
  
   - This function allows the player to deposit an initial balance.
   - It prompts the player to enter an amount and validates that it's a positive integer before returning the initial balance.

11. **Get Number of Lines Function (`get_number_of_lines()`):**
   def get_number_of_lines():
     
   - This function prompts the player to choose the number of lines they want to bet on.
   - It ensures that the input is a valid number within the allowed range (1 to `MAX_LINES`).

11. **Get Bet Amount Function (`get_bet()`):**
   def get_bet():
    
   - This function prompts the player to specify the bet amount.
   - It validates that the bet amount is within the allowed range (between `MIN_BET` and `MAX_BET`).

11. **Spin Function (`spin()`):**
    def spin(balance):
     
    - This function manages a single spin of the slot machine.
    - It takes the current balance as input and guides the player through the betting process.
    - It checks if the player has enough balance to place the bet, generates the spin result, calculates winnings, and updates the player's balance accordingly.
    - The function returns the net change in the player's balance (winnings - total bet).

12. **Main Game Loop (`main()`):**
    def main():
       
    - The `main()` function is the central game loop.
    - It starts by obtaining the player's initial balance using the `deposit()` function.
    - It then repeatedly allows the player to play spins or quit the game.
    - After each spin, the balance is updated, and the player can continue playing or exit the game.

13. **Running the Game:**
    main()

    - Finally, the game is initiated by calling the `main()` function, which sets everything in motion. The player interacts with the game, depositing money, spinning the reels, and checking their final balance.

This comprehensive explanation provides a detailed breakdown of the code's logic, from defining game parameters to managing player interactions and calculating winnings on the slot machine.
