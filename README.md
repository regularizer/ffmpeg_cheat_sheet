# ffmpeg cheat sheet
frequently used command

***

## [ffmpeg](https://www.ffmpeg.org/) wiki! for frequently used command:
ffmpeg tools: **ffmpeg**, **ffplay**, **ffprobe**

***

### windows: 
cmd -> ffmpeg\bin\ffmpeg.exe

### video converter
`ffmpeg -i path\input.mov -acodec copy -vcodec copy path\output.mp4`

### key frame extraction from video
`ffmpeg -i path\input.mov -vf select='eq(pict_type\, I)' -vsync 2 -f image2 path\keyframe_%03d.jpg`

### convert framerate without changing the video length
`ffmpeg -i path\input.mov -r 30 -c:v libx264 -y path\output.mov`

### rotating video
`ffmpeg -i path\input.mov -vf "transpose=1" path\output.mov`  
transpose parameter use  
0 = 90CounterCLockwise and Vertical Flip (default)  
1 = 90Clockwise  
2 = 90CounterClockwise  
3 = 90Clockwise and Vertical Flip  
-vf "transpose=2,transpose=2" for 180 degrees  
