# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  - pressing ewnter after inputing a guess doesn't decrement the attemps left count
  - answer seems to be outside the range of 1 to 100 telling me that it is higher than 100
  - even with one attempt left it tells me the answer and the answer is 15 which contradicts when it told me to guess higher
  - when I try to start a new game it resets the count but it doesn't let me enter a new value or give me hints it jsut tells me to start a new game (stays stuck in the last game)

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
|   90  |      go higher    |     go lower    |         none           |
|   92  |      go lower     |     go higher   |         none           |
| - 100 |      go higher    |     go lower    |         none           |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  -Copilot was used for this project 

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  -The fix for starting a new game was correct and the way the AI did that was by setting st.session_state.attempts to 0
  
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
  - it tried to make me launch the game in the wrong directory and I switched it to the correcty directory and it started to work correctly 
---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
  - for the logic issues I simply determined whether the outputs of the code made sense when compared to the inputs, if go LOWER only appeared when the guess was higher than the answer.
  - for issues like new game not starting I simply tested to see if a new game would start if I pressed the button 

- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
    - I purposely put in a guess higher than the answer and waited for the output but instead of outputting go LOWER it outputted go HIGHER, this showeed me that either the logic was off or the string was off.

- Did AI help you design or understand any tests? How?
  - the AI helped me design the tests by updating the functionms in the test_game_logic.py file 
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
    The way streamlit rerunbs work is that they automatically re-execute the entire python script from top to bottom to update the app's fronmt-end. The way session state is used is to store data during the length of one session.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
    -I would like to keep documentation in a seperate file of the same folder as the project I am working on

- What is one thing you would do differently next time you work with AI on a coding task?
    -I would ask the AI to explain things in more depth to get a better understanding of what the AI is changing

- In one or two sentences, describe how this project changed the way you think about AI generated code.
    -I used to think of AI generated code as a one step process to make the project I want to make but now I look at AI generated code as the "base" of my project adn a way to get the grunt work out of the way. 

---