# yoga

#Yoga-117 Dataset

"Yoga-117" is a large-scale dataset for yoga poses analysis which is introduced in our paper.

###Structures of the dataset
"Yoga-117" dataset contains 16,680 samples of yoga poses which includes 3 different modalities of data for each sample:
*RGB images
*Depth images
*3D skeleton data

Images have been cautured by two  synchronized Microsoft Azure Kinect cameras.
The acquisition frame rate was 30fps, and the image resolution was 1280 × 720. 3D skeletal data contains the 3D locations of 32 major body joints at each frame.

The storage structure of the dataset is as follow:
poses capturing site(field 1 or field 2) --- camera viewpoint（master(front view) or sub(side view)）--- different subjects（subjects' number as 129 ,etc.）--- 10 classes of first level --- corresponding classes of second-level( specific poses) ---  data in 3 different modalities of the pose

Each name of the  manually labeled skeleton data is in the format of 
(e.g. MASTER_2_action_3_timestamp_1609222772783_asso_1526.csv) in which the "timetamp_xxxxxxxxxxxxx" is the timetamp of the image and the "action_x" is the the pose second class label.

###Poses classes
The 10 first level classes are:
* I. dynamic pose
* II. sitting
* III. inversion
* IV. standing
* V. revolve
* VI. prone pose
* VII. support
* VIII. balance
* IX. bending
* X. kneeling
The specific second level classes are shown in the "Poses classification index.pdf"

###Skeleton data
The skeleton data have saved as .csv files include Tick, PersonId, JointId, depth data of each joint (xyz_x, xyz_y, xyz_z), quaternions of each joint(wxyz_w, wxyz_x, wxyz_y, wxyz_z) and confidence.
