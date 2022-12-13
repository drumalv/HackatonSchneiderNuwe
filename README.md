# HackatonSchneiderNuwe
Solution to Schneider hackaton
Authors:
  - Beltrán Camacho, Álvaro.
  - Cabezas González de Lara, Sergio.
  - Gallego López, Pedro.
  
  
In [presentation.pdf](https://github.com/drumalv/HackatonSchneiderNuwe/blob/main/presentation.pdf) you can see a brief explanation about the solution. Also in [main.ipynb](https://github.com/drumalv/HackatonSchneiderNuwe/blob/main/main.ipynb) you can see the solution properly.

## Final Hackaton Score:
- **Ranking position**: 7 / 203 (top 3.5%)
- **Score**: 961 / 1200
- **Nuwe's Feedback** (This is the feedback given by our experts): Excellent presentation, very clear and visual! Regarding the code there are some functions that can be used from keras (to_categorical) to make it more elegant and several PyDocs of the functions are missing. For the rest of the code I see good concepts of OOP and very original the idea of using clustering by regions!


## Hackaton Description
  
### Background
Deforestation is the permanent removal of standing forests, which occurs for a variety of reasons and has many devastating consequences. The loss of trees and other vegetation can cause climate change, desertification, soil erosion, fewer crops, flooding, increased greenhouse gases in the atmosphere, and a host of problems for Indigenous people. In the last 13 years, more than 43 million hectares of forest have been devastated in the world, an area the size of California, USA. It is important to stop deforestation, as soon as possible, before the damage is irreversible. There are many ways to fight deforestation. This challenge will consist of using the help of thousands of satellites in space to capture images of the earth's surface in order to detect, as soon as possible, areas in the midst of deforestation and prevent its expansion.

### Dataset
For this challenge, you will have 2 CSVs: Train and Test. As their names indicate, the first one will be used to train your classification model on the forest images and test to know to which label they belong. It is important to remember to be careful with the paths for reading images in the train_test_data folder.

You will have the following attributes to be able to make the classifications:

- **latitude**: Where the photo latitude was taken.
- **longitude**: Where the photo longitude was taken.
- **year**: Year, in which the photo was taken.
- **example_path**: Path where the sample image is located.
- **label**: In this column you will have the following categories:
- **'Plantation'**:Encoded with number 0, Network of rectangular plantation blocks, connected by a well-defined road grid. In hilly areas the layout of the plantation may follow topographic features. In this group you can find: Oil Palm Plantation, Timber Plantation and Other large-scale plantations.
- **'Grassland/Shrubland'**: Encoded with number 1, Large homogeneous areas with few or sparse shrubs or trees, and which are generally persistent. Distinguished by the absence of signs of agriculture, such as clearly defined field boundaries.
- **'Smallholder Agriculture'**: Encoded with number 2, Small scale area, in which you can find deforestation covered by agriculture, mixed plantation or oil palm plantation.

For this challenge, you will have to predict the class of the deforested area.

There are three downloadable files:

- train_SE.csv: It is a table that relates the images of the training dataset with the attributes of the image.
- test.csv: It is a table that relates the images of the testing dataset with the attributes of the image. 
- train_test_data.zip: It is a zipped folder containing the training image datasets and testing datasets. 


### Task
- Create a classification predictive model in order to be able to classify the testing images. First train your model with the training images, once you have the model that maximize the f1-score (macro.) use the test images as input for your model.
- Create a presentation (MAX 4 slides) explaining what you have done and why you have done it.

### Submission
You must submit the link to your GitHub challenge repository (must be PUBLIC).

You must have at least the following 3 files in your Github repository (the name must be the same as below):

- predictions.json
- main.ipynb or main.py
- presentation.pdf

##### File 1: predictions.json
Predictions must be in a JSON file named as predictions.json, an example can be found in the following link

In this predictions file, in json format, each row will correspond to the predicted value of the test row, i.e. if the first value is a 2 it means that this 2 corresponds to the first file of the test dataset. It is IMPORTANT to call the column target as specified in the format. Remember that you can use the to_json function of pandas to convert your dataframe to json, length of predictions has to be the same as in test.csv.

The objectives score will come from applying the f1-score of the predictions you have made to the testing dataset with our ground truth.

IMPORTANT: Your predictions must be in int format (0, 1 or 2).

##### File 2: main.ipynb or main.py
This file must contain the source code of your solution. This file can be a notebook or a python document file. From this file the code quality will be evaluated.

##### File 3: presentation.pdf
This file should be a short presentation in PDF format explaining what you have done and how you have done it.

From this document the documentation score will be evaluated.


### Evaluation
Scoring is based on the following points:

100/1200:(DOC) Brief presentation explaining what you have done and how you have done it.
The evaluation will be taken into consideration the following:

700/1200:(OBJECTIVES) This will be obtained from the f1-score(macro) of the predictive model. Comparing the predictions your model has made about versus ground truth.

400/1200:(QUALITY) Code quality and automation, complexity, maintainability, reliability, and security.

