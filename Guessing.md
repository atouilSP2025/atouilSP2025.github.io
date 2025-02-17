
```mermaid
---
config:
  look: handDrawn
  theme: forest
---
flowchart TD
    %% This is the start of the game.
    A[Press Start] -->|Computer generates a random number 0 to 99| B(Please guess a number 0 to 99!)
    %% The computer will generate a number to be guessed and prompt for a number to be guessed.
    B --> C{User Guess is input}
    %% The User will guess a number and input it to see if it is correct.
    C -->|Number is correct| D[Correct! Play again?]
    %% The input number is correct and the User can choose to play again.
    C -->|Number is incorrect| E{Computer checks if number is higher or lower than generated number}
    %% The computer notifies that the User Guess is incorrect and prompts User to try again with another guess. 
    E -->|Number is too high| F[Number is too high. Guess again.]
    %% The number guessed was too high and the User needs to guess a lower number.
    E -->|Number is too low| G[Number is too low. Guess again.]
    %% The number guessed was too low and the User needs to guess a higher number.
    E -->|Guess is a letter, character, or number not in range.| H[Incorrect input! Try again!]
    %% Input is not within parameters of game. User needs to try again within parameters.
    F --> B 
    %% User is sent back to guess screen to input new number.
    G --> B 
    %% User is sent back to guess screen to input new number.
    H --> B 
    %% User is sent back to guess screen to input new number.
    D --> A
    %% The User will need to guess a new number.
```    
