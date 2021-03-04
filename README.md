# ArionIMC_CameraPlay
ArionIMC를 활용한 카메라 영상 재생

## 작동환경
1. ubuntu 18.04 LTS
2. JetPack 4.4
4. gstreamer 1.14.5


## 준비물
![requisite](https://user-images.githubusercontent.com/44572895/109899633-7a81b380-7cd9-11eb-8956-0099fb944eac.jpg)


카메라 전원 어댑터 / 카메라 / micro HDMI to micro HDMI / ArionIMC / ArionIMC 전원 어댑터

키보드 / 마우스 / micro B OTG

## 명령어
$ gst-launch-1.0 v4l2src device=/dev/video0 ! ximagesink

"gst-launch-1.0"

-> arionIMC에 설치되어있는 gstreamer를 통해 영상을 재생하기 위한 gstreamer element 명령어.

"v4l2src device=/dev/video0"

-> v4l2는 Video 4(For) Linux 2의 준말로, Linux System에서 실시간 비디오 캡쳐를 위해 제공되는 API와 Device Driver의 모음을 의미함. 

v4l2src 명령어를 통해 gstreamer에서 v4l2 element를 사용할 수 있게 됨. 이를 통해 arionIMC에 연결한 카메라 소스에 대해 데이터를 읽어오는 것이 가능해짐.
"device=~" 명령어를 통해 video0 장치에 대해 Stream을 읽어오겠다고 명시함.

"ximagesink"

-> 모니터에서 영상을 확인하기 위한 gstreamer element

## 실행영상
![20210304071950-272020bd79 gif-2-mp4 com](https://user-images.githubusercontent.com/44572895/109910965-8fb40d80-7cec-11eb-81e5-248f1d2e13dd.gif)
