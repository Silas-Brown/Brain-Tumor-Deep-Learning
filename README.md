# Brain-Tumor-Deep-Learning

## (1) Overview  

We use 3064 brain images to distinguish and predict three kinds of tumors: Meningioma, glioma, and pituitary tumors with 708, 1426, and 930 images for each class respectively. 

✅ **Dataset:** 3064 images, 3 classes (Meningioma, Glioma, Pituitary tumors)   
✅ **Goal:** Predict and distinguish the 3 tumors  
✅ **Result:** A custom performance metric normalized between 0 and 1 scoring 0.835.
---

## (2) Methodology  
### 🔹 (2.1) Defining the hyperparameter space
  - **Using theory to infer a reasonable, efficient search space that respects computational costs and learning**
  - **Hyperparameter defined as resolution of images, batch size, number of hidden layers**
  - **Hyperparameter search space defined as**
      - Resolution in {128 x 128, 256 x 256}
      - Batch sizes in {32, 64}
      - Layers in {2, 3, 4}
 ### 🔹 (2.2) Designing the neural architecture of the model
   - **Make earlier layers extremely wide but abruptly narrow the deeper layers**
 ### 🔹 (2.3) Custom loss function. Custom performance metric to maximize with respect to hyperparameter.
   - **Loss function is a weighted cross-entropy function weighted based on the mortality risks of each tumor**
   - **Performance metric is a weighted combination of F1-scores weighted on the same principles as the loss function. Normalized to be between 0 and 1 for easier interpretability.**
 ### 🔹 (2.4) Hyperparameter grid search and early stopping for each model training
   - **Best configuration is (resolution, batch size, hidden layers)=(128x128, 64, 2)**
   - **Early stopping for each model with maximum epochs of 50, patience of 5, and min_delta of 0.005**

## (3) Implementation  

### **🔗 Full Implementation in Colab:**  
https://colab.research.google.com/drive/1eVoLfGZiMh0AS-hb1pFFrILkTDfG6nzC?usp=sharing
## (5) Contact  
📧 Email: **silasaverybrown@gmail.com**  
💡 LinkedIn: [Silas Brown](https://www.linkedin.com/in/silas-brown/) 



