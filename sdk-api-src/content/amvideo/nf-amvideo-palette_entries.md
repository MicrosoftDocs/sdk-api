---
UID: NF:amvideo.PALETTE_ENTRIES
title: PALETTE_ENTRIES macro (amvideo.h)
description: The PALETTE_ENTRIES macro retrieves the maximum number of colors in the palette of a specified bitmap.
helpviewer_keywords: ["PALETTE_ENTRIES","PALETTE_ENTRIES macro [DirectShow]","amvideo/PALETTE_ENTRIES","dshow.palette_entries"]
old-location: dshow\palette_entries.htm
tech.root: dshow
ms.assetid: 7923b767-2b38-4aa8-bbc2-21d0254bdbd9
ms.date: 07/01/2025
ms.keywords: PALETTE_ENTRIES, PALETTE_ENTRIES macro [DirectShow], amvideo/PALETTE_ENTRIES, dshow.palette_entries
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
 - PALETTE_ENTRIES
 - amvideo/PALETTE_ENTRIES
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
 - PALETTE_ENTRIES
---

# PALETTE_ENTRIES macro

## -syntax

```cpp
DWORD PALETTE_ENTRIES(
    VIDEOINFOHEADER *pbmi
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns 2 raised to the power of the color depth; that is, 1 << **bmiHeader.biBitCount**.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>PALETTE_ENTRIES</b> macro retrieves the maximum number of colors in the palette of a specified bitmap.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
