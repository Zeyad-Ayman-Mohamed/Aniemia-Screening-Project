# Aniemia-Screening-Project

## Introduction
Anemia is one of the most common health issues in third world countries. According to the World Health Organization (WHO), nearly a quarter of the human population suffers from anemia.
The image of the eye is captured and the eye conjunctiva is automatically extracted from the image as a Region of Interest (ROI). The ROI is then processed and features are extracted from it to train a machine-learning algorithm to determine if the patient is anemic or not.

## Project pipeline

![alt text][fig1]

[fig1]:https://github.com/Zeyad-Ayman-Mohamed/Aniemia-Screening-Project/blob/main/images/A1.png

## Dataset
The dataset used for training the model was Eyes-defy-anemia. The dataset contains 218 patients of both Indian and Italian nationalities. Out of these images, 99 are anemic while 119 are non-anemic(healthy). The dataset also contains manually segmented palpebral 216 images, fornical 212, and palpebral + forniceal conjunctiva 212  in addition to 218  eye images that can be used for custom segmentation. Some subjects’ images were not segmented. The images were captured with a Samsung S6 smartphone, equipped with a particular device that magnifies images, standardizes lighting, and eliminates the influence of ambient light. So, all the images were captured from the same distance and with the same white LED light

ROI image 

![alt text][fig2]

[fig2]:https://github.com/Zeyad-Ayman-Mohamed/Aniemia-Screening-Project/blob/main/images/A2.png

![alt text][fig3]

[fig3]:https://github.com/Zeyad-Ayman-Mohamed/Aniemia-Screening-Project/blob/main/images/A3.png


## Feature selection

The features that will be used are the mean intensity of green and red components of ROI.
As shown in following figures, the blue component is irrelevant and cannot be used to differentiate between anemic and non-anemic. as here we only need to calculate green and red mean intestines as they what implies hemoglobin level.

![alt text][fig4]

[fig4]:https://github.com/Zeyad-Ayman-Mohamed/Aniemia-Screening-Project/blob/main/images/A4.png

![alt text][fig5]

[fig5]:https://github.com/Zeyad-Ayman-Mohamed/Aniemia-Screening-Project/blob/main/images/A5.png

## Models used 
a modified SVM(Support Vector Machine) was used, along with KNN, Decision tree, and logistic regression.

## Results
Metric| Log Reg| SVM| Tree| KNN|       
--- | --- | --- | --- |  ---  |
Score | 0.75 | 0.58  | 0.64 |0.84 



