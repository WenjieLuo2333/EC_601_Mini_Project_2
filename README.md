# EC_601_Mini_Project_2<br/>
This Project was build on Keras(Anaconda tensorflow-gpu backend) and used to make a classification between cats and dogs.<br/>
### Referece<br/>
For the standard resnet-34 network. I Use ResNet Module from: https://github.com/raghakot/keras-resnet/blob/master/resnet.py

### DataSet
There're about 25000 images in the [dataset](https://www.kaggle.com/c/dogs-vs-cats/data) provided by Kaggle.<br/>
Due to the limitation of memory and GPU memory, I generate<br/> 
  1.a training set of 8000 images<br/>
  2.a validation set of 2000 images<br/> 
  3.a test set of 10000 images<br/>

All images are resized into 122x122 to for the utilizing of networks.<br/>

### Tutorial<br/>
1.install jupyter notebook and the required libs.``Keras`` ``Tensorflow-gpu`` ``jupyter notebook`` ``Numpy`` ``Pandas``<br/>
2.Download the data set from [here](https://www.kaggle.com/c/dogs-vs-cats/data).<br/>
3.Run ```getdata.ipynb``` in jupyter notebook to generate the data for network(train,val and test).<br/>
4.Run ```class_model.ipynb``` to train and test the model.<br/>

### Train<br/>
Simply run ```class_model.ipynb``` from top to bottom except for 15~19 entries(model=load_model('xxxx.model')).<br/>

### Test<br/>
If you already have a pretrained model. Run from the [15] entries (model=load_model('xxxx.model')), and all the above cells.

### Result<br/>
For the standard ResNet-34 and ResNet-50 network i got an acc at 86%.
For the model build by myself. I write my own residual learning module and use it to build a deep network with shorcut.With a dropout ratio at 0.5 i got an acc at 82%~83%. However,when i set dropout as 0.1, i got an acc at 85.9%,which is similar to standard resnet-34.
The two models are both in entry[11].
The two images are visual structure for two networks.
