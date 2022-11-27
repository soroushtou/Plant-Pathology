# Plant-Pathology
Training Program to classify apple foliar diseases.
You Can Change The model in "Model" section.
The current model trained by this program can achieve 84% accuracy on hidden test data in Kaggle Comptetion:
https://www.kaggle.com/competitions/plant-pathology-2021-fgvc8/leaderboard
This project is also my Master's Thesis.
___________________________________________________________________________________

![1](https://github.com/soroushtou/Plant-Pathology/blob/main/images/1%20(5).png)
This is the distribution of classes in the dataset. It has 6 single label classes, and the other 6 are multi-labeled. It's completely imbalanced!!
___________________________________________________________________________________

I'm splitting the multi-labeled classes and treat this problem as a multi-label classification problem.
![2](https://github.com/soroushtou/Plant-Pathology/blob/main/images/1%20(1).png)
![3](https://github.com/soroushtou/Plant-Pathology/blob/main/images/1%20(2).png)
Some labels are noisy and need to be softened, especially in case of "complex" images.

___________________________________________________________________________________

![4](https://github.com/soroushtou/Plant-Pathology/blob/main/images/1%20(3).png)

Batches of 20 images, 400x400 pixels, and normalized are sent to a GTX 1080Ti. All models are pretrained and I use Transfer Learning to fine-tune them. They are trained for 30 epochs and when they reach the minimum loss, they are saved. Then they are uploaded to kaggle to test their accuracy.

![5](https://github.com/soroushtou/Plant-Pathology/blob/main/images/1%20(4).png)
