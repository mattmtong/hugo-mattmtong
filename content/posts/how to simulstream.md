---
title: "How to Simulstream to Facebook/Youtube/Zoom"
date: 2020-08-30T19:02:33-08:00
draft: false
cover:
    image:
    alt:
    caption:
tags: ["streaming"]
categories: ["tutorials"]
---

The purpose of this guide is to show you how to simultaneously stream to Facebook, Youtube, and Zoom (call/webinar), all from the convenience of OBS.  

## 1. Install and setup OBS

OBS is an open-source broadcasting software that you can download [here](https://obsproject.com)!

Once you've downloaded and installed the application, open it up, and you should be welcomed by the following screen:

![](/img/annotation-2020-09-01-205209_orig.png#center)

OBS is basically a program that lets you create scenes and push those scenes out to a streaming video platform.  That big black screen you see in the middle is called the preview pane, which will show you the preview of what OBS is going to output.  

You should already have a scene created, but let's create a second scene by clicking the "+" at the bottom left of the "Scenes" module, and title it "Scene 2" so we can try toggling between two different scenes.

![](/img/annotation-2020-09-01-213050_orig.png#center)

While making sure Scene 2 is selected, let's add a source to this scene by selecting the "+" icon under the "Sources" module, and selecting "Video Capture Device".  As you can see, the moment you hit "+", you will see all the different types of sources you can add, which provide a lot of freedom and flexibility to your scene creation.

![](/img/annotation-2020-09-01-205656_orig.png#center)

I am assuming that you have access to a webcam, whether it is your built in laptop one or an external USB one.  If not, feel free to add one of the other sources just to experiment!  I will be adding my built in laptop as a source, so I am renaming my source to "Laptop Webcam". 

![](/img/annotation-2020-09-01-212128_orig.png#center)

In the next screen, make sure your webcam of choice is selected next to "Device".  OBS sometimes has issues getting the full resolution of webcams, so I usually take the extra safety measure of changing "Resolution/FPS Type" to "Custom", and then selecting highest possible resolution next to "Resolution".  Click OK!

![](/img/annotation-2020-09-01-212212_orig.png#center)

Depending on the resolution of your webcam source, your source will fill up a certain amount of the screen.  Mine is 720p, so it fills only a portion of the screen.  All the little red squares are draggable (hold alt + drag in order to crop and shift + drag to resize without keeping aspect ratio).  Since we just want to fill up the screen, right click your video in the preview pane and go to Transform > Fit to screen.

![](/img/annotation-2020-09-01-211749_orig.png#center)

Next up, we're going to add an audio source.  Click the same "+" in the "Sources" module and add an "Audio Input Capture" source.  Name this "Laptop Mic", or whatever mic source you want to use.

![](/img/annotation-2020-09-02-174615_orig.png#center)

Next, use the dropdown menu to select the mic you would like to use, and then hit "OK"!  Now, when you try saying something, you should see the audio levels move under your mic source.

![](/img/annotation-2020-09-02-174906_orig.png#center)

Alright, your two scenes are now set up!  If you still see a red selection square around your video, click in the gray area to the left or right of the preview pane to remove it.  Then, try out switching between "Scene" and "Scene 2" under the "Scenes" module.  If everything has been done correctly, you should be able to fade between the black screen of "Scene" and then your full screen webcam of "Scene 2".  You'll notice that the audio sources also disappear form your "Audio Mixer" panel.  Congrats, you've just created your first scene!

## 2. Setup stream to the Facebook and Youtube (Restream.io)

Now that OBS is set up, we're going to want to tell OBS where it should stream to once we click the "Start Stream".  For our purposes of streaming to both Facebook and Youtube, we will be using Restream, which takes our OBS feed and streams it out to however many platform we desire.  You can sign up for a free account [here](https://restream.io/join/E5my0) and easily connect streaming platform accounts that you already own.  Once you've signed up, you will have a blank dashboard page where you can set destinations for your stream.
This is where you can add different destination points for your stream, and there are limits to the free account.  I am personally on the Standard package, which allows me to stream to a public Facebook page, such as my church's page.  Feel free to click "+ Add Channel" and add in your personal FB page and your YT channel (YT may require you to activate livestreaming, which I believe requires a 24-hour window of time). 

For this guide, I'll be using my church's account to show what I have set up for our multi-stream.  As you can see below, I have both my church's Facebook page as well as its Youtube page assigned as destinations, and I have them both toggled to ON, so that Restream knows to stream to those platforms.  They are both marked as "Offline" because I have not started the stream yet from OBS.

![](/img/annotation-2020-09-01-213953_orig.png#center)

Next, I want to edit the titles and descriptions of these streams to suit the stream's content.  Click the "Update Titles" button, which is near the top, to the right of the lovely "+ Add Channel" button.  You should be taken to the page below.

![](/img/annotation-2020-09-01-214615_orig.png#center)

Restream conveniently lets you update all your stream titles and descriptions at once, or you can also go down to each stream and hit "EDIT" in order to give specific titles to each stream.  Try out typing in a Title and Description and clicking "Update All".  A notification should fly-in from the top right to inform you that both streams have been updated.

Great, we've got the Restream side of things set up! Now, we're going to head back to OBS and connect it to Restream.  Once you're back in the program, go to File > Settings and then click the "Stream" tab on the left.  Next to "Service", select "Restream.io" from the dropdown menu, and then click "Connect Account (recommended)".  Finishing filling in your credentials, click "Allow", and then click "OK" in the Settings window to go back to the main OBS screen.  You will be greeted with three pop-up Restream windows.

![](/img/annotation-2020-09-01-215655_orig.png#center)

As you can tell from the text within these windows, you can edit the stream title as well as toggle on/off the platforms right from within OBS, which is useful for any quick adjustments! The third chat window is for monitoring the chats that come in through your multiple platforms.  For now, exit out of the three windows (you can make them reappear by selecting them under View > Docks).

The last thing to do is to check out your stream output settings.  Head to File > Settings, click the side tab "Output", and notice the "Video Bitrate" option.  This controls how much video data OBS is pushing out, and changes the quality of your image.  Higher bitrate for the most part = higher quality.  I have mine set to 2500 kbps, but experiment with lower ones if your stream is coming out super laggy.

![](/img/annotation-2020-09-02-181133_orig.png#center)

Now click the "Video" side tab, and change your output resolution to your desired size.  This can also affect the smoothness of your stream, so experiment with different resolutions to see which suits your needs best.


Now that you're done, click "OK" to back to the main window, and then the final thing to do is to simply click "Start Streaming" under the "Controls" panel at the bottom right, and OBS will instantly start streaming to the selected platforms you selected within Restream!

Alright, you've got the stream going up to FB and YT, but what if you also happen to want to send that feed straight to Zoom webinar?

## 3. Setup stream to Zoom call/webinar (Virtualcam)

In order for Zoom to detect our OBS stream as a camera source, we're going to use a little plug-in called Virtualcam (Windows, Mac).  This lets OBS output its stream to a virtual camera, which can then be selected within Zoom.  After installing the camera, restart your OBS app and head up to Tools > Virtualcam.

![](/img/annotation-2020-09-02-175527_orig.png#center)

Notice the name of the target camera (mine is named "OBS-Camera"), and then click on "Start" in order to start the virtual cam, which will tell OBS to start streaming your feed to "OBS-Camera".  You can now close out of the window and head over to Zoom.  (You will need to start the camera each time you relaunch OBS)

Start up a new Zoom meeting, and then go to the the "^" symbol next to the "Stop Video" button (you'll want to make sure your video is on), and then select "OBS-Camera" as your new source.

![](/img/annotation-2020-09-02-175827_orig.png#center)

Your video feed should now be whatever you have shown in your OBS' preview pane.  Feel free to put OBS and Zoom side by side and watch how the feed changes when you switch between your two scenes.

![](/img/annotation-2020-09-02-180152_orig.png#center)

Whoo!  You now have your OBS feed directly going into your Zoom video source.  Remember that this is only for video, and you should still make sure you select the audio source that you want within the Zoom app.  (For those who want a solution to route OBS audio into Zoom, check out [VB-Cable](https://www.vb-audio.com/Cable/))

## 4. Record the stream

Now that you have all your stream ready to go, OBS also gives you the option of recording your stream and saving it as a video file to your local drive.  All you need to do is click Start Recording before you hit Start Streaming, and you'll see that OBS will start recording.  You can change where your recordings download to by going to File > Settings > Output, and then changing the recording path.
Alright, we've got everything set up and ready to go!  As a summary, here is the best practice that you should do every time you want to set up this specific multi stream format:

1. Launch OBS and make sure visual and audio sources are functional
2. Start Virtualcam
3. Launch Zoom and make sure the video source is set to "OBS-Camera"
4. Make sure Restream destinations are titled properly and are toggled to ON
5. Hit "Start Recording"
6. Hit "Start Streaming"

And of course, once you're done, don't forget to hit "Stop Streaming" and then "Stop Recording" to have the file save to your local folder.
Thanks for reading, and happy streaming!