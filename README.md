# Distracted-Driver-Detection-Deep-Learning

## Problem Space
According to CDC motor vehicle safety division, 20% of car accidents are caused by distracted drivers who are either spotted texting, talking over the phone. These accidents can be avoided by tracking driver behaviour. We hope to improve these statistics and reduce the fatality rate by analyzing images of drivers using the dataset from the Kaggle competition - ’State Farm Distracted Driver Detection’.

We have built models using Fully Connected Layers and CNNs. Also, we have compared and consolidated the performance of using transfer learning techniques like ResNet-152 and Inception V3 to assess the performance and get an overall idea of how deep learning models/techniques perform for this dataset. Apart from this, we have analyzed how these models work for every data class(driver behaviour) by assessing the number of false predictions each model predicts. 

## Dataset

The publicly available Statefarm Distarcted Driver Detection dataset is used for training and testing our proposed model. This dataset consists of 22,400 training images. As we do not have access to the test dataset, we have divided the available train data set into 3 classes for training, validating and testing the model. 70% of the train set will be used for training with 15% each being used for validating and testing the model. 
Train Data:  Approx. 19,000 Images
Test Data:  Approx. 3000 Images

Class Labels:
- Safe driving
- Texting - right 
- Talking on the phone - right
- Texting - left
- Talking on the phone - left 
- Operating the radio
- Drinking
- Reaching behind
- Hair and makeup
- Talking to passenger

## Approach

- Pre-Processing:
  - Image re-sizing
  - Converting images to grayscale – for Simple CNN Model
  - One Hot Encoding of class labels
- Model Architecture:
  - CNN Model
  - ResNet-152 
  - Inception V3 
  
## Architecture for CNN Model
<img width="450" alt="Model Arch" src="https://user-images.githubusercontent.com/29837264/177228188-c31a6204-2482-4f30-908a-83cf1674c760.png">

## Results

The predicted labels are compared against the actual label to evaluate the performance of the model using accuracy score and LogLoss value. 

| No. | Approach | Test Accuracy | LogLoss | 
|-----|----------|---------------|---------|
| Exp. 1 | CNN model | 86.3% | 0.538 |
| Exp. 2 | Pretrained: ResNet-152 | 89.6% | 0.362 |
| Exp. 3 | Pretrained: InceptionV3 |  93.5% | 1.73 |

### Key Insights 

- CNN model - achieve comparable performance as complex pretrained models.
- Complex models require more memory and processing power.
- From the experiments conducted, we were successfully able to detect driver distraction behavior correctly approx. 90% of the times tested.


