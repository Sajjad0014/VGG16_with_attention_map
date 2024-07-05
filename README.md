# Improved Glioma Grading using Deep Learning Techniques

### BACKGROUND
	
Gliomas are a sort of primary brain tumor that originates from glial cells. These cells are accountable for supporting the central nervous system of the human body. These tumors vary widely based on their nature, they could be either malignant or aggressive. The survival rate for a patient with a high-grade tumor is low. Therefore, glioma grading is an essential part of diagnosis and treatment planning, as it can give critical information regarding the tumor’s characteristics and its behavior. 

![image](https://github.com/Sajjad0014/VGG16_with_attention_map/assets/77324837/ffa7c695-ee94-4733-809d-3e3af013cbfd)


## PURPOSE

Typically, tumor grade is determined by biopsy, which is an invasive and expensive process. Thus, a computer aided diagnosis (CAD) tool, which is fast, automated, and discreet, is needed for determination of tumor grade. A major drawback with ML techniques is the need for explicit extraction of features. On the other hand, convolutional neural networks (CNN) extract the most relevant features from scanned images. 

The key difference from other research projects is that an explicit segmentation step is required to locate the tumor region. Note that this pre-processing step of locating the tumor is challenging. In this project, I have proposed a deep learning model that helps in eliminating the segmentation step by using an attention layer, which allows you to focus on the tumor regions automatically. Moreover, classify the tumor whether it is high or low grade.

## Quick Start

1. **Kaggle Account**
   - Create a Kaggle account [here](https://www.kaggle.com/account/login).
3. **Clone the repository**
   - git clone https://github.com/Sajjad0014/VGG16_with_attention_map.git
4. **Navigate to the project directory**
   - cd VGG16_with_attention_map
2. **Prepare MRI Scans**
   - The patient’s dataset should be in a .nii format and it should contain 4 sequences, namely flair, t1, t1ce, and t2. A sample HGG patient dataset shall look like this: [Link](https://drive.google.com/drive/folders/1iwjKcridsm9hnkrTI85xJq3-PI1hK3jY?usp=sharing)
   - Copy this dataset to the project directory.
   - Run the code "nii to jpg converter.ipynb" by adding the respective directory of the patient folder in the “walk_path” variable. This will convert the “.nii” images into jpg format.
   - The dataset generated will have a few empty images at the start and end of each sequence. Run the code “Remove Blank images.py” by adding the respective directory of the patient folder in the “walk_path” variable. This will remove all the blank images. After removing it, the folder should look like this: [Link](https://drive.google.com/drive/folders/1FLE1CoHPbNE9pd-du7cDW0X-2CNWtGUH?usp=sharing)
   - Sample images
 	![image](https://github.com/Sajjad0014/VGG16_with_attention_map/assets/77324837/d9b69230-7af5-4327-97aa-4d1c848d4f36)

4. **Steps to Run the Code on Kaggle:**
   - zip the patient dataset folder and upload it to your Kaggle account by clicking on the “+ Create” button on the Kaggle homepage.
     ![image](https://github.com/Sajjad0014/VGG16_with_attention_map/assets/77324837/80bde91d-febd-4197-9cda-f88729c8dd95)
     
   - Also upload the trained model by clicking “New Dataset”
   - Similarly click on “New Notebook” in the “+ Create” button.
   - After opening the new notebook click on “Import Notebook” and import the “Test your model on a Single Patient.ipynb” to your Kaggle account.
     
     ![image](https://github.com/Sajjad0014/VGG16_with_attention_map/assets/77324837/2117ef9f-18a9-4625-88bf-8259d237005d)
     
   - Make necessary changes in the code, such as adding all the directories in respective fields like “image_dir”, “model_dir”.
   - It’s ready. Now run the code!

## Usage
   **Determine the grade of the glioma:** Use the trained model to classify gliomas as high or low grade.
   
   **Visualize the tumor region:** Utilize the attention mechanism to highlight and focus on the tumor regions in MRI scans.
   Visualizations should look something like this:
   
   ![image](https://github.com/Sajjad0014/VGG16_with_attention_map/assets/77324837/6951dee6-9b4f-4103-b7e7-3b7506698302)


## Contribution

Contributions to this project are welcome. Please follow the standard procedures for contributing to open-source projects. If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.
