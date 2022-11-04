# Bosch Digital Twin

### Current 2 ways to access the project files:
1. Download the project file at the Google Drive Link here https://drive.google.com/file/d/1nLYiE6tKn-VuaBJ-lygrG3-9saaCYCv8/view?usp=sharing
2. Bosch Laptop SGPZ73012 which I have passed to Trung 

### Download Pre-requisite
- Version of Unity3D used must be 2020.1.8f1 to run the project. Other version will result in inconsistencies.

### Launching Unity3D Scene
- Go to Asset/Scene and launch SampleScene. Successful launching would result in the same scene as seen below
![image](https://user-images.githubusercontent.com/38741564/199883763-6d37a470-3a0e-4577-bca0-73a3fd9614aa.png)

### Launching Digital Twin Demo
- Go to Game tab and click on the play icon as seen below. The demo will begin and objects will start to move on the conveyor belt. *Object picking motion for the robotic arm is not yet implemeted.
- ![image](https://user-images.githubusercontent.com/38741564/199903424-f0544b28-ba99-4bcb-9f92-47709fe81c2f.png)

### Connecting a physical robotic arm to Unity3D
- Check the IP address for the robotic arm (192.168.1.2 at the time of this entry) and ensure that the physical robotic arm is switched on
- Click on the first icon on the right panel as seen below after [Launching Digital Twin Demo] is done and type in the IP address for the robotic arm to connect
- Jogging the robotic arm physically will allow the robotic arm to follow the same motion in Unity3D
- ![image](https://user-images.githubusercontent.com/38741564/199921674-417d6f60-da25-4d76-b832-29ebfcf1f162.png)

### Connecting a virtual robotic arm to Unity3D
- Create a ABB ARM1200 robotic arm in RobotStudio with virtual controller and check for its IP address while it is active in the background.
- Click on the first icon on the right panel as seen below after [Launching Digital Twin Demo] is done and type in the IP address for the robotic arm to connect
- Jogging the robotic arm physically will allow the robotic arm to follow the same motion in Unity3D


### Important Files
These files can be retrieved from Scripts folder of the project
1. Scripts/ABB/Link --> This folder is comprises of 6 parts which irb120_link1 forming the base of the robotic arm and irb120_link6 forming the end-effector of the robotic arm. These 6 parts make up the 3D model used for the IRB120 robotic arm in Unity3D in which the inital postion vector of Link1 will undergo Euler Transformation with reference to the position vector of its N-1 counterpart until all 6 parts are completely transformed.

3. Abb_data_processing -> 

2. Conveyor Belt -> Conveyor speed is set at 0.5 m/s for faster simulation instead of the deafult 0.28 m/s that the project use but this setting can be changed anytime. Do remember to set the Box Collider to Is Trigger to allow the object to not fall through conveyor 

3. Main UI --> Reads the connection status of the robotic arm and its joint angle 
