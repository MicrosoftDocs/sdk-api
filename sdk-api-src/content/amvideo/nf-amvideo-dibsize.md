---
UID: NF:amvideo.DIBSIZE
title: DIBSIZE macro (amvideo.h)
description: The DIBSIZE macro calculates the number of bytes required by a device-independent bitmap (DIB).
helpviewer_keywords: ["DIBSIZE","DIBSIZE macro [DirectShow]","amvideo/DIBSIZE","dshow.dibsize"]
old-location: dshow\dibsize.htm
tech.root: dshow
ms.assetid: a1feaa57-f403-46d0-b9a4-56e94ff2ceee
ms.date: 12/05/2018
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


## -description

The <code>DIBSIZE</code> macro calculates the number of bytes required by a device-independent bitmap (DIB).

## -parameters

### -param bi

Specifies a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

## -remarks

The size of a DIB is calculated as <code>stride * height</code>, where stride is width * bits per pixel/8, rounded up to the nearest <b>DWORD</b> alignment; and height is the absolute value of <i>biHeight</i>.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>