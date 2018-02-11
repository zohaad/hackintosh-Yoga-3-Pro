# hackintosh-Yoga-3-Pro

Files for hackintoshing the Lenovo Yoga 3 Pro

## Acknowledgements

_[RehabMan](https://github.com/RehabMan)_ - helped with getting the graphics working and provided the inital config.plist file.

## What works

- Intel HD 5300 integrated graphics with HiDPI 1600x900
- native power management
- WiFi
- audio
- built-in webcam
- iMessage, if you follow [this guide](https://www.tonymacx86.com/threads/an-idiots-guide-to-imessage.196827/)

## What doesn't work

- touchpad
- bluetooth
- built-in microphone
- battery status
- sleep (doesn't work with laptops anyways)
- Siri (lack of built-in microphone, didn't test with 3.5mm jack mic yet)

## Instructions

1. Make a bootable usb the [vanilla way](https://www.reddit.com/r/hackintosh/comments/68p1e2/ramblings_of_a_hackintosher_a_sorta_brief_vanilla/).
2. copy contents of [hackintosh stuff](/hackintosh\ stuff) into the Install MacOS High Sierra partition for post install.
3. Perform post install and enjoy!

## DSDT patching for battery

There is only one `Field (ECF2, ByteAcc, Lock, Preserve)`, the table shows which fields are accessed.

| Field | Size (bit) | Accessed? |
| ----- | ---------- | --------- |
| SMD0  | 256        | yes       |
| PPWR  | 16         | no        |
| B1FV  | 16         | no        |
| B1TM  | 16         | no        |
| B1VT  | 16         | yes       |
| B1CR  | 16         | yes       |
| BAPR  | 16         | no        |
| B1RC  | 16         | yes       |
| B1FC  | 16         | yes       |
| B1CC  | 16         | no        |
| B1CV  | 16         | no        |
| B1DC  | 16         | yes       |
| B1DV  | 16         | yes       |
| BDCW  | 16         | no        |
| BDCL  | 16         | no        |
| B1AR  | 16         | no        |
| B1MA  | 64         | no        |
| B1DN  | 64         | no        |
| B1CH  | 32         | no        |
| B1MO  | 16         | no        |
| B2MO  | 16         | no        |
| B1SN  | 16         | no        |
| B2SN  | 16         | no        |
| B1DT  | 16         | no        |
| B2DT  | 16         | no        |
| B1CY  | 16         | yes       |
| BCRT  | 16         | yes       |
