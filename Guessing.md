flowchart TD
    Start([Start]) --> GenerateRandom[Generate Random Number]
    GenerateRandom --> GetUserInput[Get User Input]
    GetUserInput --> ValidateInput[Validate Input]
    ValidateInput -->|Valid| CheckGuess[Check Guess]
    ValidateInput -->|Invalid| GetUserInput
    CheckGuess -->|Too High| InformTooHigh[Inform User: Guess is Too High]
    CheckGuess -->|Too Low| InformTooLow[Inform User: Guess is Too Low]
    CheckGuess -->|Correct| CongratulateUser[Congratulate User]
    InformTooHigh --> GetUserInput
    InformTooLow --> GetUserInput
    CongratulateUser --> End([End])


## Description of Steps

1. Start: The game begins.
2. Generate Random Number: A random number is generated within a specified range (e.g., 1 to 100).
3. Get User Input: The game prompts the user to enter a guess.
4. Validate Input: The game checks if the input is a valid number and within the acceptable range.
   - Valid: If the input is valid, proceed to check the guess.
   - Invalid: If the input is invalid, prompt the user to enter a valid guess.
5. Check Guess: The program compares the user’s guess to the generated random number.
   - Too High: If the guess is higher than the random number, inform the user.
   - Too Low: If the guess is lower than the random number, inform the user.
   - Correct: If the guess matches the random number, congratulate the user.
6. Inform User: Based on the feedback, the game prompts the user for another guess if the guess was too high or too low.
7. Congratulate User: If the guess is correct, the user is congratulated.
8. End: The game ends.
