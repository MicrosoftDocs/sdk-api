---
UID: NS:amvideo.tagAnalogVideoInfo
title: ANALOGVIDEOINFO (amvideo.h)
description: The ANALOGVIDEOINFO structure maintains information about the format of the analog video signal.
helpviewer_keywords: ["ANALOGVIDEOINFO","ANALOGVIDEOINFO structure [DirectShow]","ANALOGVIDEOINFOStructure","amvideo/ANALOGVIDEOINFO","dshow.analogvideoinfo"]
old-location: dshow\analogvideoinfo.htm
tech.root: dshow
ms.assetid: c0c568ce-6834-4bfe-aaae-addfbc0218bd
ms.date: 4/26/2023
ms.keywords: ANALOGVIDEOINFO, ANALOGVIDEOINFO structure [DirectShow], ANALOGVIDEOINFOStructure, amvideo/ANALOGVIDEOINFO, dshow.analogvideoinfo
req.header: amvideo.h
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
req.typenames: ANALOGVIDEOINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAnalogVideoInfo
 - amvideo/tagAnalogVideoInfo
 - ANALOGVIDEOINFO
 - amvideo/ANALOGVIDEOINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - ANALOGVIDEOINFO
---

# ANALOGVIDEOINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ANALOGVIDEOINFO</b> structure maintains information about the format of the analog video signal.

## -struct-fields

### -field rcSource

Source video rectangle.

### -field rcTarget

Destination target rectangle.

### -field dwActiveWidth

Source video width.

### -field dwActiveHeight

Source video height (483 for NTSC, 575 for PAL/SECAM).

### -field AvgTimePerFrame

Average time per frame in 100-nanosecond units.

## -remarks

Filters using this format usually pass the video signal using a hardware-based connection rather than using memory-based transports.

An example of a definition of an analog video media type connection would be a connection of NTSC video using "M" color encoding. This would use a major media type of MEDIATYPE_AnalogVideo, a subtype of MEDIASUBTYPE_AnalogVideo_NTSC_M, and a format type of FORMAT_AnalogVideo.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>