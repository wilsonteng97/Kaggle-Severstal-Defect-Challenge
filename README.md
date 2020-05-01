# Kaggle-Severstal-Defect-Challenge
For CZ4041 Group 28 | WIlson Teng, Benedict Low, Swa Ju Xiang, Teo Boon Shuan, Arthur Koh

**All Notebooks are Ran on Kaggle with GPU and Internet Turned On with the exception of the Stage 5**

This project consists of 5 different notebooks:        

## 1) **Group 28 Stage 1 (Test Missing Count)**        
This notebook performs the binary classification of the images, by allocating an allMissing score to each test image.       
                      
**Output:**          
	`dense121_model.h5`            
	`history.csv`               
	`model.h5`                  
	`test_missing_count.csv`            
                   
## 2) **Group 28 Stage 2 (Train Missing Count)**                     
This notebook uses the model trained in Stage 1 and apply it to the train images to obtain their individual allMissing score.                  

To run this notebook, the .h5 file from Stage 1 is required:                    
	`model.h5`                     
	     
The filepath stated in this notebook is with respect to the Kaggle directory.                   
To run this code you would need to upload the .h5 file into the notebook's working directory on Kaggle.                    
Name the dataset Stage1.                   
	
**Output:**                      
	`train_missing_count.csv`                             

## 3) **Group 28 Stage 3 (EDA to find optimal threshold for Stage 4)**                             
This notebook performs an EDA to determine the optimal threshold of allMissing score to split the dataset into two groups with the highest percentage of defect images and non defect images respectively.                    
                 
To run this notebook, two .csv files from Stage 1 and 2 is required:
	`train_missing_count.csv`
	`test_missing_count.csv`
	           
The filepath stated in this notebook is with respect to the Kaggle directory. 
To run this code you would need to upload the .csv files into the notebook's working directory on Kaggle.                        
Name the dataset Stage2.
                            
## 4) Group 28 Stage 4 (Segmentation)    
This notebook performs the segmentation task of classifying the defect class of the pixels.                    
                	           
The filepath stated in this notebook is with respect to the Kaggle directory. 
To run this code you would need to upload the .csv files into the notebook's working directory on Kaggle.                        
Name the dataset Stage4.

**Output:**                      
	`submission.csv` : This csv file is the pre post-processing csv file.                   
        `model.pth`                    
        `Unet_visualization.svg`                      

## 5) Group 28 Stage 5 (Inference Notebook)                           
This notebook performs the post-processing task of removing false negatives using the binary classification model in Stage 1 and the threshold calculated in Stage 2.                    
                 
To run this notebook, two .csv files from Stage 1 and 2 is required:
         `submission.csv`
	`test_missing_count.csv`

The filepath stated in this notebook is with respect to the Kaggle directory. 
To run this code you would need to upload the .csv files into the notebook's working directory on Kaggle.    
	           
**Output:**                      
	`submission.csv`


## Results (0.88536 on Private LeaderBoard):
![Submission Results](/images/results.png)

