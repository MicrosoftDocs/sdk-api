---
UID: NF:amvideo.RESET_HEADER
title: RESET_HEADER macro (amvideo.h)
description: The RESET_HEADER macro fills a VIDEOINFOHEADER with zeroes. You can also use this macro to clear just the VIDEOINFOHEADER portion of a VIDEOINFO structure.
helpviewer_keywords: ["RESET_HEADER","RESET_HEADER macro [DirectShow]","amvideo/RESET_HEADER","dshow.reset_header"]
old-location: dshow\reset_header.htm
tech.root: dshow
ms.assetid: bd976ff0-fbfb-4911-bee6-d53044eb3d23
ms.date: 07/01/2025
ms.keywords: RESET_HEADER, RESET_HEADER macro [DirectShow], amvideo/RESET_HEADER, dshow.reset_header
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
 - RESET_HEADER
 - amvideo/RESET_HEADER
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
 - RESET_HEADER
---

# RESET_HEADER macro

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

The <code>RESET_HEADER</code> macro fills a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> with zeroes. You can also use this macro to clear just the <b>VIDEOINFOHEADER</b> portion of a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.



This macro is equivalent to calling <b>ZeroMemory</b> with <code>sizeof(VIDEOINFOHEADER)</code>.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
