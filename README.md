# TensorFlow_Service
Set up web service in TensorFlow
https://www.tensorflow.org/serving/serving_basic

## Server:
1. use saved_model_builder to save model
2. Install tensorflow-serving-api:
```
pip install tensorflow-serving-api
```
3. saved model to /tmp/mnist_model
```
python tensorflow_serving/example/mnist_saved_model.py /tmp/mnist_model
```
4. load model using tensorflow_model_server:
* Add TensorFlow Serving distribution URI as a package source (one time setup)
```
echo "deb [arch=amd64] http://storage.googleapis.com/tensorflow-serving-apt stable tensorflow-model-server tensorflow-model-server-universal" | sudo tee /etc/apt/sources.list.d/tensorflow-serving.list
```
* Install and update TensorFlow ModelServer
```
curl https://storage.googleapis.com/tensorflow-serving-apt/tensorflow-serving.release.pub.gpg | sudo apt-key add -
```
