# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
    The game looked like you're regular number guessing game in which it would tell you to guess higher or lower depending on your initial guess.
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
    The New Game button doesn't seem to work. The history only resets after I refresh the page.
    Sometimes the hints are just incorrect. I put in 50 and the hint said to go lower even though the target number was 74.

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| 50    | Hint says higher  | Hint said lower | None
| -1    | Hint tells user   | Hint said lower | None
|       | their guess is    | 
|       | out of range      | 
| Press | Game history      | History didn't  | None
| New   | resets            | reset and I     |
| Game  |                   | don't get more  |
|       |                   | attempts        |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  Copilot
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  The AI suggested to add:
       st.session_state.status = "playing"
       st.session_state.history = []
       st.session_state.score = 0
  into new_game to fix the button and it was correct. I verified the result by running a game and pressing the New Game button.
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.
  When I described the two bugs I decided to fix---fixing the new game button and fixing the hint system---it accurately fixed the bugs without touching anything else or over-engineering the result. I didn't need to reject any solutions since they fixed the problems I had at the time.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
  I decided a bug was really fixed by testing different testcases on the browser. 
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
  I ran a manual test with the new game button, pressing it after 8 failed attempts, after a successful guess, halfway through a current round and all of them worked.
- Did AI help you design or understand any tests? How?
  AI did not help me create testcases because it was easier to test them myself manually.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
  Streamlit is like something that re-runs my program everytime a user interacts with the app, updating the result. Session state is more like memory that saves the data inbetween the streamlit restarts.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
    One takeaway from this project is how to properly use the built in VSCode copilot chat. I usually stick with claude or gemini in browser, but I now know how convient it is to just use VSCode's built in chat to edit my programs rather than copying and pasting into an external application.
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
  Next time I might ask more indepth questions or ask the AI to make comments for me to save time.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  This project made me realize how much easier it is to code these days with the assistance of AI. I'm not very knowledgeable about how to use python or python syntax in general, but with the help of AI I was able to quickly complete this assistance without having to watch various youtube videos on how to code python from scratch.
