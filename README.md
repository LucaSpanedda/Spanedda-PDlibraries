## FOCUSRITE 18i20

nel terminale Bash apri il mixer 
con il comando:
```
alsamixer
```

nel mixer premere M per mutare/smutare i canali desiderati,
smutare quindi il canale di master e i canali utili.
I canali hanno un MM scritto se sono muti.

F6 imposta i device.

La focusrite 18i20 funziona solo con le uscite PCM1 e PCM2 su linux
dunque andare su Line out 1 e Line out 2 (L & R) e assegnarli a 
PCM1 e PCM2

(ora dovrebbe funzionare tutto)


## JACK & PURE DATA

installa jack:
```
sudo apt-get install pulseaudio-module-jack
```


## Lancia jack per Pure Data:
```
pacmd load-module module-jack-source channels=2; pacmd load-module module-jack-sink channels=2;
```

chiudi processi jack:
```
killall jackd
killall pulseaudio
```
