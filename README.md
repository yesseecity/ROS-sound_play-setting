# Switch audio output in commandline of RPi
### Auto  
```
amixer cset numid=3 0
```
### 3.5mm Jack  
```
amixer cset numid=3 1
```

### HDMI  
```
amixer cset numid=3 2
```
### Play Mp3 File
```
mplayer  music.mp3
```


### Volume control
At first, we use ```amixer scontrols``` to show yourmixer control.  
Or use ```alsamixer```

```
amixer sset 'PCM' 80%
```

### catkin_make
```
catkin_make
source ./devel/setup.bash
echo source $(pwd)/devel/setup.bash >> ~/.bashrc
```

### Install ROS sound play depdence
When catkin_make done, use rosdep install sound_play
```
rosdep install sound_play
```

### remake 
```
catkin_make
```


# Sound Play Node
In ```soundplay_node.launch``` you can set device path in linux env, for example '/dev/audio' is  
