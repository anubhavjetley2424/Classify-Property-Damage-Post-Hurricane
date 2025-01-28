# Classify-Property-Damage-Post-Hurricane
Using Satellite Imagery and Computer Vision we will predict wether a property is damaged by analysing images of the property and neighbouring areas of the property.

![image](https://github.com/user-attachments/assets/4df213d1-8499-47f3-90c2-e28c69b9acfe)


# Datset 
https://www.kaggle.com/datasets/swarnava007/post-hurricane

- train_another: the training data; 5000 images of each class(damage/no damage)
- validation_another: the validation data; 1000 images of each class(damage/no damage)
- test_another: the unbalanced test data; 8000/1000 images of damaged/undamaged classes
- test: the balanced test data; 1000 images of each class(damage/no damage)

![image](https://github.com/user-attachments/assets/45c03136-1b52-461e-8261-0545bbf4b095)


# Results 

Model Name	Accuracy(unbalanced test)	Loss(unbalanced test)	ROC_AUC	F1 Score	Model Parameter
- Baseline CNN	0.93811	0.28326	0.94336	0.75255	76993
- Custom CNN	0.95044	0.05006	0.92907	0.79428	664225
- ResNet50	0.98822	0.05006	0.99707	0.94586	57668481
- Xception	0.98922	0.03069	0.99927	0.95298	54942249

![image](https://github.com/user-attachments/assets/136267c7-ff7d-4cab-af81-c1123ae38eff)    ![image](https://github.com/user-attachments/assets/692f93aa-7b46-4912-b0b4-06de5c262383)

![image](https://github.com/user-attachments/assets/3244e7a9-3c78-4451-b1d9-ed99492c3332)

# Conclusion
1. The **Xception model** had low misclassification accuracy, **~1%** hence we can declare this model as the Best Model.
2. AUC score for ResNet50 and Xception model is `very close`.
3. F1 score is better for **Xception model** than ResNet50 model.
4. Xception model tooks less amout of time per epoch also **least number of epochs** for optimizing `minimun loss` for our case.
5. We also need to take care for `computational complexity` between ResNet50 and Xception model, **Xception model** has `less number of model parameter`.
6. We are going to use this **`Custom Xception model`** as our final model.
