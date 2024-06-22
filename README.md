


<h2>Objective :</h2>
<p>To build a gender and age detector that can approximately guess the gender and age of the person (face) in a picture or through webcam.</p>

<h2>About the Project :</h2>
<p>In this Python Project, I had used Deep Learning to accurately identify the gender and age of a person from a single image of a face. The predicted gender may be one of ‘Male’ and ‘Female’, and the predicted age may be one of the following ranges- (0 – 2), (4 – 6), (8 – 12), (15 – 20), (25 – 32), (38 – 43), (48 – 53), (60 – 100) (8 nodes in the final softmax layer). It is very difficult to accurately guess an exact age from a single image because of factors like makeup, lighting, obstructions, and facial expressions. And so, I made this a classification problem instead of making it one of regression.</p>

<h2>Dataset :</h2>
<p>For this python project, I had used the Adience dataset; the dataset is available in the public domain and you can find it <a href="https://www.kaggle.com/ttungl/adience-benchmark-gender-and-age-classification">here</a>. This dataset serves as a benchmark for face photos and is inclusive of various real-world imaging conditions like noise, lighting, pose, and appearance. The images have been collected from Flickr albums and distributed under the Creative Commons (CC) license. It has a total of 26,580 photos of 2,284 subjects in eight age ranges (as mentioned above) and is about 1GB in size. The models I used had been trained on this dataset.</p>

<h2>Additional Python Libraries Required :</h2>
<ul>
  <li>OpenCV</li>
  
       pip install opencv-python
</ul>
<ul>
 <li>argparse</li>
  
       pip install argparse
</ul>

<h2>The contents of this Project :</h2>
<ul>
  <li>opencv_face_detector.pbtxt</li>
  <li>opencv_face_detector_uint8.pb</li>
  <li>age_deploy.prototxt</li>
  <li>age_net.caffemodel</li>
  <li>gender_deploy.prototxt</li>
  <li>gender_net.caffemodel</li>
  <li>a few pictures to try the project on</li>
  <li>detect.py</li>
 </ul>
 <p>For face detection, we have a .pb file- this is a protobuf file (protocol buffer); it holds the graph definition and the trained weights of the model. We can use this to run the trained model. And while a .pb file holds the protobuf in binary format, one with the .pbtxt extension holds it in text format. These are TensorFlow files. For age and gender, the .prototxt files describe the network configuration and the .caffemodel file defines the internal states of the parameters of the layers.</p>
 
 <h2>Usage :</h2>
 <ul>
  <li>Download my Repository</li>
  <li>Open your Command Prompt or Terminal and change directory to the folder where all the files are present.</li>
  <li><b>Detecting Gender and Age of face in Image</b> Use Command :</li>
  
      python detect.py --image <image_name>
</ul>
  <p><b>Note: </b>The Image should be present in same folder where all the files are present</p> 
<ul>
  <li><b>Detecting Gender and Age of face through webcam</b> Use Command :</li>
  
      python detect.py
</ul>
<ul>
  <li>Press <b>Ctrl + C</b> to stop the program execution.</li>
</ul>

# Working:
[![Watch the video](https://img.youtube.com/vi/ReeccRD21EU/0.jpg)](https://youtu.be/ReeccRD21EU)

<h2>Examples :</h2>

    >python detect.py --image girl1.jpg
    Gender: Female
    Age: 25-32 years
    
![image](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/79d17632-86d6-4f10-ae19-4d0911027c2c)

    >python detect.py --image girl2.jpg
    Gender: Female
    Age: 8-12 years
    
![Detecting age and gender girl2](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/97ba02b6-5593-42c8-9a23-b04883d013f0)

    >python detect.py --image kid1.jpg
    Gender: Male
    Age: 4-6 years    
    
![Detecting age and gender kid1](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/a1acdadd-8816-453b-86d8-7e6a347c01ab)

    >python detect.py --image kid2.jpg
    Gender: Female
    Age: 4-6 years  
    
![Detecting age and gender kid2](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/e6912f84-b112-4a73-a6f8-12f368eaab94)


    >python detect.py --image man1.jpg
    Gender: Male
    Age: 38-43 years
    
![Detecting age and gender man1](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/89d701e6-0262-4158-92c7-734fe90be1b9)


    >python detect.py --image man2.jpg
    Gender: Male
    Age: 25-32 years
    
![Detecting age and gender man2](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/f0199df9-f6e1-4899-9d81-883263604dfc)


    >python detect.py --image woman1.jpg
    Gender: Female
    Age: 38-43 years
    
![Detecting age and gender woman1](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/assets/170930248/b867e719-2069-446a-b12d-222c9f8dcc12)

### Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
              
### License

This project is licensed under the [MIT license](https://github.com/KrishnaveniGarla/Gender-and-Age-Prediction/tree/main?tab=MIT-1-ov-file#:~:text=README-,MIT%20license,-MIT%20License%0A%0ACopyright) - see the LICENSE file for details.
