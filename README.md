<h1 align="left">
    Social Distancing Detector
</h1>

A social distancing detector built with OpenCV using YOLO V4 object detector

<h2> Motivation<span style='font-size:100px;'>;</span></h2>	
<p>
Social distancing is a method used to control the spread of contagious diseases. It implies that people physically distance themselves from one another, reducing close contact, and thereby reducing the spread of a contagious disease (such as the COVID-19 Disease). 
</p>


## Features :
* Object detection using the YOLO COCO model to detect only people in a video stream.
* Computes the pairwise distances between all detected people.
* Based on the computed distances, we determine whether social distancing rule is being violated or not.


## Installation :

1. Clone the repo

```bash
   $ git clone https://github.com/aibenStunner/social-distancing-detector.git
   $ cd social-distancing-detector
```

2. Install dependencies

```bash
   $ pip install -r requirements.txt
```

3. Run the main social distancing detector file. (set display to 1 if you want to see output video as processing occurs)
```bash
   $ python social_distancing_detector.py --input pedestrians.mp4 --output output.avi --display 0
```

## Usage :
* Caution :
For most accurate results, you should calibrate your camera through intrinsic/extrinsic parameters so that you can map pixels to measurable units.
An easier alternative(but less accurate) method would be to apply triangle similarity calibaration. Both of these methods can be used to map pixels to measurable units.\
If you do not want/cannot apply camera calibration, you can still utilize the social distancing detector but you'll have to rely strictly on the pixel distances, which won't necessarily be accurate.
For the sake of simplicity, this OpenCV Social Distancing detector implementation will rely on pixel distances. 
You can extend the implementation as you see fit though .

* YOLO COCO weights\
The weight file exceeds the github limits but can be download from <a href="https://pjreddie.com/media/files/yolov3.weights">here</a>.\
Add the weight file to the yolo-coco folder.

* GPU\
Provided you already have OpenCV installed with NVIDIA GPU support, all you need to do is set ```USE_GPU=True``` in your ```config.py``` file.

## Demo :
![raw-vid](res/demo0.gif "Unprocessed video") ![processed-vid](res/demo1.gif "Processed video")

## Contributing : 
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.

## Connect :

If you  have something to suggest  you can catch me around the web .

- Email - ramcharanteja.380@gmail.com 
- Let's connect on <a href="https://www.linkedin.com/in/ramcharan-teja-256704182/">LinkedIn.</a> :pushpin:


## References :
* <a href="https://en.wikipedia.org/wiki/Social_distancing">Social Distancing</a>
* <a href="https://www.reddit.com/r/computervision/comments/gf4zhj/automatic_social_distance_measurement/">Automatic social distance measurement</a>
* <a href="https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A6661455400346492928/">Rohit Kumar Srivastava’s social distancing implementation</a>
* <a href="https://www.linkedin.com/feed/update/urn%3Ali%3Aactivity%3A6655464103798157312/">Venkatagiri Ramesh’s social distancing project</a>

## Todos :
* Utilize proper camera calibration.
* Apply top-down transformation of view angle.
* Improve the poeple detection process.

## License and credits :

MIT &copy; Gadri Ebenezer
