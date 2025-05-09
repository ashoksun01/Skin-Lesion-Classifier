# LesionLens - Skin Lesion Classification Using Deep Learning

## Project Summary
LesionLens is a machine learning-powered web application that provides near-instant visual diagnostic support for skin lesions, classifying them as malignant or benign. The project addresses the global issue of melanoma and other skin cancers, which are often misdiagnosed due to visual similarities between benign and malignant lesions. By offering a low-cost, accessible diagnostic support tool, LesionLens aims to reduce unnecessary biopsies, improve early detection, and make dermatological care more accessible.

- **Problem:** Melanoma and other malignant skin lesions are challenging to differentiate visually, even for trained clinicians, leading to high biopsy rates and delayed care. 
- **Solution:** LesionLens provides real-time diagnostic support using a machine learning model that classifies user-uploaded images of skin lesions. It offers guidance on potential malignancy risk while emphasizing the need for professional consultation.
- **Target Users:** High-risk individuals with frequent lesions, people avoiding care due to cost or inconvenience, and anyone seeking quick, reliable information about their skin lesions.

---

## 🚀 Demo
Check out the live demo of LesionLens: [LesionLens Demo](https://www.youtube.com/watch?v=rn0gUaACZ3k)

This demo showcases how users can upload images of their skin lesions and receive immediate diagnostic support using our machine learning-powered model.

---

## Repository Structure

- **data_preprocessing_pipeline.ipynb**: Jupyter notebook for image data preprocessing (resizing, noise removal, masking, augmentation, normalization).
- **final_models.ipynb**: Jupyter notebook for model training, fine-tuning, and ensemble creation.
- **lesionlens_slides.pdf**: Presentation slides providing an overview of the project.

### What This Repository Contains
- **Data Preprocessing Pipeline:** Contains the full code for cleaning, augmenting, and preparing image data for model training.
- **Model Training and Fine-Tuning:** Contains the complete process of building, training, and fine-tuning deep learning models for skin lesion classification.
- **Presentation Slides:** A PDF with a visual overview of the LesionLens project, covering the problem, approach, and results.

### What This Repository Does Not Contain
- **Frontend Code:** The code for the user interface of the LesionLens web application is not included.
- **Backend Code:** The server-side code and deployment scripts for the LesionLens web application are not included.
- **Raw Image Data:** The image datasets used for training the models are not included for privacy and storage reasons.

---

## How It Works
1. **Image Upload:** Users upload an image of their skin lesion through the web application.
2. **Preprocessing:** The image is processed (resizing, noise removal, RGB normalization) to ensure consistent quality.
3. **Classification:** The processed image is fed into the trained model ensemble (MobileNet, DenseNet121, DenseNet169, NASNetMobile), which classifies the lesion as malignant or benign.
4. **Results Display:** The model provides a diagnostic support result with a probability score, along with guidance to consult a dermatologist.

---

## Model Performance
LesionLens outperformed human expert classification in diagnosing malignant skin lesions, achieving the following metrics:

| Model                     | Accuracy | Precision | Recall | F1 Score | AUC  |
|---------------------------|-----------|------------|--------|-----------|------|
| LesionLens Final Model     | 87.4%     | 86.7%      | 87.4%  | 86.6%     | 76.1%|
| Best External Model        | 88.8%     | Not reported| 83.8%  | Not reported| 88.8%|
| Human Expert Classification| 84.0%     | Not reported| 85.5%  | Not reported| 71.0%|

---

## Key Learnings & Impact
- **Image Quality:** Handling user-uploaded images required robust preprocessing techniques (resizing, noise removal, masking).
- **Class Balancing:** Augmentation methods helped improve model robustness by generating synthetic data for underrepresented classes.
- **Ensemble Approach:** A stacked logistic regression ensemble of MobileNet, DenseNet121, DenseNet169, and NASNetMobile models provided the best performance.
- **Accessible Diagnostics:** LesionLens provides diagnostic support directly to users, lowering barriers to early skin cancer detection.

---

## Future Improvements
- **Enhanced Image Preprocessing:** Integrate additional image preprocessing techniques for better noise handling.
- **Expanded Classification:** Extend the model to classify multiple types of skin conditions, beyond just binary (malignant/benign).
- **Continuous Model Improvement:** Implement user feedback for continuous model refinement.
