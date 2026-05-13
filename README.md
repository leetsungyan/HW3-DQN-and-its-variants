# Homework 3: DQN and its Variants

## 環境說明

本作業使用 GridWorld 4×4 格子地圖環境，AI 需要學會移動到 Goal 並避開 Pit 和 Wall。

```
符號說明：
P = Player（AI 代理人）
+ = Goal（目標，reward +10）
- = Pit（陷阱，reward -10）
W = Wall（牆壁）
```

三種訓練模式：
- `static`：所有物件位置固定
- `player`：玩家位置隨機，其他固定
- `random`：所有物件位置全部隨機

---

## 作業內容

### HW3-1：Naive DQN for Static Mode（30%）
- 實作基本 DQN，包含 Experience Replay Buffer 和 Target Network
- 環境：static mode
- 結果：勝率 94.6%
- 檔案：`HW3_1_Naive_DQN.ipynb`

### HW3-2：Enhanced DQN Variants for Player Mode（40%）
- 實作並比較三個版本：Naive DQN、Double DQN、Dueling DQN
- 環境：player mode
- 結果：三個版本勝率均達 100%
- 檔案：`HW3_2_DQN_Variants.ipynb`

### HW3-3：Enhanced DQN for Random Mode with Training Tips（30%）
- 將 DQN 改寫為 PyTorch Lightning 框架
- 加入三個訓練技巧：Gradient Clipping、Learning Rate Scheduling、ε 指數衰減
- 環境：random mode
- 結果：勝率 86%
- 檔案：`HW3_3_Lightning.ipynb`

### HW3-4：Rainbow DQN for Random Mode（加分題）
- 整合五個技術：Double DQN、Dueling DQN、PER、n-step Returns、Noisy Nets
- 環境：random mode
- 結果：勝率 88.2%
- 檔案：`HW3_4_Rainbow.ipynb`

---

## 環境需求

```
torch
numpy
matplotlib
lightning
```

在 Google Colab 執行時，每份 notebook 的第一個 cell 會自動下載所需環境檔案。

---

## 勝率總結

| 作業 | 方法 | 環境 | 勝率 |
|------|------|------|------|
| HW3-1 | Naive DQN + Experience Replay + Target Network | random | 94.6% |
| HW3-2 | Naive / Double / Dueling DQN | player | 100% |
| HW3-3 | PyTorch Lightning + 訓練技巧 | random | 86% |
| HW3-4 | Rainbow DQN | random | 88.2% |
