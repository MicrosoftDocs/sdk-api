---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagCapStatus structure


## -description



The <b>CAPSTATUS</b> structure defines the current state of the capture window.




## -struct-fields




### -field uiImageWidth

Image width, in pixels.


### -field uiImageHeight

Image height, in pixels


### -field fLiveWindow

Live window flag. The value of this member is <b>TRUE</b> if the window is displaying video using the preview method.


### -field fOverlayWindow

Overlay window flag. The value of this member is <b>TRUE</b> if the window is displaying video using hardware overlay.


### -field fScale

Input scaling flag. The value of this member is <b>TRUE</b> if the window is scaling the input video to the client area when displaying video using preview. This parameter has no effect when displaying video using overlay.


### -field ptScroll

The x- and y-offset of the pixel displayed in the upper left corner of the client area of the window.


### -field fUsingDefaultPalette

Default palette flag. The value of this member is <b>TRUE</b> if the capture driver is using its default palette.


### -field fAudioHardware

Audio hardware flag. The value of this member is <b>TRUE</b> if the system has waveform-audio hardware installed.


### -field fCapFileExists

Capture file flag. The value of this member is <b>TRUE</b> if a valid capture file has been generated.


### -field dwCurrentVideoFrame

Number of frames processed during the current (or most recent) streaming capture. This count includes dropped frames.


### -field dwCurrentVideoFramesDropped

Number of frames dropped during the current (or most recent) streaming capture. Dropped frames occur when the capture rate exceeds the rate at which frames can be saved to file. In this case, the capture driver has no buffers available for storing data. Dropping frames does not affect synchronization because the previous frame is displayed in place of the dropped frame.


### -field dwCurrentWaveSamples

Number of waveform-audio samples processed during the current (or most recent) streaming capture.


### -field dwCurrentTimeElapsedMS

Time, in milliseconds, since the start of the current (or most recent) streaming capture.


### -field hPalCurrent

Handle to current palette.


### -field fCapturingNow

Capturing flag. The value of this member is <b>TRUE</b> when capturing is in progress.


### -field dwReturn

Error return values. Use this member if your application does not support an error callback function.


### -field wNumVideoAllocated

Number of video buffers allocated. This value might be less than the number specified in the <b>wNumVideoRequested</b> member of the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure.


### -field wNumAudioAllocated

Number of audio buffers allocated. This value might be less than the number specified in the <b>wNumAudioRequested</b> member of the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure.


## -remarks



Because the state of a capture window changes in response to various messages, an application should update the information in this structure whenever it needs to enable menu items, determine the actual state of the capture window, or call the video format dialog box. If the application yields during streaming capture, this structure returns the progress of the capture in the <b>dwCurrentVideoFrame</b>, <b>dwCurrentVideoFramesDropped</b>, dwCurre<b></b>ntWaveSamples, and <b>dwCurrentTimeElapsedMS</b> members. Use the <a href="https://msdn.microsoft.com/31349599-a52c-45ba-8f08-91008773f317">WM_CAP_GET_STATUS</a> message or <a href="https://msdn.microsoft.com/5c974707-b6ca-4177-a262-6838d308fb0a">capGetStatus</a> macro to update the contents of this structure.




## -see-also




<a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a>



Video Capture



<a href="https://msdn.microsoft.com/180010d2-240e-433d-b306-341b9b1e0b57">Video Capture Structures</a>



<a href="https://msdn.microsoft.com/31349599-a52c-45ba-8f08-91008773f317">WM_CAP_GET_STATUS</a>
 

 

