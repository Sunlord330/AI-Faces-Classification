## AI-Faces-Classification


DetectNet "detects" your emotion 

## The Algorithm

I used premade Python code from JupyterLab and put fifty pictures of my face in each category

## Running this project
**Important** You will **need** a Jetson Nano, PuTTY (also make sure to never update the Jetson Nano, this will corrupt it)

1. First open Device Manager and look for the ports (COM & LPT) section to find the COM number for your connection (if there are multiple COM devices in the list, unplug the data cable from the microUSB port on your Nano and make note of which COM devices remain listed, then reconnect the data cable and look for the new COM device added)
2. Use PuTTY to open the serial communication line by setting the following: Category: Session, Connection type: Serial
Serial line: COM4, Speed: 9600
3. Then enter the username and passcode which are both nvidia
4. Then set up a mobile hotspot on Windows with 2.4 GHz network bandwidth and connect to it using this command sudo nmcli --ask device wifi connect 'name of wifi'
6. Under Share my Internet connection from, choose your internet connection, then set Share my Internet connection over to Wi-Fi, and click to enable Share my Internet connection with other devices.
7. Go into your command prompt and type ipconfig and find an IP address called inet.
9. Now use PuTTY to open the ssh communication line by setting the following: Category: Session, Connection type: SSH, Host Name or IP address/(inet): X.X.X.X, Port: 22
10. And then enter the username and password which is nvidia
11. In the directery /home/nvidia you need to paste this docker command: ./docker_dli_run.sh
12. Then you shuld go to a webbroser and look up http:// + Jetson Nano IP + 888/lab  (password=dlinano)
13. Navagate to  /classification and open classification_interactive.ipyn
14. Then scroll down to task and uncomment # TASK = 'emotions', and # CATEGORIES = ['none', 'happy', 'sad', 'angry'] and comment TASK = 'thumbs', and CATEGORIES = ['thumbs_up', 'thumbs_down']
15. then run all the cells and enjoy!!!

[View a video explanation here](video link)
