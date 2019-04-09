---
UID: NS:vmr9._VMR9VideoDesc
title: VMR9VideoDesc (vmr9.h)
author: windows-sdk-content
description: The VMR9VideoDesc structure describes a video stream to be deinterlaced.
old-location: dshow\vmr9videodesc.htm
tech.root: DirectShow
ms.assetid: af4bf46a-fae7-4485-b5fb-3fd1857f383f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VMR9VideoDesc, VMR9VideoDesc structure [DirectShow], VMR9VideoDescStructure, dshow.vmr9videodesc, vmr9/VMR9VideoDesc
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9VideoDesc
product: Windows
targetos: Windows
req.typenames: VMR9VideoDesc
req.redist: 
---

# VMR9VideoDesc structure


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

Specifies the interlacing format of the sample, as a member of the <a href="https://msdn.microsoft.com/en-us/library/Dd407379(v=VS.85).aspx">VMR9_SampleFormat</a> enumeration.


### -field dwFourCC

Specifies the FOURCC code. Valid values include NV12, YV12, YUY2, UYVY, IMC1, IMC2, IMC3 and IMC4


### -field InputSampleFreq

A <a href="https://msdn.microsoft.com/en-us/library/Dd407365(v=VS.85).aspx">VMR9Frequency</a> structure that specifies the input frequency. For NTSC TV, the frequency would be expressed as 30,000:1001.


### -field OutputFrameFreq

A <a href="https://msdn.microsoft.com/en-us/library/Dd407385(v=VS.85).aspx">VMRFrequency</a> structure that specifies the output frequency. For NTSC TV, the frequency would be expressed as 60,000:1001.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/31d59f17-552b-46d1-89e4-751216f54280">Setting Deinterlace Preferences</a>
 

 

