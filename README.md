# Transformer Models for Voltage Prediction

This repository provides the trained Transformer-based models, and interpretability outputs for **voltage prediction of battery electrode materials**. It includes baseline metrics, per-ion analysis with weighted sampling, and SHAP-based feature attribution.

---


## Repository Structure

```text
baseline_metrics_and_bootstrapping/  
├── entire_model_transformer_*.pth  
├── sd_transformer_*.ipynb        # Baseline & bootstrapping notebooks  

per-ion-metrics/
├── entire_model_transformer_*.pth  
├── *_weighted_sampling.ipynb     # Weighted-sample training for rare ions  
├── base.ipynb  
├── ffn.ipynb  
├── rnn_gru.ipynb  
├── rnn_lstm.ipynb  

shap/
├── Base_Transformer_global.ipynb  
├── FNN_global.ipynb  
├── GRU_global.ipynb  
├── LSTM_local.ipynb  

```


## 📑 Contents
 
- **Trained Models**: Saved PyTorch `.pth` files for:  
  - Base Transformer  
  - Transformer + FFNN  
  - Transformer + GRU  
  - Transformer + LSTM  
- **Weighted-Sample Models**: Versions trained with loss weighting to improve per-ion accuracy on underrepresented ions (e.g., Rb, Y).  
- **Baseline Metrics & Bootstrapping**: Scripts for error metrics (MAE, MSE, R²) and bootstrapped confidence intervals.  
- **Per-Ion Metrics**: Training and evaluation notebooks with weighted sampling.  
- **SHAP Interpretability**: Global and local SHAP analyses for feature importance and case-by-case explanations.  

---
