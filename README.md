# Optical Recognition

Our optical recognition software is designed for users to be able to automatically upload videos for analysis, extract key games data, store the data in a database, and utilize a dashboard so that they can use the system.

## Installation

Our project used to have a custom URI, but not anymore so unfortunately you'll have to setup everything locally if you want to see the website.

Reccomended Python version: 3.9.13.
1. Create your virtual enviroment using command "python -m venv venv" in the root directory of project
2. Activate the virtual enviroment using ".\venv\Scripts\activate"
3. Then use command "pip install -r requirements.txt" to install all required packages for the project.

## Configuring Database

1. Download MySQL server to host the server for the database
2. Configure mysql server during installation setup so it satisfies DATABASE dictionary located in opticalrec/.env.
3. Make the password to the server "fsp-password123", user: "root", hostname as: "127.0.0.1", port as: "3306".
3. Make sure the sql server is running.
4. Download SQL workbench and connect it to the sql server using credentials you set the server up with in step 3.
5. Create a scheme with name "opticalrec_db"

## Final Steps
1. Change directory from root directory to opticalrec/
2. And run these commands in your terminal if this is your first time creating the database or changing anything such as creating new models, changing existing ones, or adding/removing fields.:
    "python manage.py makemigrations"
    "python manage.py migrate"
3. Once ran run this command: "python manage.py runserver"
4. The application server should be running at "http://127.0.0.1:8000/"




## Application Usage
1. Navigate to the link shown above
2. If an account has been made, sign in by clicking "Login" in the profile tab. Else, sign up by clicking "Register" in the profile tab.
3. Go to the "Upload" tab and select a name and the video file to be uploaded to the dashboard.
4. Crop the frame that you want to be analyzed by using the cropper tool. Multiple croppings of different frames are also possible.
5. Once you have decided all the frames that you want to be analyzed, click "Finished"
6. You will be directed to the "Video List" tab. Here, all of your videos are stored. Available options are to crop another frame again, delete the video, or extract the data to the dashboard.
7. If data is extracted, you will be redirected to the "Dashboard" tab and the data can be seen in a table format.
8. Click "Export All to CSV" if you want the data to be downloaded to your computer in a CSV format.


In the test folder there is a video that demonstrates the type of information the project was made for. It detects numbers throughout the video by capturing frames of the video and processing it through tensorflow for analysing in which we store at the end as a .csv file for the user to download and analyse their gameplay.

## Authors and acknowledgment
This project is the combined work of Zach Larsen, Imran Lawal, Howard Kang, Robbie Hill and Ikenna Nnaji. Special thanks to our supervisor John Drake for his guidance and support and to Jeremy Levesley for being our client for this project.
