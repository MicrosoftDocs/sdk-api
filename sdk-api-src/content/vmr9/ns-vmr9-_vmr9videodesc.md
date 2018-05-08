---
UID: NS:vmr9._VMR9VideoDesc
title: "_VMR9VideoDesc"
author: windows-driver-content
description: The VMR9VideoDesc structure describes a video stream to be deinterlaced.
old-location: dshow\vmr9videodesc.htm
old-project: DirectShow
ms.assetid: af4bf46a-fae7-4485-b5fb-3fd1857f383f
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: VMR9VideoDesc, VMR9VideoDesc structure [DirectShow], VMR9VideoDescStructure, _VMR9VideoDesc, dshow.vmr9videodesc, vmr9/VMR9VideoDesc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
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
req.typenames: VMR9VideoDesc
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vmr9.h
api_name:
-	VMR9VideoDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

