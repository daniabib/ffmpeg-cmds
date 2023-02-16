## 1. From POCOPHONE to Davinci Resolve 

from H.264 to PRORESS

```bash
ffmpeg -i INPUT.mp4 -c:a copy -c:v prores -profile:v 0 -pix_fmt yuv422p10 OUTPUT.mov
```

https://ottverse.com/ffmpeg-convert-to-apple-prores-422-4444-hq/
https://wideopenbokeh.com/AthenasFall/?p=111

## 2. Davinci Resolve Timeline
https://videowithjens.com/how-to-make-instagram-reels-in-davinci-resolve-full-guide/

## 3. Mixing in Resolve
Guitar and vocals:
https://www.youtube.com/watch?v=5-0aQGUiycY&t=126s

Compression:
https://www.youtube.com/watch?v=LAZ-bkK-AGw

## 4. Resolve Export
- Settings
![Davinci Settings](export-settings.png)

## 5. Convert MXF to MOV
```bash
ffmpeg -i CINCO-OUT.mxf -pix_fmt yuv420p -c:v libx264 -c:a aac -b:a 384k -sn MXF-OUT.mov
```

## 6. Cut
```bash
ffmpeg -i INPUT.mov -ss 00:00:00 -to 00:40:00 OUTPUT.mov
```

## PNG to file
### MP4
```bash
ffmpeg -framerate 24 -pattern_type glob -i '*.png' -c:v libx264 -pix_fmt yuv420p out.mp4
```

### PRORES
```bash
ffmpeg -framerate 24 -pattern_type glob -i '*.png' -c:v prores -profile:v 0 -pix_fmt yuv422p10 out.mov
```
