---
UID: NE:strmif.tagVideoProcAmpFlags
title: VideoProcAmpFlags (strmif.h)
description: The VideoProcAmpFlags enumeration indicates whether a particular video property is controlled manually or automatically.
helpviewer_keywords: ["VideoProcAmpFlags","VideoProcAmpFlags enumeration [DirectShow]","VideoProcAmpFlagsEnumeration","VideoProcAmp_Flags_Auto","VideoProcAmp_Flags_Manual","dshow.videoprocampflags","strmif/VideoProcAmpFlags","strmif/VideoProcAmp_Flags_Auto","strmif/VideoProcAmp_Flags_Manual"]
old-location: dshow\videoprocampflags.htm
tech.root: dshow
ms.assetid: 42876f3b-d2b9-4ddb-85c0-80f5177eef6b
ms.date: 4/26/2023
ms.keywords: VideoProcAmpFlags, VideoProcAmpFlags enumeration [DirectShow], VideoProcAmpFlagsEnumeration, VideoProcAmp_Flags_Auto, VideoProcAmp_Flags_Manual, dshow.videoprocampflags, strmif/VideoProcAmpFlags, strmif/VideoProcAmp_Flags_Auto, strmif/VideoProcAmp_Flags_Manual
req.header: strmif.h
req.include-header: Dshow.h
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
targetos: Windows
req.typenames: VideoProcAmpFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVideoProcAmpFlags
 - strmif/tagVideoProcAmpFlags
 - VideoProcAmpFlags
 - strmif/VideoProcAmpFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VideoProcAmpFlags
---

# VideoProcAmpFlags enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VideoProcAmpFlags</b> enumeration indicates whether a particular video property is controlled manually or automatically.

## -enum-fields

### -field VideoProcAmp_Flags_Auto:0x1

The setting is controlled automatically.

### -field VideoProcAmp_Flags_Manual:0x2

The setting is controlled manually.

## -remarks

The following flags defined in KsMedia.h are equivalent to the values in <b>VideoProcAmpFlags</b>:


``` syntax
#define KSPROPERTY_VIDEOPROCAMP_FLAGS_AUTO        0X0001L
#define KSPROPERTY_VIDEOPROCAMP_FLAGS_MANUAL      0X0002L
```


## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>
