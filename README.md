# print-pod-stream
--------------
This is a really simple set of files that makes it easier to stream an array of webcams through OBS. Examples can be found on the [Clemson Makerspace Youtube Channel](https://www.youtube.com/channel/UCxhofKqVc4fUdA4Ro0gVvOA).

There are two files included in this repo.

1. ppod_camera.html - this file composes 6 different webcam streams into a two tier scene. All you have to do is change the `<img src>` tags to point at the camera streams you want
1. status_overlay.html - this file overlays the stats from each printer onto the streams. This is accomplished through a couple Octoprint API calls. There are also a few lines of code that call the Formlabs dashboard API commands to update status for our Form 2 printers. You will need to find your [Octoprint API key, and turn on CORS](http://docs.octoprint.org/en/latest/api/index.html).

Host each of these files on a server that can be seen by your OBS encoder and modify the API keys and `<img src>` links to point at the printers you need. Then add two Browser Sources in OBS - one for the cameras and one for the overlay.
