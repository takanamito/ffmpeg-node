#FFMPEG-NODE

Node.js module to control ffmpeg
###To install
>npm install ffmpeg-node

<h3>Usage</h3>:

```   ffmpeg.call(
      [ ... ],                 // array of ffmpeg flags
      callback                 // function to call after ffmpeg is done
   );
   ```

<p>Examples:</p>

<p>   See file test.js

These are the ffmpeg commands used by the module for the convenience methods.
(If you know how to improve them for better quality/speed, please let me know).</p>

 ```
 mp4:

   ffmpeg -i ./test.3gp \
      -acodec libfaac -ab 128k -ar 41000 \
      -vcodec libx264 -vpre slow -vpre baseline -s 640x360 -r 25 \
      ./test.mp4


   ogg:

   ffmpeg -i ./test.3gp \
      -acodec libvorbis -ab 128k -ar 41000 \
      -vcodec libtheora -s 640x360 -r 30 \
      ./test.ogg

   webm:

   ffmpeg -i ./test.3gp \
      -acodec libvorbis -ab 128k -ar 41000 \
      -vcodec libvpx -s 640x360 -b 614400 -aspect 16:9 \
      ./video.webm

``` 
