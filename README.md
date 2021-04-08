# Pedestrian_Distance_Classifier
For our Product ‘IntelliPick’ we have developed an application that is capable of identifying and measuring the distance between any two number of people.The application is supported by The TensorFlow Object Detection API which is the framework for creating a deep learning network that solves object detection problems. It contains some pre-trained models trained on different datasets which can be used for inference.

The current application can be used for transfer learning that helps us to customize the software to serve our needs .In our case we use it identify shortest distance between the firefighter and the people trapped to help reach them on time.
The common intuition behind transfer learning for image classification is that if a model is trained on a large and general enough dataset, this model will effectively serve as a generic model of the visual world. We can then take advantage of these learned feature maps without having to start from scratch by training a large model on a large dataset.
In this case, we did not need to apply transfer learning since we want to identify people, and there are already some models trained to inference this. We have used the model ssd_mobilenet_v2_coco_2018_03_29 which has been trained on these objects.

Based on these trained models ,edge contours had already been trained enough to identify any person in the frame.Based on these pre-trained calculations ,whenever a  person enters into the frame ,his/her outline will be marked and a rectangle outline will cover the human and distance between two such humans will be compared based on the distance between the edges and centroid of the rectangle.For a video ,a frame of the video will be taken and the distance will be calculated and the process will continue until every frame of the video is exhausted.

Sample:
![image34](https://user-images.githubusercontent.com/58656351/113976438-c8e91b80-985e-11eb-8769-85b7893c2c9f.jpg)
![image34_p](https://user-images.githubusercontent.com/58656351/113976457-d0102980-985e-11eb-880e-3e1373b9c83c.jpg)
