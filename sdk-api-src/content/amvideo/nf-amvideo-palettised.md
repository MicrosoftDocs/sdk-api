---
UID: NF:amvideo.PALETTISED
title: PALETTISED macro (amvideo.h)
description: The PALETTISED macro checks whether a bitmap has a color depth of 8 bits or less.
helpviewer_keywords: ["PALETTISED","PALETTISED macro [DirectShow]","amvideo/PALETTISED","dshow.palettised"]
old-location: dshow\palettised.htm
tech.root: dshow
ms.assetid: 0f233f6f-ed52-4b32-8766-42e2416b6fc5
ms.date: 07/01/2025
ms.keywords: PALETTISED, PALETTISED macro [DirectShow], amvideo/PALETTISED, dshow.palettised
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
 - PALETTISED
 - amvideo/PALETTISED
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
 - PALETTISED
---

# PALETTISED macro

## -syntax

```cpp
BOOL PALETTISED(
    VIDEOINFOHEADER *pbmi
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the color depth (**bmiHeader.biBitCount**) is 8 bits or less, or **FALSE** otherwise.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PALETTISED</code> macro checks whether a bitmap has a color depth of 8 bits or less.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/containspalette">ContainsPalette</a>



<a href="/windows/desktop/api/amvideo/nf-amvideo-palette_entries">PALETTE_ENTRIES</a>



<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
