# Task 3: Multimodal House Price Prediction

**Intern Name:** Aimen Irfan  

This project predicts house prices using both tabular features and images of houses. The model combines traditional tabular data with image features extracted from a small Convolutional Neural Network (CNN), creating a multimodal deep learning pipeline.  

---

## Description

The goal of this project is to predict the price of a house based on:

- **Tabular features:** Bedrooms, bathrooms, square footage, and other property details.
- **Image features:** House photos processed through a CNN.

The pipeline includes:

1. **Data Loading:**
   - Tabular data from Kaggle (`socal2.csv`).
   - Images of houses (`socal_pics` folder).

2. **Data Preprocessing:**
   - Standardization of numeric tabular features.
   - Image resizing, conversion to tensor, and normalization.

3. **Custom Dataset:**
   - PyTorch `Dataset` combining tabular and image data for training and evaluation.

4. **Model Architecture:**
   - CNN for image feature extraction.
   - MLP (feed-forward network) for tabular data.
   - Fusion layer combining both feature sets for final regression output.

5. **Training & Evaluation:**
   - Mean Squared Error (MSE) loss function.
   - Optimizer: Adam.
   - Metrics: Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
   - Model checkpointing for best validation performance.

6. **Deployment:**
   - Gradio web interface for live predictions.
   - Input: Image and tabular features.
   - Output: Predicted house price.

---

## Summary

- **Dataset:** Kaggle House Prices with Images (Socal dataset)
- **Model:** CNN (images) + MLP (tabular features)
- **Evaluation Metrics:** Test MAE ≈ 232,567, RMSE ≈ 320,441
- **Output:** Saved model (`house_price_model.pth`)
- **Deployment:** Gradio app for interactive inference
- **Key Skills:** Multimodal ML, CNNs, PyTorch, regression modeling, Gradio deployment

---

## How to Run

1. Clone the repository:

```bash
git clone <your-github-repo-link>
cd Task3
