---
UID: NF:vfw.StretchDIB
title: StretchDIB function (vfw.h)
description: The StretchDIB function copies a device independent bitmap from one memory location to another and resizes the image to fit the destination rectangle.
helpviewer_keywords: ["StretchDIB","StretchDIB function [Windows Multimedia]","_win32_StretchDIB","multimedia.stretchdib","vfw/StretchDIB"]
old-location: multimedia\stretchdib.htm
tech.root: Multimedia
ms.assetid: 9b542bcf-c32f-40ab-96d1-6f0d96b856c5
ms.date: 12/05/2018
ms.keywords: StretchDIB, StretchDIB function [Windows Multimedia], _win32_StretchDIB, multimedia.stretchdib, vfw/StretchDIB
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StretchDIB
 - vfw/StretchDIB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - StretchDIB
---

# StretchDIB function


## -description

The <b>StretchDIB</b> function copies a device independent bitmap from one memory location to another and resizes the image to fit the destination rectangle.

## -parameters

### -param biDst

Pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that describes the destination bitmap.

### -param lpDst

Pointer to the memory buffer that will receive the copied pixel bits.

### -param DstX

X coordinate of the destination rectangle's origin.

### -param DstY

Y coordinate of the destination rectangle's origin.

### -param DstXE

Width, in pixels, of the destination rectangle.

### -param DstYE

Height, in pixels, of the destination rectangle.

### -param biSrc

Pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that describes the source bitmap.

### -param lpSrc

Pointer to the source bitmap data.

### -param SrcX

X coordinate of the source rectangle's origin.

### -param SrcY

Y coordinate of the source rectangle's origin.

### -param SrcXE

Width, in pixels, of the source rectangle.

### -param SrcYE

Height, in pixels, of the source rectangle.

## -remarks

The size of the destination buffer must be large enough to accommodate any alignment bytes at the end of each pixel row.

This function does nothing if <i>biSrc</i> and <i>biDst</i> have different values for <i>biBitCount</i> or if the value for <i>biSrc</i>.  <i>biBitCount</i> does not equal 8, 16, or 24.

This function performs no dithering or other smoothing. Pixel values are merely dropped or duplicated on a line-by-line, column-by-column basis.

This function does not do any special processing based on pixel encoding except for calculating the number of bits per pixel. In particular this function will not generate correct results when pixels are encoded in groups of more than 1 pixel, as in the case of a YUV format where U and V are decimated and so are not represented equally in each pixel.

Before including Vfw.h, you must add the following line to your code:


```cpp

#define DRAWDIB_INCLUDE_STRETCHDIB

```