---
UID: NE:mfobjects._MFNominalRange
title: MFNominalRange (mfobjects.h)
description: Specifies whether color data includes headroom and toeroom.
helpviewer_keywords: ["MFNominalRange","MFNominalRange enumeration [Media Foundation]","MFNominalRange_0_255","MFNominalRange_16_235","MFNominalRange_48_208","MFNominalRange_64_127","MFNominalRange_Normal","MFNominalRange_Unknown","MFNominalRange_Wide","fe7547f8-84cd-461a-8d33-dbc0b90add37","mf.mfnominalrange","mfobjects/MFNominalRange","mfobjects/MFNominalRange_0_255","mfobjects/MFNominalRange_16_235","mfobjects/MFNominalRange_48_208","mfobjects/MFNominalRange_64_127","mfobjects/MFNominalRange_Normal","mfobjects/MFNominalRange_Unknown","mfobjects/MFNominalRange_Wide"]
old-location: mf\mfnominalrange.htm
tech.root: mf
ms.assetid: fe7547f8-84cd-461a-8d33-dbc0b90add37
ms.date: 12/05/2018
ms.keywords: MFNominalRange, MFNominalRange enumeration [Media Foundation], MFNominalRange_0_255, MFNominalRange_16_235, MFNominalRange_48_208, MFNominalRange_64_127, MFNominalRange_Normal, MFNominalRange_Unknown, MFNominalRange_Wide, fe7547f8-84cd-461a-8d33-dbc0b90add37, mf.mfnominalrange, mfobjects/MFNominalRange, mfobjects/MFNominalRange_0_255, mfobjects/MFNominalRange_16_235, mfobjects/MFNominalRange_48_208, mfobjects/MFNominalRange_64_127, mfobjects/MFNominalRange_Normal, mfobjects/MFNominalRange_Unknown, mfobjects/MFNominalRange_Wide
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
req.typenames: MFNominalRange
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFNominalRange
 - mfobjects/_MFNominalRange
 - MFNominalRange
 - mfobjects/MFNominalRange
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
 - MFNominalRange
---

# MFNominalRange enumeration


## -description

Specifies whether color data includes headroom and toeroom. Headroom allows for values beyond 1.0 white ("whiter than white"), and toeroom allows for values below reference 0.0 black ("blacker than black").

## -enum-fields

### -field MFNominalRange_Unknown:0

Unknown nominal range.

### -field MFNominalRange_Normal:1

Equivalent to MFNominalRange_0_255.

### -field MFNominalRange_Wide:2

Equivalent to MFNominalRange_16_235.

### -field MFNominalRange_0_255:1

The normalized range [0...1] maps to [0...255] for 8-bit samples or [0...1023] for 10-bit samples.

### -field MFNominalRange_16_235:2

The normalized range [0...1] maps to [16...235] for 8-bit samples or [64...940] for 10-bit samples.

### -field MFNominalRange_48_208:3

The normalized range [0..1] maps to [48...208] for 8-bit samples or [64...940] for 10-bit samples.

### -field MFNominalRange_64_127:4

The normalized range [0..1] maps to [64...127] for 8-bit samples or [256...508] for 10-bit samples. This range is used in the xRGB color space.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MFNominalRange_Last

### -field MFNominalRange_ForceDWORD:0x7fffffff

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-mt-video-nominal-range-attribute">MF_MT_VIDEO_NOMINAL_RANGE</a> attribute.
      

For more information about these values, see the remarks for the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_nominalrange">DXVA2_NominalRange</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>
