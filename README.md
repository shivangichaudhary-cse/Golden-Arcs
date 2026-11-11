# Golden-Arcs# 🕵️‍♂️ Mystery at the Manor: Text-Based Detective Engine

A modular, Object-Oriented CLI mystery investigation game engineered with Python, dynamic lambda win-condition evaluation, and function-dispatch game loops.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Architecture-OOP%20%2B%20Functional-ff69b4?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Logic-Lambda%20Evaluators-blueviolet?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Engine-CLI%20Dispatch-brightgreen?style=for-the-badge" />
</p>

---

## 📌 Project Introduction

**Mystery at the Manor** is a lightweight, interactive text adventure where players act as a detective resolving a manor murder case. By searching rooms, collecting evidence into set structures, and interviewing suspects to update game state dictionaries, players must deduce the true culprit. 

Instead of relying on hardcoded `if-else` branching for victory states, the engine utilizes **higher-order functional programming** by embedding custom `lambda` logic directly within each `Suspect` object to evaluate evidence sets dynamically upon accusation.

---

## 🎯 Core Features

- **Dynamic Lambda Win-Conditions:** Each suspect encapsulates a functional rule evaluation taking active `clues` (Set) and `interviewed` (Dict) state frames to determine guilt seamlessly.
- **Set & Dictionary State Management:** Instant $O(1)$ clue tracking and suspect trait indexing eliminate duplicate evidence while keeping track of interviewed leads.
- **Function Dispatcher Loop:** Replaces traditional conditional menu loops with a dynamic function-mapping dictionary dispatch table.
- **Stateful Room Tracking:** Visual status updates mark explored locations to streamline player navigation.

---

## 🧠 System Architecture

The game decouples location searching, suspect evaluation, and main loop routing across three core classes:

<pre>
Mystery at the Manor Engine
 ┣ 📂 Domain Models
 ┃ ┣ Room (Location tracking, evidence retrieval, & search state)
 ┃ ┗ Suspect (Quote/trait holding & lambda condition evaluation)
 ┣ 📂 Game Engine
 ┃ ┗ DetectiveGame (Master engine initializing rooms, suspects, & state)
 ┗ 📂 Control Tier
   ┣ search_room() (Evidence set updates)
   ┣ interview_suspect() (State dict updates)
   ┣ make_accusation() (Triggers suspect.evaluate lambda)
   ┗ play() (Dictionary-driven execution loop)
</pre>

> [!NOTE]
> The engine uses pure Python native data structures, requiring zero external package installation to run.

---

## 💻 System Requirements

- **Environment & OS:** Cross-platform compatible with Windows 10/11, macOS, or Linux.
- **Runtime:** Python 3.8 or higher.
- **Execution:** Run directly via terminal using `python detective.py`.

---

## 🕹️ How to Play

1. **Search Rooms:** Explore locations like *The Study*, *The Library*, or *The Kitchen* to gather clues into your evidence set.
2. **Interview Suspects:** Question *The Butler*, *The Maid*, *The Gardener*, or *The Chef* to gather traits and record interviews.
3. **Make an Accusation:** Select a suspect. If your gathered evidence matches their unique lambda condition, they confess and you win the case!

---

## 🔮 Future Enhancements

- **Procedural Case Generation:** Randomize clues, murder weapons, and suspect lambda conditions per run.
- **Turn Counter / Limited Moves:** Introduce time constraints to raise difficulty and strategic choice.
- **Save / Load Game State:** Serialize game state dictionaries using JSON or Pickle.

---

## 💡 Conclusion

**Mystery at the Manor** demonstrates how combining Object-Oriented design with functional programming concepts like lambda expressions can create a clean, extensible text-engine architecture without complex dependencies.

---

<div align="center">
  <sub>Engineered by <b>shivangichaudhary-cse</b> • INTJ/ENTP Core Software Design</sub>
</div>
