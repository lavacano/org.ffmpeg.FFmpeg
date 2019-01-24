# org.ffmpeg.FFmpeg

This is a Flatpak manifest for FFmpeg built with many advanced features for transcoding. It is built with additional libraries listed below as well as assembly optimizations when possible:

| Project                                                            | Version    | Extra info               |
|:------------------------------------------------------------------:|:----------:|:------------------------:|
| [FFmpeg](https://ffmpeg.org/)                                      | 4.1        |                          |
| [libaom](https://aomedia.googlesource.com/aom/)                    | Recent git |                          |
| [x264](https://www.videolan.org/developers/x264.html)              | Recent git | 10 bit                   |
| [x265](http://x265.org/)                                           | 3.0        | 12 bit                   |
| [libvpx](https://www.webmproject.org/code/)                        | 1.7.0      | 8–12 bit VP9             |
| [libfdk-aac](https://github.com/mstorsjo/fdk-aac)                  | 2.0.0      |                          |
| [libmp3lame](http://lame.sourceforge.net/)                         | 3.100      |                          |
| [libopus](http://opus-codec.org/)                                  | 1.3        | w/ custom modes          |
| [libvorbis](https://xiph.org/vorbis/)                              | 1.3.6      |                          |
| [libass](https://github.com/libass/libass)                         | 0.14.0     | w/ harfbuzz & fontconfig |
| [libzimg](https://github.com/sekrit-twc/zimg)                      | 2.8        |                          |
| [opencl](https://www.khronos.org/opencl/)                          | 2.2        |                          |
| [nvdec/nvenc](https://developer.nvidia.com/nvidia-video-codec-sdk) | 8.2.16     |                          |

To install you need the Flathub repository as a remote

```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

Then you build and install FFmpeg and its dependencies with

```bash
flatpak-builder --user --force-clean --install builds org.ffmpeg.FFmpeg.yaml
```
