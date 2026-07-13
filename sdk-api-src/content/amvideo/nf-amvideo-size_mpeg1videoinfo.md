---
UID: NF:amvideo.SIZE_MPEG1VIDEOINFO
title: SIZE_MPEG1VIDEOINFO macro (amvideo.h)
description: The SIZE_MPEG1VIDEOINFO macro calculates the size of an MPEG1VIDEOINFO structure, including the sequence header (bSequenceHeader).
helpviewer_keywords: ["SIZE_MPEG1VIDEOINFO","SIZE_MPEG1VIDEOINFO macro [DirectShow]","amvideo/SIZE_MPEG1VIDEOINFO","dshow.size_mpeg1videoinfo"]
old-location: dshow\size_mpeg1videoinfo.htm
tech.root: dshow
ms.assetid: 192c9179-baed-4fa5-a972-34964a6bdfd7
ms.date: 07/01/2025
ms.keywords: SIZE_MPEG1VIDEOINFO, SIZE_MPEG1VIDEOINFO macro [DirectShow], amvideo/SIZE_MPEG1VIDEOINFO, dshow.size_mpeg1videoinfo
req.header: amvideo.h
req.include-header: Streams.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SIZE_MPEG1VIDEOINFO
 - amvideo/SIZE_MPEG1VIDEOINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Amvideo.h
api_name:
 - SIZE_MPEG1VIDEOINFO
---

# SIZE_MPEG1VIDEOINFO macro

## -syntax

```cpp
LONG SIZE_MPEG1VIDEOINFO(
    MPEG1VIDEOINFO *pv
);
```

## -returns

Type: **LONG**

Returns the byte size of the specified <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a> structure.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SIZE_MPEG1VIDEOINFO</code> macro calculates the size of an <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a> structure, including the sequence header (<b>bSequenceHeader</b>).

## -parameters

### -param pv

Pointer to an <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
