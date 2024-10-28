# Pupil-Reaction-Predictor-in-Cataract-Surgeries
There are more than 2.5 million canadians living with cataracts, but only a small subset receive cataract surgery in a year. 

Cataracts are a painless clouding of the lens in your eye that increasingly blurs your vision over time. Cataracts can only be treated with surgery. The minimally invasive procedure involves removing the cloudy lens and replacing it with an artificial intraocular lens (IOL).

A recent study has reported a 24% increase in demand for ophthalmologists

There are 2 major complications that can occur during Cataract Surgery. 
Firstly, Pupil Contraction: the pupil can unexpectedly reacts to the lighting changes and become quickly contracted which may lead to serious intra-operative implications.

Secondly, the IOL may rotate or dislocate following the surgery. Even slight deviations, or the slight displacement of the IOLs, can result in significant distortions in vision and leave patients dissatisfied.

Thus, the post-operative analysis of cataract surgeries to detect even minor intraoperative deviations that might explain a lack of a post-operative success makes this research topic an increasingly important issue.

Current solutions for managing pupil reactions during cataract surgery include manual observation by skilled surgeons, medications to control pupil size, and some automated measurement systems. While helpful, these methods lack the predictive and real-time analytical capabilities that AI could offer.
Imagine an AI tool that predicts pupil reactions and gives early warnings to the surgeon. This would enable proactive management of complications, leading to more successful surgeries and better patient outcomes.

Our Model:
Identified ideal pretrained model to assist our segmentation tasks (DeepLab V3)


Trained a model to return the area populated by a pupil in cataract surgery images
Learning rate = 0.001
Optimizer = Adam
Batch Size = 10

Conducted research to identify the changes in area sizes consistent with dangerous pupil contractions

Findings:
Data augmentation/pre-processing: intensity normalisation, compressing frame size, frame extraction using decord
Model does a better job in testing data to prevent overfitting
Can effectively identify pupil without interference from other objects in the images
Pupil dilations commonly occur in the videos, but serious contractions are rare - area can decrease by almost 50% during serious contractions
