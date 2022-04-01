# Image Face Clustering

cluster face images with and without **CNN**. I did some result analysis on the nootbook with visual diagrams and logs.

## Without CNN

On this approach I did not use any vision model architectures, I just extracted **Pixels** as features and transformed it from 3-dimensional to 2-dimensional.

## With CNN

On this approach I used any vision model architectures **VGG15**. It is considered to be one of the excellent vision model architecture till date. 

Most unique thing about VGG16 is that instead of having a large number of hyper-parameter they focused on having convolution layers of 3x3 filter with a stride 1 and always used same padding and maxpool layer of 2x2 filter of stride 2. It follows this arrangement of convolution and max pool layers consistently throughout the whole architecture. 

In the end it has 2 FC(fully connected layers) followed by a softmax for output. The 16 in VGG16 refers to it has 16 layers that have weights. This network is a pretty large network and it has about 138 million (approx) parameters.

## Supported Cluster Algorithm

- [x] Kmeans
- [x] DBScan
- [x] Agglomerative (ward, complete, single, average)
- [x] Documented
- [x] Visual Analysis

## Kmeans

Kmeans and MiniBatchKMeans used and the results were compared.


## DBScan

DBScan were used with epsilon estimator which use **NearestNeighbour** to evaluate best epsilon. Also the effect of min samples on the amount of noisy detected datas were measured.

## Agglomerative  

Four types ward, complete, single and average were used. Also the best threshold was measured and the differences of 4 types were analysed.
