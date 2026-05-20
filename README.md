# 🎭 Fairness-Aware Face Anti-Spoofing

A deep learning system for face presentation attack detection (PAD) that addresses demographic bias, ensuring equitable security performance across racial groups.

## 📌 What It Does
- Detects face spoofing attacks (printed photos, replayed videos) using **ResNet-50**
- Evaluates fairness across demographic groups (Asian, Black, White)
- Applies **bias mitigation techniques** to reduce demographic performance gaps
- Measures trade-offs between security performance and fairness

## 📊 Key Results
| Model | AUC (%) | Error Gap |
|-------|---------|-----------|
| Baseline | 47.7 | 12.8% |
| Balanced Sampling | 52.7 | Reduced by 20.3% |
| Loss Re-weighting | 45.5 | — |
| Combined | 51.2 | — |

## 🛠️ Fairness Techniques Applied
- **Balanced Sampling** — equal demographic representation per mini-batch
- **Loss Re-weighting** — higher weights for poorly performing groups
- **Combined Approach** — both techniques together

## 📁 Project Structure
├── PAD_Fairness_Colab_Final.ipynb  # Main implementation notebook
├── requirements.txt                 # Dependencies
├── roc.png                         # ROC curves comparison
├── score_hist.png                  # Score distributions by group
├── table_baseline.csv              # Baseline results
├── table_groupwise.csv             # Group-wise performance
└── table_fairness.csv              # Fairness methods comparison

## 🔧 Tech Stack
- **Python, PyTorch** — model implementation
- **ResNet-50** — base architecture
- **FairFace Dataset** — demographic classifier training
- **Replay-Attack Dataset** — PAD evaluation

## 📚 Background
This work addresses a critical gap in biometric security — most PAD systems report only aggregate accuracy without examining demographic fairness. Inspired by Gender Shades research, this project extends fairness evaluation to face anti-spoofing.

## 👩‍💻 Author
**Dharani Punniyamoorthi**
- LinkedIn: [linkedin.com/in/dharanipunniyamoorthi](https://linkedin.com/in/dharanipunniyamoorthi)
- Email: dharanimoorthi2002@gmail.com
