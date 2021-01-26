# BCS_Body_Condition_Score_Cattle_Prediction
BCS Project Description:

1.Problem Statement
•	Here we need to predict the BCS classes. Basically it’s a Multiclass Classification Problem.
•	We have 1,2,3,4 classes.



2.Preprocessing Steps & Feature Engineering

•	Here we have train , test data & labels.csv file. So based on this csv file i created  a separate folders . so that each folder indicates different classes (Class_1,Class_2,Class_3,Class_4) .


•	These data divided into train-valid data(each folder contains Class_1,Class_2,Class_3,Class_4 folders). You can find these in this file (Step_1_Train-Validation Split_final.ipynb).


•	here we have less amount of data. We applied a data agumentation steps & also applied transformations, filters on images like Gradient, Negative Images, Box filter , Adaptive + Gassiun thresholding , Discrete Fourier Transform , Est. transformation , Fitting Polygons , log_transformation , Gassiuan filters + Kernals , Canny_edge , Image_temparature , Contrast Stretching ,K-means , Keras augmentation. 


•	You can find all these image preprocessing steps in (Image Preprocessing.ipynb ) file.

•	After applying all the above feature engineering steps finally we’re with 2466 images of train,719 images of valid. 

•	Data Visualization analysis is available in (visualization.ipynb) file


3. Models Applied & Results 

•	We used a base CNN model along with Reguralization techniques(Drop out , Batch Normalization , MaxPooling) etc.

•	We have used activation functions ( Relu, swish) . and also used softmax as in the last layer.

•	Base CNN model given Train_Accuracy of 73.01% , Validation_Accuracy of 69.96% (After applying all filters & Keras augmentation). 

•	You Can see this model in (Base_CNN.ipynb) file

•	After this we tried with transfer learning techniques VGG16 , Resnet101.

•	The same preprocessed images  are given input to these above transfer techniques.

•	VGG16 has given Train_accuracy of  72.43% , Valid_accuracy of 68.98% (After applying all filters & Keras augmentation).

•	You Can see this in (VGG16.ipynb) file.

•	Resnet has given Train_accuracy of 70.85% , valid_accuracy 69.40% (After applying all filters & Keras augmentation).

•	You can see this in (Resnet101.ipynb) file.

•	You can see some of the model analysis results images are store in Output_images folder. 


