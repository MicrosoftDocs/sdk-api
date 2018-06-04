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

# _MFVideoChromaSubsampling enumeration


## -description



Contains flags that define the chroma encoding scheme for Y'Cb'Cr' data.




## -enum-fields




### -field MFVideoChromaSubsampling_Unknown

Unknown encoding scheme.


### -field MFVideoChromaSubsampling_ProgressiveChroma

Chroma should be reconstructed as if the underlying video was progressive content, rather than skipping fields or applying chroma filtering to minimize artifacts from reconstructing 4:2:0 interlaced chroma.


### -field MFVideoChromaSubsampling_Horizontally_Cosited

Chroma samples are aligned horizontally with the luma samples, or with multiples of the luma samples. If this flag is not set, chroma samples are located 1/2 pixel to the right of the corresponding luma sample.


### -field MFVideoChromaSubsampling_Vertically_Cosited

Chroma samples are aligned vertically with the luma samples, or with multiples of the luma samples. If this flag is not set, chroma samples are located 1/2 pixel down from the corresponding luma sample.


### -field MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes

The U and V planes are aligned vertically. If this flag is not set, the chroma planes are assumed to be out of phase by 1/2 chroma sample, alternating between a line of U followed by a line of V.


### -field MFVideoChromaSubsampling_MPEG2

Specifies the chroma encoding scheme for MPEG-2 video. Chroma samples are aligned horizontally with the luma samples, but are not aligned vertically. The U and V planes are aligned vertically.


### -field MFVideoChromaSubsampling_MPEG1

Specifies the chroma encoding scheme for MPEG-1 video.


### -field MFVideoChromaSubsampling_DV_PAL

Specifies the chroma encoding scheme for PAL DV video.


### -field MFVideoChromaSubsampling_Cosited

Chroma samples are aligned vertically and horizontally with the luma samples. YUV formats such as 4:4:4, 4:2:2, and 4:1:1 are always cosited in both directions and should use this flag.


### -field MFVideoChromaSubsampling_Last

Reserved.


### -field MFVideoChromaSubsampling_ForceDWORD

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.


## -remarks



These flags are used with the <a href="https://msdn.microsoft.com/0c930348-8669-42cc-9d74-df9ef475bdc8">MF_MT_VIDEO_CHROMA_SITING</a> attribute.

For more information about these values, see the remarks for the <a href="https://msdn.microsoft.com/0f9d63fd-46fa-498c-8703-1beeaf09ce86">DXVA2_VideoChromaSubSampling</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

