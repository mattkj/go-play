# go-play-quiet

## tldr;
I lowered the volume steps in the `go-play` code from {0, 125, 250, 500, 1000} to
{0, 30, 70, 100, 125} and made a build so people can use it.

## Full explaination
I've seen a lot of people online complaining about the sound on the ODROID-Go.
It's crazy loud by default and there isn't any easy way for people to lower the volume to anything with a reasonable volume. I made a small change to the
`odroid-go-common/components/odroid/odroid_audio.c` file so the most quiet
volume is now the loudest, with smaller steps.

I used [Odroid-Go-Tools](https://github.com/23pieces/Odroid-Go-Tools/tree/master/make_goplay) to make my build, I'd recommend it if you want to make your own build of the current OS.

## Install
1. Turn off your ODROID Go. I'd recommend exiting the game if you're in one, just so your progress saves. (Note: this should **not** effect any ROM files you have on your SD card)
2. Download a new release [here](https://github.com/milesoberstadt/go-play-quiet/releases/latest). All you need is to download the `Go-Play-Quiet.fw` file.
3. Remove your microSD card from your ODROID Go, put it in a microSD card reader, and plug that into your computer. Copy that to the following path on your microSD card: `odroid/firmware`
4. Remove your microSD card from your computer and put it back in your ODROID Go.
5. Hold **B** on your ODROID Go and turn the power on. Keep holding **B** until you boot into Springboard (you should see your `Go-Play.fw` file and `Go-Play-Quiet.fw`)
6. Select `Go-Play-Quiet` with **A**, then press **Start** to confirm flashing this firmware.
7. Wait a minute or so while all 4 firmware partitions flash.
8. Your ODROID Go should boot to the new firmware.
