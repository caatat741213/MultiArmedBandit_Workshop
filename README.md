# 🎰 Casino Challenge — Multi-Armed Bandits & ε-Greedy (Gamified Workshop)

## 📘 Overview
This workshop introduces **exploration–exploitation trade-offs** in **Reinforcement Learning** through a gamified **Multi-Armed Bandit (MAB)** challenge.  
Students will implement ε-greedy policies, compete for the highest rewards, and analyze their strategies in both stationary and non-stationary environments.

---

## 🧠 Learning Objectives
By completing this workshop, students will be able to:
- Explain the **exploration vs. exploitation dilemma**.
- Implement **ε-greedy** and **decaying ε-greedy** algorithms.
- Compare the effects of different ε values on performance.
- Adapt policies for **non-stationary bandits** using constant step-size (α).
- Reflect critically on their strategies and outcomes.

---

## 🏗️ Workshop Structure

| Phase | Activity | Description |
|-------|-----------|-------------|
| 1 | **Setup & Introduction** | Review MAB concepts and workshop goals. |
| 2 | **Round 1 – Stationary Casino** | Students compete using ε-greedy strategies. |
| 3 | **Leaderboard & Reflection** | Submit scores, compare results, and discuss strategies. |
| 4 | **Round 2 – Non-Stationary Casino** | Adapt to drifting reward probabilities using constant α. |
| 5 | **Final Discussion** | Relate bandit learning to real-world systems (A/B testing, ads, recommendations). |

---

## 🎮 Gamified Components
- **Leaderboards:** Students submit results to CSV files (`submissions_round1.csv`, `submissions_round2.csv`) and view rankings.
- **Badges / Awards:**
  - 🥇 *Efficient Exploiter* — Highest reward with low ε.
  - 🧭 *Risk Taker* — High ε with competitive performance.
  - 🔄 *Adaptive Strategist* — Best performance in non-stationary round.
- **Reflection Prompts:** Encourage analysis of exploration behavior and real-world parallels.

---

## 🏆 My Workshop Summary & Key Findings

### 1. Round 1 (Static Environment)
* **What I found:** When the casino does not change, **less exploration is better**. My fixed $\epsilon = 0.01$ got the highest score of **1826 points**.
* **The Reason:** After the agent finds the best machine, it should stop trying other machines and focus on exploiting it to make money.

### 2. Round 2 (Changing Environment)
* **What I found:** When the casino changes over time, **we must keep exploring**. My `eps=0.1` got **2594 points**, which is better than `eps=0.01` (**2584 points**).
* **The Reason:** If the agent stops exploring, it will get "stuck" on an old machine when that machine becomes bad. 
* **The Alpha ($\alpha$) Rule:** A medium $\alpha$ (0.1) is the best. It helps the agent forget old data and learn new changes quickly.

### 3. Conclusion
* **In a stable world**, we should exploit more and explore less.
* **In a changing world**, we must always explore a little bit and update our memory fast.

---

## 💻 Technical Notes
- Works in **Jupyter Notebook** or **Google Colab**.
- Dependencies: `numpy`, `matplotlib`, `pandas`, `IPython.display`
- Each student runs locally; the instructor collects leaderboard CSVs for aggregation.

---

## 🧩 Files Included
| File | Description |
|------|--------------|
| `Casino_Challenge_MAB_Workshop_LCC.ipynb` | Main notebook with competition, code, and reflection prompts. |
| `README.md` | This summary document. |

---

## 🧭 Instructor Tips
- Keep the same random seed (`SEED_ENV`) for fairness.
- Hide true means during competition.
- Encourage students to explain *why* their chosen ε performed as it did.
- Optionally extend to **UCB** or **Thompson Sampling**.

---

## 🧾 License
For educational use in academic settings.  
Developed with support from OpenAI’s ChatGPT (GPT‑5) as part of CSCN8020 Machine Learning Education Tools.
