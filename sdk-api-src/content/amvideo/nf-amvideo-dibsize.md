---
UID: NF:amvideo.DIBSIZE
title: DIBSIZE macro (amvideo.h)
description: The DIBSIZE macro calculates the number of bytes required by a device-independent bitmap (DIB).
helpviewer_keywords: ["DIBSIZE","DIBSIZE macro [DirectShow]","amvideo/DIBSIZE","dshow.dibsize"]
old-location: dshow\dibsize.htm
tech.root: dshow
ms.assetid: a1feaa57-f403-46d0-b9a4-56e94ff2ceee
ms.date: 07/01/2025
ms.keywords: DIBSIZE, DIBSIZE macro [DirectShow], amvideo/DIBSIZE, dshow.dibsize
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
 - DIBSIZE
 - amvideo/DIBSIZE
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
 - DIBSIZE
---

# DIBSIZE macro

## -syntax

```cpp
DWORD DIBSIZE(
     bi
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the size in bytes.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DIBSIZE</code> macro calculates the number of bytes required by a device-independent bitmap (DIB).

## -parameters

### -param bi

Specifies a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

## -remarks

The size of a DIB is calculated as <code>stride * height</code>, where stride is width * bits per pixel/8, rounded up to the nearest <b>DWORD</b> alignment; and height is the absolute value of <i>biHeight</i>.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
