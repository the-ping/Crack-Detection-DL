# Live-Crack-Detection-using-JetsonNano
- Summer 2019 SMRT project with NTU and NUS engineering students. (project proposal link ref: https://docs.google.com/presentation/d/1YAa_tffII_fIUdK7QxtHg4VfHRmDeVpNaP1xnDjmRvM/edit#slide=id.g5508887eb5_0_95)
- keywords: #real-time, #recognition, #cracks, #TensorflowObjectionDetectionAPI, #ComputerVision, #DeepLearning, #JetsonNano
- project overview: 
    Deploying a robotcar to detect location of cracks in tunnel tracks.  
    
- forked repo: https://github.com/Tony607/object_detection_demo.git
    
------------------------------------------------------------------------------------------------------------------------------------------
## <Custom trained objection detection model>
- What is Tensorflow Object Detection API?: an open source framework that is built on top of Tensorflow, to construct/train/deploy object detection models.

- How to train my own custom object detection model using Tensorflow Object Detection API
    - outline: 
    - source: https://www.dlology.com/blog/how-to-train-an-object-detection-model-easy-for-free/
    - steps overview: 
    
        1. annotate images
        2. prepare `tfrecord` files 
            -which each holds an image and its corresponding annotation
        3. configure a training pipeline
            -instead of training model from scratch, apply transfer learning from a pre-trained model
        4. train the model
            -takes less time if we use Google Colab's free GPU (by the Jupyter Notebook from DLology website) because laptop's GPU isn't strong enough
        5. export the trained model
     
   
```
After completing the steps above, you should have 3 files downloaded to your local PC
    1. frozen_inference_graph.pb (executes to inferencing of new inputs)
    2. label_map.pbtxt (maps the object class name to an integer)
    3. ssd_mobilenet_v2_coco.config (the configured training pipeline)
```
