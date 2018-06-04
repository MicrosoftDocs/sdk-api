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

# _MFMPEG2DLNASINKSTATS structure


## -description


Contains encoding statistics from the Digital Living Network Alliance (DLNA) media sink.

This structure is used with the <a href="https://msdn.microsoft.com/1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35">MF_MP2DLNA_STATISTICS</a> attribute.


## -struct-fields




### -field cBytesWritten

Total number of bytes written to the byte stream.


### -field fPAL

If <b>TRUE</b>, the video stream is a PAL format. Otherwise, the video stream is an NTSC format.


### -field fccVideo

A FOURCC code that specifies the video format.


### -field dwVideoWidth

The width of the video frame, in pixels.


### -field dwVideoHeight

The height of the video frame, in pixels.


### -field cVideoFramesReceived

The number of video frames received.


### -field cVideoFramesEncoded

The number of video frames that have been encoded.


### -field cVideoFramesSkipped

The number of video frames that have been skipped.


### -field cBlackVideoFramesEncoded

The number of black frames that have been encoded.


### -field cVideoFramesDuplicated

The number of duplicated video frames.


### -field cAudioSamplesPerSec

The audio sample rate, in samples per second.


### -field cAudioChannels

The number of audio channels.


### -field cAudioBytesReceived

The total amount of audio data received, in bytes.


### -field cAudioFramesEncoded

The number of audio frames that have been encoded.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

