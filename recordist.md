# Recordist Role

So you wanna be a recordist?

The recordist is responsible for setting up the capture device (Mevo), recording the jams, monitoring audio levels, and uploading the recordings to the 'tube.

## Recordist inventory

- Mevo
- Gorilla tripod
- Travel wireless access point (repeater)
- USB-A to USB-mini power cable
  - to power the travel wireless
- 2x USB-A to USB-C power cable
  - to charge the Mevo
  - to charge your phone
- 1/8 to 1/4 stereo audio cable
- wireless stereo transmitter and receiver

## Set up the capture device: Mevo

You may have your own capture device (a GoPro for video and a field recorder for audio), but the Art~Hack capture device (provided by Mikey) is a Mevo, described below:

### Tripod

Take the Mevo out of the case and screw onto the tripod.

**Be very careful** because the Mevo's base is munted, there's a big crack, but has survived for years now despite this. _Somebody should_ fix this somehow, but whatever.

### Audio

Make sure to plug in the stereo audio cable from the mixer (use the "phones" output) to the Mevo.

### Internet

(Alternatively, you can use your cellular data with the Mevo and skip this step.)

The Mevo's WiFi doesn't work with Dev Academy WiFi, so we have a special travel wireless access point to use.Plug in the travel wireless access point.

- SSID: Art~Hack
- Password: art~hack

Boot up the Mevo and start up the Mevo app on your phone. Connect both to the Art~Hack WiFi network (2.4 GHz).

Once connected, you should see the video coming from the Mevo onto your phone.

## Record the jams

Record 720p to SD card, maybe stream to Facebook.

Don't stream to Facebook if recording a DJ playing copyrighted material. Lame but is what it is, soz.

Color adjustments: stage or high contrast are great, but depends on the vibe you want.

### Monitor audio levels

A good audio level is one where the audio is usually green (below the limit) and only occasionally goes red (above the limit).

You can change the audio levels within the Mevo app, or using the mixer.

## Upload the recordings to the 'tube

Take the SD card out of the Mevo and plug into your laptop.

With https://github.com/arthacknz/tube-tools installed and configured:

```shell
git pull origin main # to make sure ./data/uploads is up-to-date

./tube-tools upload-dir /path/to/mevo/sd/card
```

This should upload any new videos to the 'tube and our backup storage.

This will also make some new files in `./data/uploaded` which must be commited and pushed.
