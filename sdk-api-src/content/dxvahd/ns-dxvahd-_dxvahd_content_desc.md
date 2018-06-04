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

# _DXVAHD_CONTENT_DESC structure


## -description


Describes a video stream for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.

The display driver can use the information in this structure to optimize the capabilities of the video processor. For example, some capabilities might not be exposed for high-definition (HD) content, for performance reasons. 


## -struct-fields




### -field InputFrameFormat

A member of the <a href="https://msdn.microsoft.com/fc720dd3-e9c1-4b92-ac09-8e53cff44bec">DXVAHD_FRAME_FORMAT</a> enumeration that describes how the video stream is interlaced.


### -field InputFrameRate

The frame rate of the input video stream, specified as a <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure.


### -field InputWidth

The width of the input frames, in pixels.


### -field InputHeight

The height of the input frames, in pixels.


### -field OutputFrameRate

The frame rate of the output video stream, specified as a <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure.


### -field OutputWidth

The width of the output frames, in pixels.


### -field OutputHeight

The height of the output frames, in pixels.


## -remarks




        Frame rates are expressed as ratios. For example, 30 frames per second (fps) is expressed as 30:1, and 29.97 fps is expressed as 30000/1001. For interlaced content, a frame consists of two fields, so that the frame rate is half the field rate.
      

 If the application will composite two or more input streams, use the largest stream for the values of <b>InputWidth</b> and <b>InputHeight</b>.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

