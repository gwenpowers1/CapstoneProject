# Capstone Project Proposal
Last updated: November 29, 2023

## Stakeholder Names and Roles
Gwen Powers Team member 

Elisabeth Waldron Team member

Will Sivolella Team member

Dr. Michaela DuBay, UVA STAR Sponsor

Aiying Zhang Mentor

Jessica Zhang Mentor

## Abstract
The project's objective is to uncover distinct patterns of parent-infant interactions within Latinx families, highlighting their cultural uniqueness. It aims to investigate how these interactions influence child language development, especially concerning autism. The ultimate goal is to create tailored early interventions for autism that align with cultural nuances discovered in the study. Specifically, the project will focus on categorizing vocal patterns exhibited by children and parents, aiming to identify markers that could potentially predict a later diagnosis of autism. 
Outline of the Project
The main objective of the project is to classify the portions of the audio files of parent-child interactions that are infants speaking versus adults speaking. The results of the project will be used by our sponsor to investigate and understand parent-infant interactions in Latinx families . These interactions will further be applied in the context of autism, to support the development of culturally relevant early autism interventions. Thus, the results of the project will lead to the enhancement of our understanding of developmental vocal interaction patterns as well as future contributions to the development of autism intervention strategies within Latinx populations. The stakeholders are Autistic/Latinx infants, families, and researchers. Our sponsor notes that the results cannot be directly generalized to or compared with other cultural groups due to the unique nature of our analysis. We are assuming that culturally unique parent-infant interaction patterns have a significant impact on child language development. The scope of the project is the identification and analysis of parent-infant vocal exchanges.

## Success Criteria
SC1: Successfully identify separate instances of parent and child vocalizations

SC2: Successfully identify vocal exchange patterns between these parent and child vocalizations


## Assumptions and Limitations
Assumptions [A] and limitations [L] on the data and the modeling approach. 

L: Ideally, families who set up the videos would have kept them running to ensure more complete data

A: Assume that each data file is accurately labeled with who is present in the file which includes actual interactions with parent-child, background noise, separate conversion, and static. This may help with linear labeling and overall data processing.

## Potential Background Literature and Resources
Using Language ENvironment Analysis to Improve Outcomes for Children Who Are Deaf or Hard of Hearing

Environmental Considerations: Home and School Comparison of Spanish–English Speakers’ Vocalizations

Accuracy of the Language Environment Analyses (LENATM) system for estimating child and adult speech in laboratory settings

Automated Assessment of Child Vocalization Development Using LENA

An Investigation of Language Environment Analysis Measures for Spanish–English Bilingual Preschoolers From Migrant LowSocioeconomic-Status Backgrounds

## Brief Outline of the Data
The raw data comprises approximately 200 hours of audio recordings (5 hours are test data with manually labeled timestamps of when an adult/infant/no one is vocalizing). The Video/audio recordings are from the homes of 32 Latinx families with a child between 6 months and 2 years old who lived within a 2 hours driving distance from Charlottesville, VA (mainly in the Richmond area and southern NOVA). Participants set up cameras to record video and audio of their families’ day to day activities in the home for roughly 2 hours. We also have access to data recording the country of origin for the parents, number of years living in the US, child age, parent age, child/parent gender, level of English proficiency, parent education, and household income. The target variable for the project is the duration and amount of parent-infant vocal exchanges within the data. Potential predictor variables are the frequency of the audio portions as well as the length of audio portions and the timing between audio portions. Data aspects which may present a challenge include any potential unintelligible/missing data resulting from background noise and multiple people speaking at once. 

## Brief Plan of How the Data will be Modeled and Processed
We will need to build a database from the 200 hours of audio files and distinguish between train and testing data. We will need to split up the audio files by silence so we can isolate each part of the interaction. Also, we will need to use software to analyze the frequency of the data, and the length of each data point, and retrieve any other variables we will be interested in.

## Brief Plan of Modeling Approaches
The primary focus of the project is to examine the duration and volume of vocal exchanges and classify audio files between parents and infants within Latinx families. 

In order to train and test on the data provided, we will use jupyter [.ipynb] files on Google Colab to compute the algorithms necessary to classify parent-infant interactions.

Regarding the technical aspect of the project, the audio files will be processed using CNN (Convolutional Neural Network) models. Similar to how images are handled in CNNs, these models will analyze audio inputs for classification purposes. The steps involved will include:

- Convolution: To extract crucial features and understand the spatial relationships within the audio.

- Max-pooling: To reduce dimensionality and focus on essential information.

- Fully connected layers: To create a linear classifier, categorizing the audio data into parent, baby, or non-specific categories.

Moreover, MFCC (Mel-Frequency Cepstral Coefficients), a widely used algorithm for audio recognition, will be employed. The process involves several steps:

- Pre-emphasis: Amplification of higher audio frequencies.
- Framing: Dividing the audio into shorter, overlapping frames.
- Windowing: Reducing spectral leakage.
- FFT (Fast Fourier Transform): Converting time-domain signals into the frequency domain.
- Mel filtering: Applying filters to mimic human speech perception.
- Log compression: Scaling the values logarithmically.
- DCT (Discrete Cosine Transform): Decorrelating features.
- Obtaining MFCC values: Finalizing the feature vectors for classification.

It's important to note that this phase of the project aims solely to classify audio segments as either from a parent, a baby, or not related to parent-infant interactions. This classification serves as a foundational step towards understanding the distinctive vocal patterns between parents and infants within the cultural context of Latinx families.

After building the advanced algorithms necessary to carry out our models, we will use our testing data to assess the accuracy and uncertainty of the model. We will use confusion matrices and prior posterior methods to assess how well the models fit the test data.

## Potential Concerns [C] and Blockers [B]
C: Potentially poor audio quality and background noise could limit the quality or quantity of data.

B: Access to additional data or resources if needed, as we have a set amount of data from this research project.

C: Ethical need to keep data in the cloud/not allowed to download. This likely will require planning and purposeful handling of this personal data throughout the project.

C: Unable to identify who is speaking. We can access additional files that contain actual videos of participants to see if the child is speaking/interacting with the adult. May take siblings' speech into perspective as well.

 
 
