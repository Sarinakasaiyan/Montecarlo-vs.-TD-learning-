((
------
 🧠 Monte Carlo vs. TD(0) Value Estimation in Gridworld

This project compares two classical reinforcement learning algorithms — Monte Carlo and TD(0) — for estimating the state-value function of a simple 4x4 Gridworld environment.

---

<img width="1431" alt="Screenshot 1404-02-05 at 10 17 58" src="https://github.com/user-attachments/assets/9f52c5ee-39a6-4845-bfd0-0b6afd5e7165" />

---


 📌 Overview

- Environment: 4x4 grid with two terminal states at `(0,0)` and `(3,3)`.
- Reward: -1 per step (except in terminal states).
- Policy: Random (uniform over actions).
- Goal: Compare how Monte Carlo and TD(0) estimate the value of each state over multiple episodes.

---

 ⚙️ Algorithms

 ✅ Monte Carlo (MC)
- Updates only at the end of each episode.
- Uses actual returns from the full episode (no bootstrapping).
- High variance, low bias.

 ✅ TD(0) (Temporal Difference)
- Updates after every single step.
- Uses bootstrapping: updates based on the estimate of the next state.
- Lower variance, higher bias.

---

 📊 Visual Output

After running the code, you’ll see:

1. Heatmap: Monte Carlo Values  
2. Heatmap: TD(0) Values  
3. Heatmap: Absolute Difference (|MC - TD|)  
4. Table: Side-by-side numerical comparison

---

 🧮 Sample Table Output

| State | Monte Carlo | TD(0) | Abs Diff |
|-------|-------------|-------|----------|
| (1,1) |     -3.89   | -4.21 |   0.32   |
| (2,2) |     -2.55   | -2.72 |   0.17   |


> 📌 Note: Results vary slightly due to random policy and initializations.

---


🔍 Ideas for Improvement

- Use OpenAI Gym environments.
- Add Q-value estimation and policy improvement.
- Visualize learning over time (per episode).
- Convert into Streamlit dashboard.


---
