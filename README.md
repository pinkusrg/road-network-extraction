
# Road Network Extraction

#### INTRODUCTION
The main purpose of this project is to extract roads from Aerial images and help in better navigation of roads using GPS and also in construction of blocks or bridges by analyzing the extracted road networks. This is mainly helpful in India as because due to the road conditions of India , developing an automated driver guidance system is very important. It is a very important research field in image processing as although road segments appear to have very elongated shapes as compared to buildings but detecting them is very difficult as due to the noise and there may be same shapes but may not be the road object.

## Table of contents  
1. [PROPOSED WORK](#PROPOSED-WORK)  
2. [Steps](#Steps)  
	2.1. [Greyscale Image Conversion](#Greyscale-Image-Conversion)<br>
	2.2. [Thresholding after Greyscale conversion](#Thresholding-after-Greyscale-conversion)<br>
	2.3. [Density Based Clustering after thresholding](#Density-Based-Clustering-after-thresholding.)<br>
	2.4. [Extracting Road Clusters](#Extracting-Road-Clusters)<br>
3. [Comparison with some of the proposed methods ](#Comparison-with-some-of-the-proposed-methods )<br>
4. [Conclusion](#Conclusion)
5. [Future Work](#Future-Work)
6. [References](#References)
7. [Contributors](#Contributors)
  
##### Sample Examples processed with the proposed algoithm :
Sample 1 :<br>
![Processed Image 1](https://springflee.files.wordpress.com/2020/02/d1.png)

Sample 2:<br>
![Processed Image 2](https://springflee.files.wordpress.com/2020/02/d2.png)
#### PROPOSED WORK
Our proposed system consists of three stages. Firstly pre-processing of image is done.The image is converted into grayscale image and thresholding is applied to segment the darker and lighter regions of the image. Secondly clustering is applied using density based which then clusters the image into different objects. Thirdly post-processing is done in which we apply Thining algorithm to reduce foregrounds and preserving the extent and connectivity of the regions. After thining is applied Curve  Fitting is done to joint the broken roads followed by finding the elongated path which will produce the desired result. 

![flowchart of the proposed](https://springflee.files.wordpress.com/2020/02/image-000.jpg)
<br>
#### Steps
#### 1. Greyscale Image Conversion
Image is first converted into greyscale.<br>
![Black and White Converted](https://springflee.files.wordpress.com/2020/02/yellowroad.png)
#### 2. Thresholding
Greyscale Image obtained is thresholded with a certain value.<br>
![Thresholding from greyscale image.](https://springflee.files.wordpress.com/2020/02/image-004.png)
#### 3. Density Based Clustering after thresholding.
After thresholding, the image is clustered based on its density.
Here below, yellow boxes are showing the road clusters and red boxes are showing the non-road clusters.<br>
![Clustered into different labels](https://springflee.files.wordpress.com/2020/02/image-030.png)
#### 4. Extracting Road Clusters
The elongated clusters are then extracted.
Below yellow pixels are the road clusters shown yellow in colour.<br>
![Road Clusters shown in yellow colour](https://springflee.files.wordpress.com/2020/02/yellowroad.png)

### Comparison with some of the proposed methods :
#### 1.  
![enter image description here](https://springflee.files.wordpress.com/2020/02/c1.png)
K-Means Clustering and Morphological Operations used by Rohit Maurya, Dr. Shalini Singh, Dr. P.R Gupta, Manish Kumar Sharma [1]. In our proposed method some extra paths were detected whose curve matched with the road ones and also the color was similar to the roads.
#### 2. ![enter image description here](https://springflee.files.wordpress.com/2020/02/c2.png) 
Adaptive Global Thresholding and Morphological Operations used by Pankaj Pratap Singh & R. D. Garg[3]. The results are almost same because we also applied the global thresholding at the beginning which filtered out most of the parts but thresholding also removes some of the regions which are actually road so an optimal amount of threshold value should be considered.
#### 3.
![enter image description here](https://springflee.files.wordpress.com/2020/02/c3.png)
Classification region from SVM by Mingjun Song and Daniel Civco[2]. White areas representing the roads group features and black areas representing nonroad features and in the proposed output the same is represented with the yellow areas. They also suggested to address the development of algorithms or heuristics to fill in road gaps caused by shadow or obscuring land features.
#### Conclusion
The proposed method of road extraction uses preprocessing of the image at the first stage where adaptive thresholding is performed after bicolor transformation, which is based on threshold limit and pixel intensity values followed by clustering to extract the road clusters which are elongated in shape from aerial images. The proposed method is tested on high resolution aerial images. Experimental results indicate possible use of algorithm in extracting the road network in a reliable manner. In some cases, small part of barren land and parking area is classified as roads. The approach is based on the pixel intensity values, which induces the detection of some unwanted objects. To get the final network thinning is applied followed by curve fitting.
#### Future Work
So far we have performed up to thinning operation and curve fitting is to be applied which will be the final output of the road. After Thinning is done Curve Fitting is applied to join the broken lines or broken curves in the pre-processing of the image and clustering.
#### References 
Works Cited: 
- [1] Rohit Maurya, Dr. Shalini Singh, Dr. P.R Gupta, Manish Kumar Sharma - “Road Extraction Using K-Means Clustering and Morphological Operations”. 
- [2] Mingjun Song and Daniel Civco[2] – “Road Extraction Using SVM and Image Segmentation”. 
- [3] Pankaj Pratap Singh & R. D. Garg – “Automatic Road Extraction from High Resolution Satellite Image using Adaptive Global Thresholding and Morphological Operations”. 
- [4] Chunsun Zhang, Shunji Murai, Emmanuel Baltsavias – “Road Network Detection by Mathematical Morphology”. 
- [5] Delio Vicini, Matej Hamas and Taivo Pungas – “ Road Extraction from Aerial Images”. 
- [6] M. Mokhtarzade, M. J. Valadan Zoej, H. Ebadi – “Automatic road extraction from high resolution satellite images using neural networks, texture analysis, fuzzy clustering and genetic algorithms”. 
- [7] Şafak Altay Açar, Şafak Bayır – “Road Detection Using Classification Algorithms”. 
- [8] M. Mokhtarzade, M. J. Valadan Zoej[8] – “Road Extraction using artificial neural networks”. 
- [9] Weixing Wang , Nan Yang , Yi Zhang, Fengping Wang , Ting Cao, Patrik Eklund - “A review of road extraction from remote sensing images”. 
- [10] Qixiang Ye, Wen Gao, Wei Zeng- “Color Image Segmentation using Density-Based Clustering”.
#### Contributors 
- Pinku Swargiary
- Sanjib Saikia
- Malong Engti
- Sibangkar Basumatary
- Indro Tokbi
- Dipankar Das
 - Nilim Kramsa
