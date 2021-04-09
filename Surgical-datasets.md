# Public datasets about surgical vision

## Recent active challenges
* **[MICCAI21](https://endovis.grand-challenge.org/)**  
HeiSurf: HeiChole Surgical Workflow Analysis and Full Scene Segmentation  
GIANA: Gastrointestinal ImAge NAlysis  
CholecTriplet2021: Surgical Action Triplet Recognition  
FetReg: Placental Vessel Segmentation and Registration in Fetoscopy  
PETRAW: PEg TRAnsfer Workflow recognition by different modalities  
SimSurgSkill: Objective Surgical Skill Assessment in VR Simulation  


## Workflow Recognition (artificial surgery; phase or tool recognition)
* **[MISAW], 2020 MICCAI challenge** 
  ```
  MIcro-Surgical Anastomose Workflow recognition on training sessions (MISAW)
  multi-modal, including video and kinematic
  ```
* **[Cholec80](http://camma.u-strasbg.fr/datasets), 2017 TMI** :star::star::star::star::star:
  ```
  Task: phase and tool recognition
  80 videos of cholecystectomy surgeries (40 train/ 40 test)
  25fps phase annotation & 7 classes; 1fps tool & 7 classes
  ```
* **[M2CAI-phase](http://camma.u-strasbg.fr/m2cai2016/), 2016 MICCAI challenge** :star::star::star::star::star:
  ```
  Task: phase recognition
  41 videos of cholecystectomy surgeries (27 train/ 14 test)
  25fps phase annotation & 8 classes
  ```
* **[M2CAI-tool](http://camma.u-strasbg.fr/m2cai2016/), 2016 MICCAI challenge** :star::star::star:
  ```
  Task: tool recognition
  15 videos of cholecystectomy surgeries (10 train/ 5 test)
  25fps tool annotation & 7 classes
  ```
* **[M2CAI-tool-location](http://ai.stanford.edu/~syyeung/tooldetection.html), 2018 WACV** :star::star::star::star:
  ```
  Task: tool recognition and bounding box detection
  2532 frames across the first 10 videos in the m2cai16-tool dataset
  no obvious temporal information
  ```
* **[Cataract-101](https://zenodo.org/record/1220951#.XRHrC_kzaos), [2018 paper](http://www.itec.aau.at/~mt/wp/wp-content/uploads/2018/04/cat101-mmsys-2018.pdf)** :star::star::star::star:
  ```
  Task: phase recognition
  Data:101 videos recording cataract surgery;
  totally 14 hours, 2 minutes, and 5 seconds duration
  10 classes for phase
  ```
* **[CATARACTS'18](https://cataracts2018.grand-challenge.org/home/), 2018 MICCAI challenge** :star::star::star::star:
  ```
  Task: tool recognition
  Data: two synchronized videos (microscopic videos& video showing surgical tray (手术台))
  2*50 videos, (2*25 train/ 2*25 test)
  Note: test GT not available
  ```
  
## Workflow Recognition (robotic-assisted surgery; phase or gesture recognition, tool detection)
* **[JIGSAW](https://cirl.lcsr.jhu.edu/research/hmm/datasets/jigsaws_release/), 2014 JHU&Intuitive surgical** :star::star::star::star::star:
  ```
  Task: gesture recognition; skill assessment
  ex-vivo robotic data; 3 tasks (39+36+28 short videos); synchronized 19 kinematic variables for each frame
  15 classes for gesture recognition; 6-class rating for skill assessment

  ```
  
* **[Nephrec9](https://zenodo.org/record/1066831#.XRQx9Pkzaot), 2018 IJCARS** :star::star::star::star:
  ```
  Task: main for phase recognition; but have various annotations(phase;action;step;tool)
  9 full videos of Robot-Assisted Partial Nephrectomy (RAPN) surgery 肾脏切除, extract to 1262 videos*~30s
  10 classes for phase recognition
  ```
* **[ATLAS](https://www.roswellpark.org/education/atlas-program/research-development/dione-dataset), [2017 TMI](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7847313)** :star::star::star::star:
  ```
  Task: tool bounding box detection and location
  Data: ex-vivo 仿真手术或者robot直接抓取object; 86 full subject study videos (910 action clips of ten surgeons using davinci robot)
  Label: tool bounding box and video-level task annotations
  ```
* **[DESK](https://github.com/nmadapan/Forward_Project), [2019 IROS](https://arxiv.org/abs/1903.00959)** :star::star::star::star:
  ```
  Task: DA!!!, phase recognition
  Data: RGB images, depth and kinematic information for the peg transfer task; 
  stereoscopic images for simulated robot and depth data for real robots; 
  multiple domains including two real robots and a simulation environment
  Label: 7 surgemes/phases
  ```
  
## Instrument/tool Segmentation
* **[MICCAI15](https://endovissub-instrument.grand-challenge.org/), 2015 MICCAI challenge** :star::star::star::star::star:
  ```
  Task: Instrument part segmentation and tracking; robotic
  Data:
  1.Rigid segmentation: ~160 images from 4 procedures train/ 10*4+50*2 test (没有时间信息，都是单张图片)
  2.Rigid tracking: 45s*4 / 60s*2  (1&2都是in-vivo) （图片是序列形式，但是给的label都是不连续的，4500 images / 180 labels）
  3.Robotic segmentation: 45s*4 videos/ 15s*4 videos+ 60s* 2
  4.Robotic tracking: 45s*4 videos/ 15s*4 videos+ 60s* 2 (3&4 ex-vivo) (是视频，但是label是position这类的数字，不是segmentation mask)
  Note: exvivo data, relatively simple
  ```
  New: Add [pose estimation](https://github.com/surgical-vision/EndoVisPoseAnnotation) annotations into this dataset
  
* **[MICCAI17](https://endovissub2017-roboticinstrumentsegmentation.grand-challenge.org/Home/), 2017 MICCAI challenge** :star::star::star::star::star:
  ```
  Task: Instrument segmentation (binary, part, type); robotic
  Data: 8x 225-frame in-vivo sequences train/ 8*75+2*300 test; robotic-assisted surgery
  ```
* **[MICCAI19](https://www.synapse.org/#!Synapse:syn18779624/wiki/), 2019 MICCAI challenge, [challenge paper](https://arxiv.org/abs/2003.10299), [data paper](https://arxiv.org/abs/2005.03501)** :star::star::star::star::star:
  ```
  Task: Instrument segmentation (binary, type); artificial
  Data: laparoscopic video data; 
  A training case encompasses a 10 second video snippet in form of 250 endoscopic image frames and a reference annotation for the last frame;
  The test cases are identical in format but do not include a reference annotation.
  ```
  
* **[TMI17](https://medicis.univ-rennes1.fr/software)** :star::star::star::star::star:
  ```
  Task: tool bounding box detection and location; 能近似于segmentation
  Data: 14 monocular sequences with total 2476 frames;
  brain and spine tumour removal process
  Label: tool bounding box and class label: 7 classes; isosceles triangle labels (semantic label)
  ```
  
* **[MICCAI19](http://opencas.dkfz.de/image2image/), 2019 MICCAI paper** :star::star::star::star::star:
  ```
  Task: DA!!!, instrument segmentation
  Data: 合成图转real图，有cholec80 dataset对应的mask GT，但是就是单张图，没有时间信息
  Label: mask; depth; normal…..蛮多基于合成图的信息
  ```
* **[SurgVisDom],2020 MICCAI challenge**

* **[NeuroID](http://openaccess.thecvf.com/content_CVPRW_2019/papers/WiCV/Kalavakonda_Autonomous_Neurosurgical_Instrument_Segmentation_Using_End-To-End_Learning_CVPRW_2019_paper.pdf), 2019 CVPR workshop paper** :star::star::star:
  ```
  Task: instrument segmentation
  Data: 2400 images
  Label: 8 classes of instruments labeled
  Note: has data link in paper, however cannot open; need to ask
  ```
* **[UCL](https://arxiv.org/pdf/2007.09107.pdf)**

## Scene Segmentation
* **[MICCAI18](https://endovissub2018-roboticscenesegmentation.grand-challenge.org/Home/), 2018 MICCAI challenge** :star::star::star::star::star:
  ```
  Task: entire scene segmentation
  Data: 16*149 train, 2*500 test
  Label: pixel wise scene label
  ```
* **[CaDIS],MICCAI 2020 challenge**

  
## Other useful websites for surgical datasets
* http://opencas.webarchiv.kit.edu/
* http://nearlab.polimi.it/medical/dataset/
* Hamlyn Centre：http://hamlyn.doc.ic.ac.uk/vision/
  

  
  
