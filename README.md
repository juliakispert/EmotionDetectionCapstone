# EmotionDetectionCapstone

## About 

#### Research question

Question: Can we make an unbiased emotion recognition tool?

Our project attempts to use existing facial recognition software for the implementation of a comprehensive emotional recognition system that accurately identifies emotions in a diverse population using. primarily use Google Collab and Tensorflow to build our program. This is an exciting opportunity to explore the more human elements of a highly technical process. The challenge of developing a program that can attempt to understand a piece of the intricacies of human emotion is both new and important to us.

#### Goal 
our goal for a minimum viable product was a locally run program that can identify at least one emotion: happiness. Given the project's time constraints, we planned to prioritize the accuracy and cultural sensitivity of the identification over the volume of emotions the program can identify. To demonstrate our findings, we created a report which outlines the way displaying emotions differs throughout people, our processes, and our results.


## Training 

#### FairFace Database
The most clear way to mitigate bias in machine learning is to train an algorithm with a dataset that is representative of the program’s intended users. In the case of this program, the entire world of emotion-expressing humans is the target user base, so a dataset with numerical proof of diverse and comprehensive data was a vital resource in accomplishing the main goal of this project. The constraints of time, finances, and the general accessibility of appropriately formatted images led to the conclusion that a pre-existing dataset was the most appropriate choice for training the program. 

We decided to use the FairFace public face image dataset. Created by UCLA researchers Kimmo Kärkkäinen and Jungseock Joo, FairFace specifically attempts to address the strong bias towards Caucasian faces in face image datasets. It contains 108,501 images with 7 defined race groups—White, Black, Indian, East Asian, Southeast Asian, Middle Eastern, and Latino—as well as labels for gender and age. 

#### Tagging 

Tags had to be added manually by the group members. We loaded the tagging data, accessed from the GitHub account of the database creators, into a Google Sheets document and added an additional column labeled “emotion.” The 86744 tagged photos were then divided evenly amongst the four team members to be identified and tagged using each individual’s best understanding of what physical happiness looks like. 
We knew that by manually tagging using our own perceptions of happiness a new set of factors needed to be considered to build a bias-conscious model so we took several steps to limit the harmful effects of these factors. 
	Because it is impossible to have any certainty what the individual subjects in the dataset were feeling at the time that their photo was taken, the first step of our process was to define what happiness looks like as a group before the actual tagging began. There were many photos in the dataset that could be described as emotionally ambiguous. It was difficult to determine if a person is truly happy or if their facial expression is a forced smile based on context. We also had trouble deciding if we would qualify the emotion “content” or rather “not not happy” as happiness. Our group collectively decided that, in the case of ambiguous photos, we would prioritize the presence of a smile or upturn of lips. When the process of labeling began, each group member tagged 1,000 photos at a time and then took a break to limit brain tiredness when tagging photos. This choice was made because exhaustion could lead to mis-tagging. 
After taking all of these potential shortcomings of our process into consideration, we concluded it is only a justifiable claim that our program can only be said to identify human emotions as accurately as the average of the group that created it, and that our program is built to identify external displays of happiness rather than the internal feeling of happiness. 

## Results

Our training ended successfully. Our network's accuracy is generally learning (ending around 86% accuracy), and loss is generally decreasing. We see a pattern of validation accuracy increasing in parallel to testing accuracy. At some points the validation accuracy is higher than testing accuracy, which could be contributed to the randomness. We also see the blue and orange line following similar paths. Though not perfect, it seems our network may flatten out at about a loss of 0.34, accuracy of 0.86, and  generally succeeds at this task. 
	We chose a categorical cross entropy loss model to display this information because we had two labeled classes (happy and not happy).
	We also chose to use the Adam optimizer. The Adam optimizer works well in deep learning practice and very efficiently on problems containing a large volume of data while using less memory than a traditional gradient descent. 

## Conclusion 

Considering the limitations we have seen, our data set is not perfectly diverse. Our data set faces limitations of bias, from developers self tagging as well as from the original data set. Though FairFace is viewed as a much improved diverse set to create facial recognition tools, it is not perfect, and emphasizes the need of growth. There must be more diverse data sets in the world. To create tools that accurately identify faces and emotions, with deep learning, data sets used must represent as many people as possible. However, a data set can not be so large to contain every different face in the world. Sacrifices must be made, but at the bare minimum should attempt to contain balanced distributions of race, gender, and age. 

We also like to bring attention to our own bias being inputted on what makes someone look happy or not. Despite taking precautions, and researching how to identify if someone is happy or not our bias ultimately still is present when tagging. To work around this, future work can involve a study where researchers take a photo of someone while also measuring their heart rate when showing stimuli and asking how they feel. Further using this method researchers could figure out if someone is happy on quantitative measurements, rather than their opinion. Basing off measurements rather than opinion will reduce the risk of bias. Another option would be to accept data by having many humans filling out captchas. The same picture can be sent to many people filling a captcha and for training we would include the average score of the people who chose it. 

Though we created an AI that works for the majority of our test data, more testing needs to be done, and we would like to create an emotion recognition tool that is much closer to being 100% accurate. To do this we can build upon our data set making it more extensive, and find a more precise way to identify happiness for faces that are more ambiguous of their emotion. Our first future goal is to improve accuracy. Other future goals include having our software identify emotions live, creating an user interface that people can use on a mobile app or online, and identifying multiple emotions. 


