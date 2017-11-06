# Classifying Singaporean Food

This is a simple notebook that details the steps in creating a CNN based classifer to recognise different types of Singaporean food. The overall accuracy was between 0.75 and 0.80 over 50 epochs.

The approach taken was to use transfer learning (using InceptionV3) to train 16000+ different images across 17 classes of food types.


Two observations are that the model does not differentiate well between roast\_chicken\_rice and white\_chicken\_rice well and between char\_kway\_teow and mee\_goreng.

roast\_chicken\_rice vs white\_chicken\_rice

- the issue here is the lack of good images for roast\_chicken\_rice because the main differentiating feature is the texture of the skin and this would require higher resolution pictures for the CNN to differentiate.

char\_kway\_teow vs mee\_goreng

- the issue here is that both dishes have the thick noodles as its base and both are fried (dry with oily texture). In addition the ingredients are also similar (bean sprouts, vegetables and the occassional egg). I was expecting the CNN to differentiate the colour of the dishes. I believe better higher resolution images would allow the CNN to be better at differentiating between these two



This code is written using TensorFlow 1.3, Keras 2.0.8 and Python 3.6