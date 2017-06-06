# Face Recognition based on Eigenfaces, SVD, and PCA
The script will detect the face from the web camera and try to recognize it among existing faces in the DB.

## Technologies and needed device:
* Ordinary Web Camera
* Python 2.7
* OpenCV v.2.4.12 (Python library)
* Tested on the device "Banana Pro"

## Brief Description of what I've done
**_[Link to the .pdf report](https://raw.githubusercontent.com/kagan94/Face-recognition-via-SVD-and-PCA/master/Report.pdf)_**

## Recognize the image from the web camera
1) Run **"main.py"**
2) Press on the **"Space"** button on your keyboard. Here, the program will try to recognize the face from the web camera among the existing faces in the DB. During the first recognition, the program will compute eigenfaces, SVD, and PCA. Once it's computed, it'll work much faster.
 
![Recognized face from the DB](https://raw.githubusercontent.com/kagan94/Face-recognition-via-SVD-and-PCA/master/report_imgs/recognized_img.jpg)

## Add new image to the face DB
* either add this image to the folder **"target_imgs"**
* or while running "main.py" in the terminal (command **"python image_preprocessing.py"**) or run this script from your IDE press on **"Space" to capture new image from a web camera**.

![Capture and save image from web camera](https://raw.githubusercontent.com/kagan94/Face-recognition-via-SVD-and-PCA/master/report_imgs/capture_img_from_web_cam.jpg)

After a new image is added, you will need to stop the script "main.py" and run pre-processing step again (to grayscale the image, detect a face, and resize it) by typing command in the terminal **"python image_preprocessing.py"**.

## Plans for future improvements:
* Test the accuracy of the algorithm
* Extract only "k" important features to reduce dimensions during projecting onto PCA space
* Add histogram equalization to frame from web camera/image to improve the quality of the recognition
* Measure execution time of the script and detect the most time-consuming parts of the code (by using timeit or similar tools)
* Add threshold to detect non-existing image in the face DB

## Links:
* [Principal component analysis in Python](http://baxincc.cc/questions/11278/principal-component-analysis-in-python)
* [PCA in Python (Jupiter notebook)](http://www.shogun-toolbox.org/static/notebook/current/pca_notebook.html)
* [PCA via SVD (Matlab example)](http://mghassem.mit.edu/pcasvd/)
* [Matlab to Numpy syntax](https://docs.scipy.org/doc/numpy-dev/user/numpy-for-matlab-users.html)
* [Yale public face dataset](http://vision.ucsd.edu/datasets/yale_face_dataset_original/yalefaces.zip)
* [Code for the book "Mastering OpenCV with Practical Computer Vision Projects" by Packt Publishing 2012.](https://github.com/MasteringOpenCV/code)