# Intel Realsense t265 for Unreal Engine 5.5

Intel Realsense t265 into Unreal Engine 5.5 Windows only. I updated this plugin from the orginal https://github.com/bjarque/t265_UE

This script sends data into Unreal Engine through the JSON liveLink plugin. Works with both location and rotation so useful for Virtual Production 

I have found that this exact combination of SDK, version of Python and specific version of pyrelease 2 works for 5.4/5.5



# Instructions
1. Install Intel Realsense SDK: 2.50 
https://github.com/IntelRealSense/librealsense/releases/download/v2.50.0/Intel.RealSense.SDK-WIN10-2.50.0.3785.exe

Once completed open the Realview software to ensure camera being picked up. The T265 should also show under Device Manager in Windows


2. Install python 3.7.9, and remember too add it to PATH option when installing

https://www.python.org/ftp/python/3.7.9/python-3.7.9-amd64.exe

 
3. Once Python is installed open we need to install pyrelease2 2.50.0.3812

To do this Open Windows CMD window with administrator rights and type: 

"pip install pyrealsense2==2.50.0.3812"


4. Download the Precompiled Unreal 5.5 plugin from link here

Unzip it and put it in the Plugins directory of your project


5. Next Launch the project and Configure livelink to recieve on localhost. I have used 127.0.0.1:54321 as my ip in this example

 ![image](https://github.com/user-attachments/assets/f03f96da-fa64-466f-b9bd-3e48b45bcf92)

6. Run script from repo with the command "py tracker.py (ip address same as livelink)", e.g. "py tracker.py 127.0.0.1" You can optinally add destination ips as arguments to the command. (ex: "py tracker.py 127.0.0.1 10.0.0.2", would send to 2 destinations)

 ![image](https://github.com/user-attachments/assets/d1449c29-7f4e-46b5-aefb-d5c8f8084777)


8. Add livelink component to your cinecamera and select MHtrack as your "Subject representation"

 ![image](https://github.com/user-attachments/assets/5eebe125-1ccd-489c-b475-5d4e4f1b75f9)


The camera should now be moving as you move the T265


Thats it! 




