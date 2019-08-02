# FaceNetTraining
FaceNet training using colab
## Inspiration
The code is heavily inspired by the [Face Recognition using Tensorflow](https://github.com/davidsandberg/facenet#inspiration) implementation.

## Steps
### Step 1 download [VGG Face2](http://zeus.robots.ox.ac.uk/vgg_face2/) using colab
Just !wget http://balabala.tar.gz directly won't work, because it is also required a lot request headers to be sent to the server to get the real dataset file. Try to "inspect" the "http://zeus.robots.ox.ac.uk/vgg_face2/" website page, click the "download link" to check the file "get_file?fname=vggface2_train.tar.gz"'s header, now, check the request header's content, then you can download the dataset with either:
!wget --header='key1: value1' --header='key2: value2' ... http://zeus.robots.ox.ac.uk/vgg_face2/get_file?fname=vggface2_train.tar.gz
or write a python script with import requests but this method is too much memory cost.

Total training dataset is about 36G, downloading which may take several minutes.

### Step 2 decompression
7z e ~/vggface2_train.tar.gz
tar –xvf vggface2_train.tar
