---
UID: NF:amvideo.MPEG1_SEQUENCE_INFO
title: MPEG1_SEQUENCE_INFO macro (amvideo.h)
description: The MPEG1_SEQUENCE_INFO macro returns the address of the sequence header inside an MPEG1VIDEOINFO structure.
helpviewer_keywords: ["MPEG1_SEQUENCE_INFO","MPEG1_SEQUENCE_INFO macro [DirectShow]","amvideo/MPEG1_SEQUENCE_INFO","dshow.mpeg1_sequence_info"]
old-location: dshow\mpeg1_sequence_info.htm
tech.root: dshow
ms.assetid: 2c3f7dd7-3437-49ab-969c-d2425a75352b
ms.date: 07/01/2025
ms.keywords: MPEG1_SEQUENCE_INFO, MPEG1_SEQUENCE_INFO macro [DirectShow], amvideo/MPEG1_SEQUENCE_INFO, dshow.mpeg1_sequence_info
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
 - MPEG1_SEQUENCE_INFO
 - amvideo/MPEG1_SEQUENCE_INFO
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
 - MPEG1_SEQUENCE_INFO
---

# MPEG1_SEQUENCE_INFO macro

## -syntax

```cpp
BYTE MPEG1_SEQUENCE_INFO(
    MPEG1VIDEOINFO *pv
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

Returns the address of the **bSequenceHeader** member of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a> structure.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MPEG1_SEQUENCE_INFO</code> macro returns the address of the sequence header inside an <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a> structure.

## -parameters

### -param pv

Pointer to an <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
