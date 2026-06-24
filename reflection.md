# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

The first time I ran the game, it loaded successfully but the hints did not seem correct. When I entered very low numbers, the game told me to go lower, and when I entered very high numbers, the game told me to go higher. This made the game confusing because the hints seemed backwards. I also had to spend time setting up Python and Streamlit before I could begin testing the game.

**Bug Reproduction Log**

| Input | Expected Behavior                                                 | Actual Behavior           | Console Output / Error |
| ----- | ----------------------------------------------------------------- | ------------------------- | ---------------------- |
| 1     | The game should suggest a higher number                           | The game said "Lower"     | None                   |
| 99    | The game should suggest a lower number                            | The game said "Higher"    | None                   |
| 50    | The game should provide a helpful hint based on the secret number | The game said "Go Higher" | None                   |


---

## 2. How did you use AI as a teammate?

I used ChatGPT as my main AI tool for this project. It helped me install Python, set up Streamlit, understand the assignment instructions, and troubleshoot errors that came up while running the project. AI was useful because it guided me through the setup process step by step.

One correct suggestion the AI gave was to install Python and add it to my PATH. Before doing that, commands like `python` and `pip` were not working correctly. I verified the suggestion worked when `python --version` returned a version number and I was able to launch the Streamlit application.

One misleading suggestion was assuming certain game behaviors were definitely bugs before I had finished testing the game. I learned that I needed to verify everything myself by running the application and recording the results. This showed me that AI suggestions should always be tested before accepting them as correct.

---

## 3. Debugging and testing your fixes

I decided a bug was fixed by running the game again and checking if the behavior matched what I expected. Instead of assuming the code worked, I tested multiple inputs and compared the results before and after making changes. This helped me confirm whether the fixes actually solved the problem.

One manual test I ran was entering different numbers such as 1, 50, and 99 to see if the hints made sense. The results showed that the hint logic appeared to be inconsistent, which helped me identify where the problem might be located. Testing different inputs made it easier to reproduce the bug consistently.

AI helped me understand what kinds of tests I should perform and what outcomes I should expect. It also explained how automated tests could be used to verify game logic. Even with AI assistance, I still had to run the tests myself and confirm the results directly in the game.

---



## 4. What did you learn about Streamlit and state?

I learned that Streamlit reruns the entire script whenever a user interacts with the application. Because of this, data can be lost unless it is stored in session state. Session state acts like memory for the application and allows values to persist between reruns. I would explain it to a friend by saying that Streamlit refreshes the page every time something happens, and session state helps the app remember important information such as scores, guesses, and game progress.


---

## 5. Looking ahead: your developer habits

One habit I want to reuse in future projects is testing my code frequently instead of waiting until the end. Running the program after small changes makes it easier to find bugs and understand what caused them. This project showed me that debugging is easier when changes are made one step at a time.

Next time I work with AI on a coding task, I will spend more time verifying its suggestions before accepting them. AI can be very helpful, but it does not always provide the correct answer immediately. This project changed the way I think about AI-generated code because I learned that AI should be treated as a tool and teammate, not as a replacement for testing and critical thinking.
