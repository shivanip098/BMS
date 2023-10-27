# Automated Locomotor Ability Prediction
*This project utilizes data collected by the He lab and associates from Harvard and BCH*  

## Introduction
The purpose of this project was to select, train, and fine-tune a model capable of taking in various locomotor qualities and use this information to accurately assign mouse models to their placement on the Basso Mouse Scale (BMS). BMS is a locomotor scale that ranges from 0 to 9 and gives information on an injured mouse's capabilities. The data was collected using software capable of auto-detecting mouse features withihn videos on mice who had undergone a variety of controlled spinal cord injuries

## Configuration and Installation
To utilize this code, two datasets are needed. The autocalc parameters and the assigned BMS labels. Due to the nature of the data collection, the group responsible for collecting the movement data is separate from the parties responsible for assigning values on the BMS, resulting in the separate dataframes.

## Contact Information
If you have any questions or suggestions for this project, please feel free to contact me at shivanip098@gmail.com !

## Challenges
The main challenges faced were with the actual model selection. The context of the data is essential to choosing the correct model. While it is standard practice to remove rows and columns that are missing data above a certain threshold, the size of the dataframe as well as the fact that a 0 on the BMS means that there might not be any movement, kept me from doing so. Instead, I focused on finding models that were capable of natively handling NaN values. Additionally, because the values on the BMS are not regularly spaced out, the values are practically arbitrary. For this reason, I chose to also focus on finding models capable of ordinal classification as opposed to regression models.

## Credits
Thank you to the He Lab as well as the countless labs who have worked with the BMS for providing the data sources used within this project.
