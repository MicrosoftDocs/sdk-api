---
UID: NE:codecapi.eAVEncVideoChromaResolution
title: eAVEncVideoChromaResolution (codecapi.h)
description: Specifies chroma resolution. This enumeration is used with the AVEncVideoInputChromaResolution and AVEncVideoOutputChromaResolution properties.
helpviewer_keywords: ["codecapi/eAVEncVideoChromaResolution","codecapi/eAVEncVideoChromaResolution_411","codecapi/eAVEncVideoChromaResolution_420","codecapi/eAVEncVideoChromaResolution_422","codecapi/eAVEncVideoChromaResolution_444","codecapi/eAVEncVideoChromaResolution_SameAsSource","dshow.eavencvideochromaresolution","eAVEncVideoChromaResolution","eAVEncVideoChromaResolution enumeration [DirectShow]","eAVEncVideoChromaResolutionEnumeration","eAVEncVideoChromaResolution_411","eAVEncVideoChromaResolution_420","eAVEncVideoChromaResolution_422","eAVEncVideoChromaResolution_444","eAVEncVideoChromaResolution_SameAsSource"]
old-location: dshow\eavencvideochromaresolution.htm
tech.root: dshow
ms.assetid: 63ac09a9-23bb-4d82-9699-541552e1ec90
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncVideoChromaResolution, codecapi/eAVEncVideoChromaResolution_411, codecapi/eAVEncVideoChromaResolution_420, codecapi/eAVEncVideoChromaResolution_422, codecapi/eAVEncVideoChromaResolution_444, codecapi/eAVEncVideoChromaResolution_SameAsSource, dshow.eavencvideochromaresolution, eAVEncVideoChromaResolution, eAVEncVideoChromaResolution enumeration [DirectShow], eAVEncVideoChromaResolutionEnumeration, eAVEncVideoChromaResolution_411, eAVEncVideoChromaResolution_420, eAVEncVideoChromaResolution_422, eAVEncVideoChromaResolution_444, eAVEncVideoChromaResolution_SameAsSource
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
 - eAVEncVideoChromaResolution
 - codecapi/eAVEncVideoChromaResolution
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
 - eAVEncVideoChromaResolution
---

# eAVEncVideoChromaResolution enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies chroma resolution. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoinputchromaresolution-property">AVEncVideoInputChromaResolution</a> and <a href="/windows/desktop/DirectShow/avencvideooutputchromaresolution-property">AVEncVideoOutputChromaResolution</a> properties.

## -enum-fields

### -field eAVEncVideoChromaResolution_SameAsSource:0 

Use the same chroma resolution as the input video. This flag applies to the <b>AVEncVideoOutputChromaResolution</b> property only.

### -field eAVEncVideoChromaResolution_444:1

4:4:4 (no downsampling).

### -field eAVEncVideoChromaResolution_422:2

4:2:2 (2:1 horizontal downsampling, with no vertical downsampling).

### -field eAVEncVideoChromaResolution_420:3

4:2:0 (2:1 horizontal downsampling, with 2:1 vertical downsampling).

### -field eAVEncVideoChromaResolution_411:4

4:1:1 (4:1 horizontal downsampling, with no vertical downsampling).

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
