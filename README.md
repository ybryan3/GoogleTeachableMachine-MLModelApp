# GoogleTeachableMachine-DeepLearningModelApp

★This content is a by-product of a lesson provided at (https://youtu.be/USQGTW34lO8).

Were you ever interested to learn how to deploy your own website for free?
Were you ever interested to get a touch of building a machine learning model, but did not know where to begin?
Then, this is a tutorial for you!

The first thing to note:

A Teachable Machine (https://teachablemachine.withgoogle.com/) is a web tool that makes it fast and easy to create machine learning models for your projects, no coding required. Train a computer to recognize your images, sounds, & poses, then export your model for your sites, apps, and more.

Netlify (https://www.netlify.com) is a web development platform that multiplies productivity. By unifying the elements of the modern decoupled web, from local development to advanced edge logic, Netlify enables a 10x faster path to much more performant, secure, and scalable websites and apps.



We will take a look at the Image Model portion of a teachable machine in this tutorial. Follow the steps described below.

1) Log on to Teachable Machine and Click on the "Image Project"

Image Project serves to use pictures as input data to the "Train Model" shown in the 2nd "inst.jpg".

You may Name class 1, class 2 in your own interest, and gather the pictures needed for each of them.

After downloading the model with "download my model", unzip the files.

My folder which I saved the files to and its file path is shown in "filepath.jpg"

Now is the time to use metadata.json, model.json, weights.bin, and implement them into a website.

I used Visual Studio Code as an IDE.

The website at the end will take an input of "real-time webcam recording from user computer", then output "an object most likely to be", or "not recognizable"

You can see how model.json and metadta.json are used in lines 32 and 33.

const URL is defined as the file path at line 21 of "index.html"

At init(), the website should ask the user for webcam access, then run the analysis on what is seen.

If the ML model derives a probability of more than 90% that the object shown in the webcam is prediction[0], then a string message is shown on the website that the object shown is the red pen.

If the ML model derives a probability of more than 90% that the object shown in the webcam is prediction[1], then a string message is shown on the website that the object shown is the blue pen.

If the object is shown on the webcam does not fall into the above criteria, then a string message that the object is not recognizable is shown to the user.

After coding is completed to meet your interest, follow the step-by-step guide on how to upload a website on Netlify.

Link: https://www.netlify.com/blog/2016/09/29/a-step-by-step-guide-deploying-on-netlify/



The result will look something like the link below this after publication.

Link: https://redbluepensver2.netlify.app/

Q. So, how can this be useful?

Well, there could be a vehicle that is meant to be driven along the fixed path with various waypoints.

Assuming the real-time vehicle camera recordings replace the webcam input in the website built, then the vehicle would be able to know its waypoints.

Q. What should be done so that ML model recognizes the object in high accuracy?

Consider elements or factors of what makes Class(pens for me) as the ones you named.

background-color
Different type of pens
Pen's position with respect to webcam frame/or whether the pen is cut off from the frame



