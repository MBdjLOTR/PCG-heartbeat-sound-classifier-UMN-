Heart Sound Segmentation and Classification

A machine learning system for accurate segmentation and classification of fundamental heart sounds (S1 "lub" and S2 "dub") in phonocardiogram (PCG) recordings.

🎯 Overview: 
This project addresses the critical challenge of automated cardiac auscultation analysis by developing robust methods to locate and classify S1 and S2 heart sounds within PCG recordings. The system leverages both supervised and semi-supervised learning approaches to enable accurate segmentation of normal heart sound audio files from labeled and unlabeled datasets.

🔬 Research Objective:
The primary goal is to develop a robust method for:

Accurate segmentation of S1 ("lub") and S2 ("dub") heart sounds
Precise classification of fundamental heart sound components
Automated analysis of cardiac auscultation data
Location identification of S1 and S2 sounds within PCG recordings (measured in audio samples)

📊 Dataset
CirCor DigiScope Phonocardiogram Dataset
Dataset Statistics:

Total recordings: 5,272 heart sound recordings

Subjects: 1,568 subjects aged 0-21 years

Age distribution: Mean ± STD = 6.1 ± 4.3 years

Recording duration: 4.8 to 80.4 seconds (Mean ± STD = 22.9 ± 7.4 s)

Total duration: >33.5 hours of recording

Auscultation locations: 4 main cardiac auscultation sites per subject

Data Structure

Each subject has four types of data files:
1. Audio Files (.wav)

Binary wave recording files per auscultation location
Contains raw heart sound data
Standard audio format for signal processing

2. Header Files (.hea)

Text files describing the corresponding .wav file
Follows standard WFDB (WaveForm DataBase) format
Contains metadata and recording parameters

3. Segmentation Files (.tsv)

Tab-separated values format
Contains segmentation annotations for S1 and S2 locations
Provides start and end points of fundamental heart sounds
Generated using semi-supervised voting scheme from three state-of-the-art algorithms

4. Subject Description Files (.txt)

Subject ID corresponds to filename
Demographic information:

Weight and height
Sex and age group
Pregnancy status


Detailed murmur event descriptions
Clinical annotations by human experts

First we perform segmentation and classification of heartbeat sounds in a single audio sample, an AV audio file indicating that the heartbeat sound is recorded from the aortic valve.
