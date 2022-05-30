reference

```
https://girishjoshi.io/post/ffmpeg-rtsp-to-hls/
https://dev.to/foyzulkarim/how-to-stream-your-ip-camera-into-browser-using-ffmpeg-node-and-react-162k
https://codepen.io/pen?template=oyLKQb
```

docker old

```bash
docker run --rm -it \
-v $PWD/videos:/videos \
linuxserver/ffmpeg \
-i $RTSP_STREAM \
-fflags flush_packets \
-max_delay 5 \
-flags \
-global_header \
-hls_time 5 \
-hls_list_size 3 \
-vcodec copy \
-y ./videos/index.m3u8
```

docker-compose old

```
-i $RTSP_STREAM -fflags flush_packets -max_delay 5 -flags -global_header -hls_time 3 -hls_list_size 2 -vcodec copy -y /videos/index.m3u8
```
