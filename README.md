# Description
A docker image for adding the popular "Deep Dream" effect to videos using Google's code.

# Usage

```
docker run --rm -it -v `pwd`/images:/images -v [path to video file]:/ddd/video.mp4 natelehman/dreamvideo [desired objective]
```
### Example

```
docker run --rm -it -v `pwd`/images:/images -v `pwd`/cut.mp4:/ddd/video.mp4 natelehman/dreamvideo 'conv2/3x3_reduce'
```


An `images` directory will be created in the directory that you run the command. Once the command finishes running (could take a while) it will contain all of the frames (converted and not converted) as well as the output video file.
### Note
If you run the command with an images directory already created in your current directory it will *fuck your shit*. It shouldn't be destructive, but the command just won't work as intended.




I stole a bunch of code from these places:

[https://github.com/mjibson/ddd]

[https://github.com/graphific/DeepDreamVideo]
