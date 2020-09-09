# Retro Sound chip simulator for FabGL devices
Retro Sound chip simulator for FabGL devices

Just a small demo to show how to do sample retro sounds.

Thanks to www.FabGL.com - 2019 by Fabrizio Di Vittorio for this amazing library. 

Thanks to Shenzhen Xin Yuan Electronics for the funny TTGO VGA32 http://www.lilygo.cn/.

I've enjoyed playing with it.


9/9/2020 - Version 0.1

https://github.com/carlesoriol/fabgl_soundchipsimulator


Carles Oriol - Barcelona 2020
carlesoriol@gmail.com

## playSound function
freertos async sound modulator

Just call it with: playSound( playsounddata ps ); where playsound data:
```
enum wavetype { WAVE_SQUARE, WAVE_SINE, WAVE_TRIANGLE, WAVE_SAW, WAVE_NOISE };
enum modfreqmode { MODFREQ_NONE, MODFREQ_TO_END, MODFREQ_TO_RELEASE, MODFREQ_TO_SUSTAIN  };

struct playsounddata
{
  long attack; // time in millis 
  long decay; // time in millis
  int sustain; // 0-127 range (over total volume)
  long release; // time in millis

  wavetype wave; // square, sine, triangle, saw, noise
  int volume; // 0 to 127
  int durationms;
  int freq_start;
  int freq_end;
  modfreqmode modfreq;

};
```

## License
[AGPL](https://choosealicense.com/licenses/agpl/)
