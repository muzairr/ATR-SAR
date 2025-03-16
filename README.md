![image](https://github.com/user-attachments/assets/0770df89-8757-4685-920d-0c7b3470645e)# ATR-SAR
Automatic Target Recognition using SAR Imagery
Follow the steps to run the code:

Extract the terrasar.zip file.
Open the terrasar/python folder open the terraSAR.py and terraSAR_vid.py files.
Change the paths of 'yolo.names', 'yolov3_custom_train_final.weights' and 'yolov3_custom_train.cfg' in the terraSAR.py and terraSAR_vid.py files.
Now run the terrasar.exe file in terrasar/obj folder.
****Abstract****
One of the most important tasks in the image analysis is the classification as we use the labels from the image data and transform it into real-world word information. In this study, we have worked on achieving the task of classification on the real-world Synthetic Aperture Radar (SAR) Imagery. The simple optical images are not that useful at night times and when there is a lot of cloud coverage in the atmosphere which makes it imperative that we deal with the SAR data for gathering information. This task is quite important as the SAR images are not like the optical images in which we can see and identify the object using our eyes, so that is why we need computers so we can know exactly what kind of objects are present with high accuracy and efficiency. Our task has majorly been to find what type of target is in the image which is the classification part as well as finding the target exactly where it is in the whole image which is the identification part. Our solution is composed of using a deep neural network to get rid of the unnecessary clutter and get the most important features. This solution can be used on any kind of data which would be available so it is a framework which can work on the SAR data and help us find the targets with high accuracy.

****Objectives****
Getting the information about the enemy territory and its vehicle positioning.
Help the security institutions to correctly identify the type of targets from the satellite data.
Identifying where the target is in the current terrain is.
Analyzing a more efficient and higher accuracy method for classification.
**Structure**
![image](https://github.com/user-attachments/assets/98686a8c-a61d-4f28-9923-2493d6550932)


****Methodology****
**Data Acquisition - MSTAR**
The Moving and Stationary Target Acquisition and Identification (MSTAR) Program is a collaborative initiative between the Defense Advanced Research Projects Organization (DARPA) and the Air Force Research Laboratory (AFRL) to develop and test the advanced ATR system.' The program started in June 1995 and would conclude at the conclude of 1999. The curriculum stressed the need to tackle extended operational situations (EOCs), i.e. situations that vary from all those found in the training data available and focused heavily upon model-based (CAD and Bayesian) technologies. The MSTAR software performed systematic assessments of the efficiency of the network every fall (1996, 1997, and 1998). The evaluation of ATR is an essential foundation for technical and algorithmic decision-making. Analytical judgments may include. The selection among two various options to some subsystem or the recognition of weak links inside the system. Programming decisions may entail competitive down-selects or innovations transformations to users. Assessment of any kind. The "trained" system has its challenges, but the evaluation of ATRs seems to be particularly problematic due to limitations. Accessible data are relative to the magnitude of the issue. The dataset has 8 targets with multiple angles and each angle contain around 49 images.
![image](https://github.com/user-attachments/assets/89a0d33b-7564-41fd-bf49-e62ee01596e6)
![image](https://github.com/user-attachments/assets/920b24a1-b58a-45a5-abea-44269439d71c)
![image](https://github.com/user-attachments/assets/4f335a4d-e5ad-4717-aa03-da1f5b7f12b1)



**Model Architecture**
The model which has been finalized to be used for the classifications is YOLOv3. The major reason behind using this algorithm is that not only it detects what type of target is in the image, it also detects and identifies where the target exists by enclosing it into a box which is quite an important thing in the SAR ATR. It helps in the real-time detection of the targets inside continuous video-based SAR imagery as well as images with a huge background. This is a step further than just classifying what is in a picture or the frame. YOLO used the convolution layers which makes it a full convolution network (FCN). The underlying architecture is called the Darknet-53, which is the feature extractor, it contains 53 convolution layers which is followed by the batch normalization layer each as well as Leaky activation. There is not sort of pooling being incorporated in this and stride 2 convolutions is used which downsamples the features.
![image](https://github.com/user-attachments/assets/2dbbc027-3246-4c2b-916b-9d6489b2ac5d)




**MVP Architecture**
Our project uses a Model-View-Presenter (MVP) approach for its system. It is a derivation of the Model-View-Controller approach. MVP comprises of three components Model, View and Presenter

![image](https://github.com/user-attachments/assets/0e2c34f3-9377-4d71-8675-cd1df9ab96eb)


**Interface**
![image](https://github.com/user-attachments/assets/f7b2200c-1442-4c2c-86fb-209dcd7dcad5)


![image](https://github.com/user-attachments/assets/979b53c5-b01b-46f6-9229-1dc4a0037858)


**Image Detection**
This is the main feature of the systems which takes the input of the SAR image and identify the targets and classify them very quickly. This shows the Browse image option after which we can use the detect image to find the targets.

![image](https://github.com/user-attachments/assets/fe14bb50-97d4-4744-8229-3b056ac9b009)


**Video Detection**
The video detection works the same way the image detection work and gets the input from the file directory you use and give the output with an actual video which shows the target being highlighted and even the moving target is a also identified with constant highlighting the target which is the key part in real-time classification.

![image](https://github.com/user-attachments/assets/8de06bbb-99de-477a-a8ef-c0d0a03be239)


**Conclusion and Future Work******
TerraSAR is Pakistan’s first software for real-time target detection of SAR images. The system is designed to detect ground military vehicles especially during nighttime and bad weather conditions. YOLO architecture has been implemented in our system which provides better real-time target detection as compared to the competitive algorithms of FASTER R-CNN and SSD. We have trained our model on publicly available MSTAR dataset. TerraSAR will help defence institutions to correctly identify the type of targets and location of targets in the current terrain using satellite data. Our research and provided solution solve the problem of target detection for military and defence purposes that cannot be done through traditional optical satellites. TerraSAR provides an accuracy of 97-99% by using YOLO architecture. Our future work includes:

Using a larger set of datasets to reduce overfitting
Making a database of more images to avoid data augmentation
Original dataset (provided by defence institutions) can be used to train and generalize our model to provide better accuracy.
