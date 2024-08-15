# MotionPhoto2

A small script to create Motion Photo v2 from HEIC or JPG files and videos. Resulting files were tested with Google Photos and are accepted as motion/live photo; and when saved to iPhone from Google Photos, they turn back into Live Photos :-)

In case the source is an iPhone Live Photo, the presentation timestamp will be migrated as well, thus the photo will start from the same keyframe.

## Installation

In order to use this, please install [ExifTool](https://exiftool.org/) and put the files in the same directory as exiftool.exe.

## Usage

To convert a pair of image and video to Motion Photo v2, run:

```
> MotionPhoto2.cmd ImageFile.HEIC VideoFile.MOV MotionPhoto.HEIC
```

Alternatively, you can run the powershell script directly:
```
PS> MotionPhoto2.ps1 -imageFile ImageFile.HEIC -videoFile VideoFile.MOV -outputFile MotionPhoto.HEIC
```

## About

The script is written with Windows in mind, but it should be possible to use it on Linux and MacOS too (possibly with some tweaking of the used .Net objects). Patches for this are welcome.

Photos are created to mimic the way Galaxy S20 FE phones create HEIC motion photos. This format internally refers to itself as mpv2, which is referred to in this document as Motion Photo version 2 (even though the XMP tag still says it's version 1).
Thanks to [@tribut](https://github.com/tribut) for uploading a sample photo [here](https://github.com/photoprism/photoprism/issues/1739#issuecomment-1216457652). Without it, this project would never start, as this format is very different from original Motion Photo spec and seems to be amalgamation of Google and Samsung ideas on how to store image and video in the same file.
