# ESP32_AWS_IoT_EduKit_Web_radio  
fork https://github.com/bwbguard/M5Stack-Core2-MediaPlayer, and slightly modified to suit AWS Core2.   


add Asia radios stations for testing, no CHT font displyesd, terminal debug string is ok, but not LCD  
```
const int stations = 12;// Change Number here if you add feeds!
char * stationList[stations][2] = {
  {"中文RTHK1", "http://stm2.rthk.hk:80/radio1"},
  {"RTHK2", "http://stm2.rthk.hk:80/radio2"},
  {"RTHK3", "http://stm2.rthk.hk:80/radio3"},
  {"RTHK4", "http://stm2.rthk.hk:80/radio4"},
  {"RTHK5", "http://stm2.rthk.hk:80/radio5"},
  {"Charlie FM", "http://24083.live.streamtheworld.com:80/KYCHFM_SC"},
  {"MAXXED Out", "http://149.56.195.94:8015/steam"},
  {"Orig. Top 40", "http://ais-edge09-live365-dal02.cdnstream.com/a25710"},
  {"Smooth Jazz", "http://sj32.hnux.com/stream?type=http&nocache=3104"},
  {"Smooth Lounge", "http://sl32.hnux.com/stream?type=http&nocache=1257"},
  {"Classic FM", "http://media-ice.musicradio.com:80/ClassicFMMP3"},
  {"Lite Favorites", "http://naxos.cdnstream.com:80/1255_128"}
};


```


setup, add volume preset,  

```
setup() {

  Serial.println("xiaolaba test, AWS IoT Edukit for web radio");
  audioGain = 8.0;  // preset
  
  changeVolume();  // To update Volume setting and graphic
  displayWiFiInformation();
}
```
