# c-craps-game

Modify the craps program in Fig 5.14 to allow wagering.

(Pages 179-180 or Ch5 slides 115-118)

Start the user off with $1000.

Prompt the user to input a wager.

Make sure they have enough in their balance to cover their wager, re-prompt if not.

Run a game of Craps.

If the user wins, add the wager to their balance.

If the user loses, subtract the wager from their balance.

Show the user their new balance and ask for their next wager (use a sentinel value to quit).

If they hit zero, display a message "Sorry. You busted." (or something like that)

As they win or lose, use a separate function to randomly print different messages to egg on the user or encourage them to continue. You should use an array to store the possible messages.

If you would like to add a little suspense, this code in the rollDice(void) method will cause it to pause for a second before telling you what the dice roll is. Near the top of the source code, include this code to support both Windows and Mac/Linux

    #ifdef _WIN32
        #include <Windows.h>
    #else
        #include <unistd.h>
    #endif

And where you put the sleep function (most likely in rollDice()), put this code to also support cross platform.

    #ifdef _WIN32
        Sleep(1000);
    #else
        sleep(1);
    #endif