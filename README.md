# Iris-Recognition-CASIA-Iris-Thousand
![](/iris-testcases/image.jpg)

## Introduction

- This project introduces an innovative iris recognition technique designed to efficiently detect and classify iris images with exceptional accuracy. The iris recognition model initiates with an eye detection process, followed by iris detection to identify irises within the eyes. Subsequently, the iris segmentation process extracts iris images, which are then saved and utilized in the final stage responsible for iris classification using a convolutional neural network.<br/><br/>
- The dataset utilized in this project is CASIA-Iris-Thousand version 4, comprising 20,000 images from 1,000 distinct individuals. <br/> <br/>
- For the iris classification stage, the model employs a pre-trained convolutional neural network (CNN) model, specifically DenseNet-201, to achieve accurate classification results.




## Project Processes Overview

This project involves several processes aimed at detecting and classifying iris images. Below is an outline of each process:

- **eye_detection_2.py**: This script initiates the initial phase of the project, focusing on detecting eyes within images to ensure their presence.

- **eyes_iris_detection_2.py**: In this stage, the script is dedicated to detecting iris within the eyes identified in the previous phase. Only images with detectable irises proceed to the subsequent steps.

- **iris_segmentation_2.py**: This script handles the extraction of iris features, constituting the third phase of the process.

- **iris_extraction_2.py**: Consolidating the functionalities of the preceding scripts, this file orchestrates the sequence starting from eye detection, followed by iris segmentation. The resulting output is preserved for utilization in the iris classification phase.

- **iris_classification_2.ipynb**: Serving as the concluding phase, this notebook employs a pre-trained DenseNet-201 model for classifying iris images into 1000 distinct categories within the CASIA-Iris-Thousand version 4 dataset.

## TestCases :-


![](/iris-testcases/test-case2.jpg)

![](/iris-testcases/testcase3.jpg)

![](/iris-testcases/testcase4.jpg)

![](/iris-testcases/testcase5.jpg)






### To run this project you will need to:
1. Download the CASIA-Iris-Thousand dataset from this link [CASIA-Iris-Thousand]( http://www.cbsr.ia.ac.cn/china/Iris%20Databases%20CH.asp)

2. Change your directory names that contain the dataset to the name in the python and notebook files in these  lines:<br/>
    - In iris_extreaction_2.py:
 
         ```html
        #here create directory name that contain the dataset "CASIA-Iris-Thousand/"
        
        for filepath in glob.iglob('CASIA-Iris-Thousand/*'):

        #here create  directory name that contain the the extracted iris feautres "final_ casia/"
        cv2.imwrite('final_ casia/'+str(L)+'.'+str(number)+".jpg",new_roi)

        ```
    - In iris_classification_2.ipynb:

         ```html
        # here directory name is "final_casia" which contain extracted iris features

        
        for filefilepath in glob.iglob('final_ casia/*'):

        ```
3. Run iris_extraction_2.py.

4. Open iris_classification_2.ipynb and run it's cells.



