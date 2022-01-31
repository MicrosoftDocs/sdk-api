---
UID: NE:codecapi.eAVEncVideoColorNominalRange
title: eAVEncVideoColorNominalRange (codecapi.h)
description: Specifies the nominal range for a video source. This enumeration is used with the AVEncVideoInputChromaSubsampling and AVEncVideoOutputChromaSubsampling properties.
helpviewer_keywords: ["codecapi/eAVEncVideoColorNominalRange","codecapi/eAVEncVideoColorNominalRange_0_255","codecapi/eAVEncVideoColorNominalRange_16_235","codecapi/eAVEncVideoColorNominalRange_48_208","codecapi/eAVEncVideoColorNominalRange_SameAsSource","dshow.eavencvideocolornominalrange","eAVEncVideoColorNominalRange","eAVEncVideoColorNominalRange enumeration [DirectShow]","eAVEncVideoColorNominalRangeEnumeration","eAVEncVideoColorNominalRange_0_255","eAVEncVideoColorNominalRange_16_235","eAVEncVideoColorNominalRange_48_208","eAVEncVideoColorNominalRange_SameAsSource"]
old-location: dshow\eavencvideocolornominalrange.htm
tech.root: dshow
ms.assetid: e3f49d42-b683-463b-8e09-9497a9bfad25
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoColorNominalRange, codecapi/eAVEncVideoColorNominalRange_0_255, codecapi/eAVEncVideoColorNominalRange_16_235, codecapi/eAVEncVideoColorNominalRange_48_208, codecapi/eAVEncVideoColorNominalRange_SameAsSource, dshow.eavencvideocolornominalrange, eAVEncVideoColorNominalRange, eAVEncVideoColorNominalRange enumeration [DirectShow], eAVEncVideoColorNominalRangeEnumeration, eAVEncVideoColorNominalRange_0_255, eAVEncVideoColorNominalRange_16_235, eAVEncVideoColorNominalRange_48_208, eAVEncVideoColorNominalRange_SameAsSource
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVEncVideoColorNominalRange
 - codecapi/eAVEncVideoColorNominalRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorNominalRange
---

# eAVEncVideoColorNominalRange enumeration


## -description

Specifies the nominal range for a video source. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoinputchromasubsampling-property">AVEncVideoInputChromaSubsampling</a> and <a href="/windows/desktop/DirectShow/avencvideooutputchromasubsampling-property">AVEncVideoOutputChromaSubsampling</a> properties.



The nominal range describes how luma components normalized to a range of [0..1] map to 8-bit or 10-bit samples. The mapping determines whether the color data includes headroom and toeroom. Headroom allows for values beyond 1.0 white ("whiter than white"), and toeroom allows for values below reference 0.0 black ("blacker than black").

## -enum-fields

### -field eAVEncVideoColorNominalRange_SameAsSource:0

Use the same nominal range as the input video. This flag applies to the <b>AVEncVideoOutputChromaSubsampling</b> property only.

### -field eAVEncVideoColorNominalRange_0_255:1

The normalized range [0..1] maps to [0...255] for 8-bit samples, or [0..1023] for 10-bit samples.

### -field eAVEncVideoColorNominalRange_16_235:2

The normalized range [0..1] maps to [16...235] for 8-bit samples, or [64..940] for 10-bit samples.

### -field eAVEncVideoColorNominalRange_48_208:3   

The normalized range [0..1] maps to [48...208] for 8-bit samples.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
