# convert_videolabels_to_NNinput
convert video labels from vatic.js to input for openpose or deeplabcut

## About this repo

- Go from video data to neural network inputs (images and keypoint labels) for pose estimation packages for [transfer learning with openpose](https://github.com/cchamber/openpose_keras) or [Deeplabcut](https://github.com/AlexEMG/DeepLabCut)

### Steps

- Upload video to [vatic.js](https://github.com/dbolkensteyn/vatic.js). Code can be run locally or [here](https://dbolkensteyn.github.io/vatic.js/). Video example files in ./files/video. 
- Label video, including bounding box around the figure. Can upload example frame zip file in ./files/frame_zip and xml file in ./files/xml to see labels
- Download output files. Vatic produces a zip file containing frames from the video and an xml file containing the labels. Unzip frame zip file. Examples in ./files/xml and ./files/image  
- To get openpose .json file and resized images, run notebook `xml_to_openposeNNinput.ipynb`. Change notebook for use case.
- To get deeplabcut pandas dataframe and resized images, run notebook `xml_to_DLCNNinput.ipynb`. Change notebook for use case.
