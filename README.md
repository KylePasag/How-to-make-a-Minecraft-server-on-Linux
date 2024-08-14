# How-to-make-a-Minecraft-server-on-Linux

![image](https://github.com/user-attachments/assets/8887f7b7-efe4-407d-a7a5-9d161bf1d238)
> [!IMPORTANT]
> This script is made specifically for minecraft java edition and Ubuntu distro, using other distros might not work.
## Tutorial
Install java
```
sudo apt update && sudo apt upgrade -y
sudo apt install default-jre-headless
```
Create a directory 
```
mkdir minecraft_server
cd minecraft_server
```
Install the minecraft server jar file from the [offical minecraft website](https://www.minecraft.net/en-us/download/server)
```
wget https://piston-data.mojang.com/v1/objects/59353fb40c36d304f2035d51e7d6e6baa98dc05c/server.jar
```
Open server file
```
java -Xmx1024M -Xms1024M -jar minecraft_server.1.21.1.jar nogui
```
> [!WARNING]
> You might need a newer version of java for newer minecraft versions. In that case, you need to install the specific java version by doing sudo apt install openjdk-21-jre-headless. >
Accept eula agreement 
```
nano eula.txt
```
Change eula=flase to eula=true
```
eula=true
```
Ctrl x + y to save
Run the server file again
```
java -Xmx1024M -Xms1024M -jar minecraft_server.1.21.1.jar nogui
```
> [!TIP]
> You can further increase the memory allocated by changing Xmx and Xms numbers. You can also change the unit of measurement by changing the 'M' (mb) on Xmx1024M to 'G' (gb). This can further increase the performance of the server and decrease latency. >
You're all done!
