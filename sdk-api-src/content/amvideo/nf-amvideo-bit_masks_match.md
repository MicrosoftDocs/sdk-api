---
UID: NF:amvideo.BIT_MASKS_MATCH
title: BIT_MASKS_MATCH macro (amvideo.h)
description: The BIT_MASKS_MATCH macro compares the color masks for two VIDEOINFO structures.
helpviewer_keywords: ["BIT_MASKS_MATCH","BIT_MASKS_MATCH macro [DirectShow]","amvideo/BIT_MASKS_MATCH","dshow.bit_masks_match"]
old-location: dshow\bit_masks_match.htm
tech.root: dshow
ms.assetid: 2b9d18fd-3251-4ab4-bb79-33829190f1b8
ms.date: 07/01/2025
ms.keywords: BIT_MASKS_MATCH, BIT_MASKS_MATCH macro [DirectShow], amvideo/BIT_MASKS_MATCH, dshow.bit_masks_match
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
 - BIT_MASKS_MATCH
 - amvideo/BIT_MASKS_MATCH
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
 - BIT_MASKS_MATCH
---

# BIT_MASKS_MATCH macro

## -syntax

```cpp
BOOL BIT_MASKS_MATCH(
     pbmi1,
     pbmi2
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if the color masks are identical, or **FALSE** otherwise.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>BIT_MASKS_MATCH</code> macro compares the color masks for two <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structures.

## -parameters

### -param pbmi1

Pointer to the first VIDEOINFO structure.

### -param pbmi2

Pointer to the second VIDEOINFO structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
