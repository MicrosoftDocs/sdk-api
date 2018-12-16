---
UID: NE:mfobjects._MFVideoChromaSubsampling
title: MFVideoChromaSubsampling
author: windows-sdk-content
description: Contains flags that define the chroma encoding scheme for Y'Cb'Cr' data.
old-location: mf\mfvideochromasubsampling.htm
tech.root: medfound
ms.assetid: 778d0456-f98e-44ac-afb7-9ce01da06741
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 778d0456-f98e-44ac-afb7-9ce01da06741, MFVideoChromaSubsampling, MFVideoChromaSubsampling enumeration [Media Foundation], MFVideoChromaSubsampling_Cosited, MFVideoChromaSubsampling_DV_PAL, MFVideoChromaSubsampling_ForceDWORD, MFVideoChromaSubsampling_Horizontally_Cosited, MFVideoChromaSubsampling_Last, MFVideoChromaSubsampling_MPEG1, MFVideoChromaSubsampling_MPEG2, MFVideoChromaSubsampling_ProgressiveChroma, MFVideoChromaSubsampling_Unknown, MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes, MFVideoChromaSubsampling_Vertically_Cosited, mf.mfvideochromasubsampling, mfobjects/MFVideoChromaSubsampling, mfobjects/MFVideoChromaSubsampling_Cosited, mfobjects/MFVideoChromaSubsampling_DV_PAL, mfobjects/MFVideoChromaSubsampling_ForceDWORD, mfobjects/MFVideoChromaSubsampling_Horizontally_Cosited, mfobjects/MFVideoChromaSubsampling_Last, mfobjects/MFVideoChromaSubsampling_MPEG1, mfobjects/MFVideoChromaSubsampling_MPEG2, mfobjects/MFVideoChromaSubsampling_ProgressiveChroma, mfobjects/MFVideoChromaSubsampling_Unknown, mfobjects/MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes, mfobjects/MFVideoChromaSubsampling_Vertically_Cosited
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfobjects.h
api_name:
 - MFVideoChromaSubsampling
product: Windows
targetos: Windows
req.typenames: MFVideoChromaSubsampling
req.redist: 
---

# MFVideoChromaSubsampling enumeration


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
 

 

