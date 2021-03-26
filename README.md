# access-classifier

Preprocessing and modeling scripts for Carleton University DATA 500 course project. Project objectives are to develop a CNN classifer for predicting whether an image is "accessible" or "inaccessible".

In 2019, the federal government initiated Accessibility Standards Canada to prioritize a barrier free Canada by 2040, however, there are data gaps on the infrastructure [1] that make the built-environment inaccessible for the 9.6% of people (over 15 years-old) who have mobility disabilities in Canada [2]. Thus, this project leverages open source crowdsourced street-level images and convolutional neural networks (CNNs) to test a hybridized approach for classifying whether a building’s entrance is accessible or not. Since identifying the various barriers that impeded those who face a diversity of mobility restrictions is complex, this research seeks to support a small piece of this puzzle, defining “accessible” building entrances as building doors that are connected to an accessible exterior pathway [3]. Therefore, we seek to answer: Can CNNs trained on open source imagery, from Ottawa, Ontario, Canada, yield accurate results when applied to classify the accessibility of building entrances broadly?

Based on local knowledge and OpenStreetMap building footprint geometries, images capturing buildings at varying angles were compiled for Ottawa by leveraging the Mapillary API [4] with Python scripts. The dataset has been reduced to 843 after manually annotating and grouping the images to 421 as “accessible” and 422 as “inaccessible”. Annotation followed the United Nations principles of accessible design, but collaborating with individuals with lived experiences would have enriched the dataset. Following methods by Wu et al (2019) [5], 85% of images will be used for training and 15% for testing. Further, with Keras, their model architecture will be applied as a starting point, in which hyperparameters will be iteratively evaluated to optimize the model.

This project will contribute to the exploration of using open source data and CNNs as a means to streamline and hybridize current approaches for collecting information on infrastructure barriers for policy-making and inclusive wayfinding. For example, this model could be integrated within autonomous feature extraction systems for collecting data on infrastructure barriers of the built-environment. Further, an optimized version of this model could be a component for autonomous vehicles’ navigation systems.

- [1] Angus Reid Institute. 2015. Disability and Accessibility: Canadians see significant room for improvement in communities where they live. https://angusreid.org/rhf-accessibility/.
- [2] Statistics Canada’s 2017 Survey on Disability. https://www150.statcan.gc.ca/n1/pub/11-627-m/11-627-m2020085-eng.htm
- [3] United Nations. 2003. Accessibility for the Disabled - A Design Manual for a Barrier Free Environment. https://www.un.org/esa/socdev/enable/designm/AD2-06.htm.
- [4] Mapillary is an open source repository of crowdsourced street-level images available under the CC BY-SA 4.0
- [5] Wu, J., Hu, W., Coelho, J., Nitu, P., Paul, H., Madiraju, P., Smith, R., & Ahamed, S.I. (2019). Identifying Buildings with Ramp Entrances Using Convolutional Neural Networks. 2019 IEEE 43rd Annual Computer Software and Applications Conference (COMPSAC), 2, 74-79. doi:10.1109/COMPSAC.2019.10186.
