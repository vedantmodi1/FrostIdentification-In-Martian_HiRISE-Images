# FrostIdentification-In-Martian_HiRISE-Images

In this project, I build a classifier that distinguishes images of Martian terrain with frost. This dataset was created to study Mars’ seasonal frost cycle and its role in the planet’s climate and surface evolution over the past 2 billion years. The data helps in identifying low-latitude frosted microclimates and their impact on climate.

I have compared the use of a custom CNN model as compared to three transfer learning model, both cases with and without image augmentation.

Analysis of Model Performance with and without Data Augmentation
Impact of Augmentation on Custom CNN and Transfer Learning Models:
Custom CNN:
The introduction of augmented data, both appended and standalone, led to a reduction in test accuracy compared to the model trained on the original un-augmented data. This indicates that, in this case, data augmentation may not have contributed positively to the CNN's performance.

EfficientNet:
EfficientNet exhibited a trend where applying data augmentation and appending it to the training set did not significantly affect test accuracy. However, it did result in a reduction in test loss. Augmenting all training data, surprisingly, reduced test accuracy. Further investigation might be required to understand the nuances of EfficientNet's response to augmentation.

ResNet50:
Unlike the custom CNN and EfficientNet, ResNet50 only showcased an decline in test accuracy when augmented data was appended. This implies that independent data augmentation benefited the transfer learning of ResNet50.

VGG16:
The behavior of VGG16 was unique, where appending augmented data to the original set decreased test accuracy, but augmenting all training data led to a relative increase in test accuracy. Understanding the specific characteristics of VGG16's response to augmentation can guide future model adjustments.

Transfer Learning vs Custom CNN:
Custom CNN vs Transfer Learning Models:
While state-of-the-art transfer learning models like EfficientNet, ResNet50, and VGG16 are pretrained on extensive datasets, they may not universally outperform a well-designed custom CNN for every use case.

The custom CNN achieved the highest test accuracy at 91.27%, showcasing its effectiveness for this specific task. In contrast, EfficientNet struggled to surpass 39.53% accuracy across all cases.

Performance Variation with Data Augmentation:
Notably, despite the custom CNN's strong performance on unaugmented data, ResNet50 and VGG16 surpassed its accuracy by over 30% points when evaluated on augmented data. This underscores the importance of considering data augmentation when choosing between custom CNNs and transfer learning models.
