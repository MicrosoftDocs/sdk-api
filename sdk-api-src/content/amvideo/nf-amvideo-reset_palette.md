---
UID: NF:amvideo.RESET_PALETTE
title: RESET_PALETTE macro (amvideo.h)
description: The RESET_PALETTE macro fills the palette entries in a VIDEOINFO structure with zeroes.
helpviewer_keywords: ["RESET_PALETTE","RESET_PALETTE macro [DirectShow]","amvideo/RESET_PALETTE","dshow.reset_palette"]
old-location: dshow\reset_palette.htm
tech.root: dshow
ms.assetid: e981f5d4-9ad2-4e9b-8bc8-6a5e9a2fd632
ms.date: 07/01/2025
ms.keywords: RESET_PALETTE, RESET_PALETTE macro [DirectShow], amvideo/RESET_PALETTE, dshow.reset_palette
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
 - RESET_PALETTE
 - amvideo/RESET_PALETTE
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
 - RESET_PALETTE
---

# RESET_PALETTE macro

## -syntax

```cpp
void RESET_PALETTE(
    VIDEOINFO *pbmi
);
```


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RESET_PALETTE</code> macro fills the palette entries in a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure with zeroes.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
