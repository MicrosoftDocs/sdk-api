---
UID: NE:mfobjects._MFVideoInterlaceMode
title: MFVideoInterlaceMode (mfobjects.h)
author: windows-sdk-content
description: Specifies how a video stream is interlaced.
old-location: mf\mfvideointerlacemode.htm
tech.root: medfound
ms.assetid: 10a3d7b1-74ed-46cd-b10e-59a8f01726d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 10a3d7b1-74ed-46cd-b10e-59a8f01726d5, MFVideoInterlaceMode, MFVideoInterlaceMode enumeration [Media Foundation], MFVideoInterlace_FieldInterleavedLowerFirst, MFVideoInterlace_FieldInterleavedUpperFirst, MFVideoInterlace_FieldSingleLower, MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_ForceDWORD, MFVideoInterlace_Last, MFVideoInterlace_MixedInterlaceOrProgressive, MFVideoInterlace_Progressive, MFVideoInterlace_Unknown, mf.mfvideointerlacemode, mfobjects/MFVideoInterlaceMode, mfobjects/MFVideoInterlace_FieldInterleavedLowerFirst, mfobjects/MFVideoInterlace_FieldInterleavedUpperFirst, mfobjects/MFVideoInterlace_FieldSingleLower, mfobjects/MFVideoInterlace_FieldSingleUpper, mfobjects/MFVideoInterlace_ForceDWORD, mfobjects/MFVideoInterlace_Last, mfobjects/MFVideoInterlace_MixedInterlaceOrProgressive, mfobjects/MFVideoInterlace_Progressive, mfobjects/MFVideoInterlace_Unknown
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
 - MFVideoInterlaceMode
product: Windows
targetos: Windows
req.typenames: MFVideoInterlaceMode
req.redist: 
ms.custom: 19H1
---

# MFVideoInterlaceMode enumeration


## -description


Specifies how a video stream is interlaced.

In the descriptions that follow, upper field refers to the field that contains the leading half scan line. Lower field refers to the field that contains the first full scan line.


## -enum-fields




### -field MFVideoInterlace_Unknown

The type of interlacing is not known.
          


### -field MFVideoInterlace_Progressive

Progressive frames.
          


### -field MFVideoInterlace_FieldInterleavedUpperFirst

Interlaced frames. Each frame contains two fields. The field lines are interleaved, with the upper field appearing on the first line.
          


### -field MFVideoInterlace_FieldInterleavedLowerFirst

Interlaced frames. Each frame contains two fields. The field lines are interleaved, with the lower field appearing on the first line.
          


### -field MFVideoInterlace_FieldSingleUpper

Interlaced frames. Each frame contains one field, with the upper field appearing first.
          


### -field MFVideoInterlace_FieldSingleLower

Interlaced frames. Each frame contains one field, with the lower field appearing first.
          


### -field MFVideoInterlace_MixedInterlaceOrProgressive

The stream contains a mix of interlaced and progressive modes.
          


### -field MFVideoInterlace_Last

Reserved.
          


### -field MFVideoInterlace_ForceDWORD

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.
          


## -remarks



Scan lines in the lower field are 0.5 scan line lower than those in the upper field. In NTSC television, a frame consists of a lower field followed by an upper field. In PAL television, a frame consists of an upper field followed by a lower field.

The upper field is also called the even field, the top field, or field 2. The lower field is also called the odd field, the bottom field, or field 1.

If the interlace mode is MFVideoInterlace_FieldSingleUpper or MFVideoInterlace_FieldSingleLower, each sample contains a single field, so each buffer contains only half the number of field lines given in the media type.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-interlace-mode-attribute">MF_MT_INTERLACE_MODE</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/video-interlacing">Video Interlacing</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/video-media-types">Video Media Types</a>
 

 

