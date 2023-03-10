---
UID: NF:amvideo.COLORS
title: COLORS macro (amvideo.h)
description: The COLORS macro retrieves the palette entries from a VIDEOINFO structure.
helpviewer_keywords: ["COLORS","COLORS function [DirectShow]","amvideo/COLORS","dshow.colors"]
old-location: dshow\colors.htm
tech.root: dshow
ms.assetid: 32541ee4-53ef-4f0a-b823-bb475a93a195
ms.date: 12/05/2018
ms.keywords: COLORS, COLORS function [DirectShow], amvideo/COLORS, dshow.colors
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
req.lib: Strmbase.lib (retail builds); Strmbasd.lib (debug builds)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - COLORS
 - amvideo/COLORS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Strmbase.lib
 - Strmbase.dll
 - Strmbasd.lib
 - Strmbasd.dll
api_name:
 - COLORS
---

# COLORS macro


## -description

The COLORS macro retrieves the palette entries from a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.

## -remarks

This macro calculates the address as an offset from the start of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, using the value of <b>bmiHeader.biSize</b>. Make sure to initialize the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure before calling this macro.

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>