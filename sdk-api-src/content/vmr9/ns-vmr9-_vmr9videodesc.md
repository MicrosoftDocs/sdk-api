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

# _VMR9VideoDesc structure


## -description



The <code>VMR9VideoDesc</code> structure describes a video stream to be deinterlaced.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwSampleWidth

Width of the video to be deinterlaced, in pixels.


### -field dwSampleHeight

Height of the video to be deinterlaced, in pixels.


### -field SampleFormat

Specifies the interlacing format of the sample, as a member of the <a href="https://msdn.microsoft.com/0e501c05-91ac-4594-bdfe-e8b4bfeb5bcb">VMR9_SampleFormat</a> enumeration.


### -field dwFourCC

Specifies the FOURCC code. Valid values include NV12, YV12, YUY2, UYVY, IMC1, IMC2, IMC3 and IMC4


### -field InputSampleFreq


              A <a href="https://msdn.microsoft.com/a2d19dcf-521e-4df0-8e28-5561f2617411">VMR9Frequency</a> structure that specifies the input frequency. For NTSC TV, the frequency would be expressed as 30,000:1001.


### -field OutputFrameFreq

A <a href="https://msdn.microsoft.com/fb4c094a-2760-45b2-b494-a44d5493987f">VMRFrequency</a> structure that specifies the output frequency. For NTSC TV, the frequency would be expressed as 60,000:1001.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>
 

 

