# Window-based vehicle detetion algorithm

This repository contains the source code for window-based vehicle detection algorithms using HOG feature. This python implementation was conducted as a final project in introduction to computer vision lecture at SNU. Specific details are explained as comment in the notebook file

### Vehicle detection using linear SVM and HOG feature
<p align="center">
<img src="https://user-images.githubusercontent.com/86834176/193737319-c47ff600-24c4-4128-bd53-07244e4eef64.png" width="400">
</p>

With the average precision of 31.03%, sample detection results are visualized in the picture above. Though training time was short, detection capability was seriously lacking. 

### Vehicle detection using cascade architecture of linear SVM with HOG feature
<p align="center">
<img src="https://user-images.githubusercontent.com/86834176/193737664-6930f474-6c74-48e5-b670-f8ef33a10a8b.png" width="400">
</p>

With the average precision of 48.77%, sample detection results are visualized in the picture above. The cascade architecture followed the details of [Fast Human Detection Using a Cascade of Histograms of Oriented Gradients](https://ieeexplore.ieee.org/document/1640933). With such architecture, average precision increased and false positive rate decreased clearly when compared to using single linear SVM. Training took 2~3 days using CPU. 


### Improved algorithm
<p align="center">
<img src="https://user-images.githubusercontent.com/86834176/193737673-45269987-7f77-418e-aa5b-10a20858def8.png" width="400">
</p>

With the average precision of 83.26%, sample detection results are visualized in the picture above. To improve the detection capability, linear SVM was replaced with Gaussial kernel tricked SVM. Furthermore, flattened rgb color histogram and local binary pattern were concatenated to flattened HOG feature to flourish the training information. This modification allowed for a noticeable improvement in detection rate, training speed, and detection speed.

<p align="center">
<img src="https://user-images.githubusercontent.com/86834176/193737676-78b2d6a0-c14f-4275-86e1-7cc4d49b9056.png" width=700">
</p>
