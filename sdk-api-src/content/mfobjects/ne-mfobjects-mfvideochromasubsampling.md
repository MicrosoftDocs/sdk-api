---
UID: NE:mfobjects._MFVideoChromaSubsampling
title: MFVideoChromaSubsampling (mfobjects.h)
description: Contains flags that define the chroma encoding scheme for Y'Cb'Cr' data.
helpviewer_keywords: ["778d0456-f98e-44ac-afb7-9ce01da06741","MFVideoChromaSubsampling","MFVideoChromaSubsampling enumeration [Media Foundation]","MFVideoChromaSubsampling_Cosited","MFVideoChromaSubsampling_DV_PAL","MFVideoChromaSubsampling_ForceDWORD","MFVideoChromaSubsampling_Horizontally_Cosited","MFVideoChromaSubsampling_Last","MFVideoChromaSubsampling_MPEG1","MFVideoChromaSubsampling_MPEG2","MFVideoChromaSubsampling_ProgressiveChroma","MFVideoChromaSubsampling_Unknown","MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes","MFVideoChromaSubsampling_Vertically_Cosited","mf.mfvideochromasubsampling","mfobjects/MFVideoChromaSubsampling","mfobjects/MFVideoChromaSubsampling_Cosited","mfobjects/MFVideoChromaSubsampling_DV_PAL","mfobjects/MFVideoChromaSubsampling_ForceDWORD","mfobjects/MFVideoChromaSubsampling_Horizontally_Cosited","mfobjects/MFVideoChromaSubsampling_Last","mfobjects/MFVideoChromaSubsampling_MPEG1","mfobjects/MFVideoChromaSubsampling_MPEG2","mfobjects/MFVideoChromaSubsampling_ProgressiveChroma","mfobjects/MFVideoChromaSubsampling_Unknown","mfobjects/MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes","mfobjects/MFVideoChromaSubsampling_Vertically_Cosited"]
old-location: mf\mfvideochromasubsampling.htm
tech.root: mf
ms.assetid: 778d0456-f98e-44ac-afb7-9ce01da06741
ms.date: 12/05/2018
ms.keywords: 778d0456-f98e-44ac-afb7-9ce01da06741, MFVideoChromaSubsampling, MFVideoChromaSubsampling enumeration [Media Foundation], MFVideoChromaSubsampling_Cosited, MFVideoChromaSubsampling_DV_PAL, MFVideoChromaSubsampling_ForceDWORD, MFVideoChromaSubsampling_Horizontally_Cosited, MFVideoChromaSubsampling_Last, MFVideoChromaSubsampling_MPEG1, MFVideoChromaSubsampling_MPEG2, MFVideoChromaSubsampling_ProgressiveChroma, MFVideoChromaSubsampling_Unknown, MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes, MFVideoChromaSubsampling_Vertically_Cosited, mf.mfvideochromasubsampling, mfobjects/MFVideoChromaSubsampling, mfobjects/MFVideoChromaSubsampling_Cosited, mfobjects/MFVideoChromaSubsampling_DV_PAL, mfobjects/MFVideoChromaSubsampling_ForceDWORD, mfobjects/MFVideoChromaSubsampling_Horizontally_Cosited, mfobjects/MFVideoChromaSubsampling_Last, mfobjects/MFVideoChromaSubsampling_MPEG1, mfobjects/MFVideoChromaSubsampling_MPEG2, mfobjects/MFVideoChromaSubsampling_ProgressiveChroma, mfobjects/MFVideoChromaSubsampling_Unknown, mfobjects/MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes, mfobjects/MFVideoChromaSubsampling_Vertically_Cosited
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
targetos: Windows
req.typenames: MFVideoChromaSubsampling
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoChromaSubsampling
 - mfobjects/_MFVideoChromaSubsampling
 - MFVideoChromaSubsampling
 - mfobjects/MFVideoChromaSubsampling
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFVideoChromaSubsampling
---

# MFVideoChromaSubsampling enumeration


## -description

Contains flags that define the chroma encoding scheme for Y'Cb'Cr' data.

## -enum-fields

### -field MFVideoChromaSubsampling_Unknown:0

Unknown encoding scheme.

### -field MFVideoChromaSubsampling_ProgressiveChroma:0x8

Chroma should be reconstructed as if the underlying video was progressive content, rather than skipping fields or applying chroma filtering to minimize artifacts from reconstructing 4:2:0 interlaced chroma.

### -field MFVideoChromaSubsampling_Horizontally_Cosited:0x4

Chroma samples are aligned horizontally with the luma samples, or with multiples of the luma samples. If this flag is not set, chroma samples are located 1/2 pixel to the right of the corresponding luma sample.

### -field MFVideoChromaSubsampling_Vertically_Cosited:0x2

Chroma samples are aligned vertically with the luma samples, or with multiples of the luma samples. If this flag is not set, chroma samples are located 1/2 pixel down from the corresponding luma sample.

### -field MFVideoChromaSubsampling_Vertically_AlignedChromaPlanes:0x1

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

### -field MFVideoChromaSubsampling_ForceDWORD:0x7fffffff

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.

## -remarks

These flags are used with the <a href="/windows/desktop/medfound/mf-mt-video-chroma-siting-attribute">MF_MT_VIDEO_CHROMA_SITING</a> attribute.

For more information about these values, see the remarks for the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videochromasubsampling">DXVA2_VideoChromaSubSampling</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>
