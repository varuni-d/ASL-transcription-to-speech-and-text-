# ASL-transcription-to-speech-and-text

In this project, the WLASL dataset was utilized [1]. This dataset is the largest dataset publicly available containing over 2,000 commonly used ASL words. Upon downloading the dataset, it was categorized into separate folders by label. 

Subsequently, Mediapipe was used for further preprocessing [2]. The detailed steps are as follows:

1) Install Mediapipe and change source files to read videos from saved input, and not in realtime, as outlined in [2].
2) In the Mediapipe source directory, execute 'python build.py --input_data_path=[INPUT_PATH] --output_data_path=[OUTPUT_PATH]'
eg: $ python build.py --input_data_path=/Users/varuni/Desktop/signculate/mediapipe/inputvideos/ --output_data_path=/Users/varuni/Desktop/signculate/mediapipe/output/
Note: inputvideos directory contains the labeled input videos, while output directory is empty
3) Run 'python train.py --input_train_path=[INPUT_TRAIN_PATH]'
eg: $ python3 train.py --input_train_path=output2/Relative/
Note: Might have to make the files executable and add '#!/usr/bin/env python' to the script



References:

[1] https://dxli94.github.io/WLASL/
[2] https://github.com/rabBit64/Sign-language-recognition-with-RNN-and-Mediapipe
