---
UID: NF:amvideo.HEADER
title: HEADER macro (amvideo.h)
description: The HEADER macro returns the address of the BITMAPINFOHEADER within a VIDEOINFOHEADER.
helpviewer_keywords: ["HEADER","HEADER macro [DirectShow]","amvideo/HEADER","dshow.header"]
old-location: dshow\header.htm
tech.root: dshow
ms.assetid: 5263f924-6f82-4d64-8dc7-0b5e7efa4150
ms.date: 07/01/2025
ms.keywords: HEADER, HEADER macro [DirectShow], amvideo/HEADER, dshow.header
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
 - HEADER
 - amvideo/HEADER
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
 - HEADER
---

# HEADER macro

## -syntax

```cpp
BITMAPINFOHEADER HEADER(
    VIDEOINFOHEADER *pVideoInfo
);
```

## -returns

Type: **BITMAPINFOHEADER**

Returns the address of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure's **bmiHeader** member.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>HEADER</b> macro returns the address of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> within a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a>.

## -parameters

### -param pVideoInfo

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
