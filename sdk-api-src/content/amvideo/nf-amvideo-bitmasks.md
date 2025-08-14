---
UID: NF:amvideo.BITMASKS
title: BITMASKS macro (amvideo.h)
description: The BITMASKS macro retrieves the color masks from a VIDEOINFO structure.
helpviewer_keywords: ["BITMASKS","BITMASKS macro [DirectShow]","amvideo/BITMASKS","dshow.bitmasks"]
old-location: dshow\bitmasks.htm
tech.root: dshow
ms.assetid: e90ddeab-a3d6-4d34-8608-4d8831d81fe5
ms.date: 07/01/2025
ms.keywords: BITMASKS, BITMASKS macro [DirectShow], amvideo/BITMASKS, dshow.bitmasks
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
 - BITMASKS
 - amvideo/BITMASKS
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
 - BITMASKS
---

# BITMASKS macro

## -syntax

```cpp
DWORD BITMASKS(
     pbmi
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a **DWORD** pointer value that is the address of the **dwBitMasks** member of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>BITMASKS</code> macro retrieves the color masks from a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.

## -remarks

This macro calculates the address as an offset from the start of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, using the value of <b>bmiHeader.biSize</b>. Make sure to initialize the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure before calling this macro.

You can access the color masks in the array using the following constants, defined in Amvideo.h:

<pre class="syntax" xml:space="preserve"><code>#define iRED   0
#define iGREEN 1
#define iBLUE  2  </code></pre>

#### Examples


```
VIDEOINFO *pVi;

/* Initialize pVi (not shown). */

DWORD dwRed   = BITMASKS(pVi)[iRED];
DWORD dwGreen = BITMASKS(pVi)[iGREEN]; 
DWORD dwBlue  = BITMASKS(pVi)[iBLUE];
```

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
