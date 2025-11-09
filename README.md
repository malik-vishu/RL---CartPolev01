# 🧠 Deep Q-Network (DQN) – CartPole Reinforcement Learning

This repository contains multiple **DQN training experiments** on the classic **CartPole-v1** environment using **Stable-Baselines3**.  
Each experiment explores different **hyperparameters** (learning rate, buffer size, learning start steps, etc.), with TensorBoard logs, trained models, evaluation results, and gameplay videos.

Models and Videos are not uploaded.
---

## 🚀 Project Structure

```
📂 RL-CartPole/
│
├── 📁 models/
│   ├── lr_1e-3_50k/
│   │   ├── seed_0/dqn_cartpole_seed_0.zip
│   │   ├── seed_7/dqn_cartpole_seed_7.zip
│   │   └── ...
│   ├── ls_10k/
│   └── ls_default/
│
├── 📁 videos/
│   ├── seed_val_0/dqn_cartpole_seed_0.mp4
│   ├── seed_val_7/dqn_cartpole_seed_7.mp4
│   └── ...
│
├── 📁 logs/
│   ├── DQN_1/
│   ├── DQN_2/
│   ├── lr_1e-3_50k/
│   ├── ls_10k/
│   └── ls_default/
│
├── 📄 results_ls_default.txt
├── 📄 results_ls_10k.txt
├── 📄 results_lr_1e-3_50k.txt
├── 📄 requirements.txt
└── 📄 code.py
```

---

## ⚙️ Installation

```bash
python -m venv venv
venv\Scripts\activate   # On Windows
# or
source venv/bin/activate  # On Mac/Linux

pip install -r requirements.txt
```

---

## 🧠 Training

To train the DQN agent with multiple random seeds:

```bash
python code.py
```

Each seed will:
- Save model weights under `models/`
- Record a gameplay video under `videos/`
- Log metrics to `results_*.txt`

---

## 📊 TensorBoard Visualization

```bash
tensorboard --logdir=logs/
```

Then open your browser and go to:
👉 [http://localhost:6006](http://localhost:6006)

---

## 🎥 Watch Trained Agent

```bash
python -m http.server
```
Then open:
```
http://localhost:8000/videos/seed_val_42/dqn_cartpole_seed_42.mp4
```

---

## 🧪 Experiments

| Experiment | Description | Folder |
|-------------|--------------|--------|
| **DQN_1–DQN_5** | Learning starts after 2k steps | `logs/DQN_1`, `logs/DQN_2`, ... |
| **lr_1e-3_50k** | Learning rate = 1e-3, 50k steps | `models/lr_1e-3_50k/` |
| **ls_10k** | Learning starts after 10k steps | `models/ls_10k/` |
| **ls_default** | Default parameters | `models/ls_default/` |

---

## 🧰 Tech Stack

- Python 3.11
- Stable-Baselines3 (DQN)
- Gymnasium (CartPole-v1)
- TensorBoard for visualization
- ImageIO for video generation
- Matplotlib for optional plots

---

## 📄 Results Logging

Example `results_ls_default.txt`:

```
Seed	MeanReward	StdReward
0	    498.10	    3.95
7	    497.45	    4.12
21	    500.00	    0.00
42	    490.25	    5.30
84	    495.90	    4.60
```

---

## 👨‍💻 Author

**Vishwas Malik**  
📫 [LinkedIn](https://github.com/malik-vishu)  

---

⭐️ **If you found this helpful, please star the repository!**
