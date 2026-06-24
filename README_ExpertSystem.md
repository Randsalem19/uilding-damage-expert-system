# 🏚️ Building Damage Assessment Expert System using Fuzzy Logic

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--fuzzy-0.4.2-orange?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Course-Expert_Systems-1F4E79?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/UCAS-Gaza-green?style=for-the-badge"/>
</p>

<p align="center">
  <b>Expert Systems Course Project</b><br/>
  University College of Applied Sciences (UCAS), Gaza, Palestine<br/>
  Student: Rand Majed Salem — ID: 220210128
</p>

---

## 🧠 Overview

A **Fuzzy Logic Expert System** prototype that evaluates building damage and recommends **reconstruction priority levels** despite real-world uncertainty — a particularly relevant application for post-conflict and disaster-affected regions.

The system takes two inputs — **damage severity** and **population density** — and outputs a **reconstruction priority score** (0–10), enabling decision-makers to allocate resources efficiently.

---

## 🎯 Problem Statement

In disaster or conflict scenarios, reconstruction teams face two key challenges:
- **Uncertainty**: damage assessments are rarely perfectly precise
- **Multiple factors**: a heavily damaged building in a low-density area may be less urgent than a moderately damaged one in a densely populated zone

Classical rule-based expert systems struggle with this. **Fuzzy Logic** handles it naturally by modeling degrees of membership rather than hard yes/no rules.

---

## ⚙️ System Design

### Input Variables
| Variable | Range | Linguistic Values |
|---|---|---|
| `damage_severity` | 0 – 10 | Low, Medium, High |
| `population_density` | 0 – 10 | Low, Medium, High |

### Output Variable
| Variable | Range | Linguistic Values |
|---|---|---|
| `reconstruction_priority` | 0 – 10 | Low, Medium, High |

### Membership Functions
All variables use **triangular membership functions (trimf)**:
```
Low:    [0, 0, 5]
Medium: [0, 5, 10]
High:   [5, 10, 10]
```

### Fuzzy Rules
```
Rule 1: IF damage_severity is HIGH   AND population_density is HIGH   → priority is HIGH
Rule 2: IF damage_severity is MEDIUM AND population_density is MEDIUM → priority is MEDIUM
Rule 3: IF damage_severity is LOW    AND population_density is LOW    → priority is LOW
```

---

## 📊 Test Results

| Test Case | Damage Severity | Population Density | Reconstruction Priority | Decision |
|---|---|---|---|---|
| Case 1 (High)   | 9 / 10 | 8 / 10 | **6.48 / 10** | 🔴 High Priority |
| Case 2 (Medium) | 5 / 10 | 5 / 10 | **5.00 / 10** | 🟡 Medium Priority |
| Case 3 (Low)    | 2 / 10 | 3 / 10 | **4.52 / 10** | 🟢 Low Priority |

---

## 📁 Repository Structure

```
├── Rand_M__M__Salem.ipynb    # Full implementation notebook
└── README.md                 # This file
```

---

## 🚀 How to Run

```bash
# 1. Install dependency
pip install scikit-fuzzy matplotlib seaborn numpy

# 2. Open the notebook
jupyter notebook Rand_M__M__Salem.ipynb
```

---

## 🛠️ Tech Stack

`Python` · `scikit-fuzzy` · `NumPy` · `Matplotlib` · `Seaborn`

---

## 👤 Author

**Rand Majed Salem** | [GitHub](https://github.com/Randsalem19) · [LinkedIn](https://linkedin.com/in/rand-majed-salem)

<p align="center">Made at UCAS, Gaza, Palestine 🇵🇸</p>
