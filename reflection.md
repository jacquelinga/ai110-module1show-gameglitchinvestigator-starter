# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?
Bug 1: The hint markers were broken, the question asked guess a number 1-100 at some point I guessed one and it made me go lower.

Bug 2: The score doesn't reset properly. After starting a new game the score was still -20 instead of starting fresh.

Bug 3: New game button does not reset the game. 

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| make multiple guesses|attempts should track guesses |attempts remained 0 |none |
|click new game| game history should reset|old guesses still there |none |
| guess 97 when secret is 50 | go lower| go higher | none|

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project AI Coding assistant in VS Code. I used AI to help me undersatnd the bugs, and test the fixes.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result). AI Suggested the higher and lower hint logic was backwards. I verified this by running tests with guesses and the tests passed. 

- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.
I did not accept a refactoring attempt the AI suggested. I had AI correct the scope and only move parse_guess and check_guess while leaving unrelated helpers alone. I verfied the final version by running the tests and checking that files compiled.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I decided a bug was fixed by testing the game.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  I ran a pytest test using a guess of 60 with a secret of 50 and guess of 40 with the same secret.
- Did AI help you design or understand any tests? How?
Yes, AI helped me create the pytest cases and helped me understand what both results should be.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Streamlit runs script from top to bottom, session state saves information between reruns, like saving your spot in a game. 

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git. Testing after each change was very helpful.
- What is one thing you would do differently next time you work with AI on a coding task? I would rewrite my prompts more carefully. 
- In one or two sentences, describe how this project changed the way you think about AI generated code. I believed AI generated code was full of bugs but AI was very helpful to me this time around. 
