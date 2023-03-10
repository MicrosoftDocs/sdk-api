---
UID: NS:wingdi.tagRGBQUAD
title: RGBQUAD (wingdi.h)
description: The RGBQUAD structure describes a color consisting of relative intensities of red, green, and blue.
helpviewer_keywords: ["*LPRGBQUAD","RGBQUAD","RGBQUAD structure [Windows GDI]","_win32_RGBQUAD_str","gdi.rgbquad","tagRGBQUAD","wingdi/RGBQUAD"]
old-location: gdi\rgbquad.htm
tech.root: gdi
ms.assetid: 22e0991d-078e-4b44-9f03-004137e31f6c
ms.date: 12/05/2018
ms.keywords: '*LPRGBQUAD, RGBQUAD, RGBQUAD structure [Windows GDI], _win32_RGBQUAD_str, gdi.rgbquad, tagRGBQUAD, wingdi/RGBQUAD'
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RGBQUAD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRGBQUAD
 - wingdi/tagRGBQUAD
 - RGBQUAD
 - wingdi/RGBQUAD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RGBQUAD
---

# RGBQUAD structure


## -description

The <b>RGBQUAD</b> structure describes a color consisting of relative intensities of red, green, and blue.

## -struct-fields

### -field rgbBlue

The intensity of blue in the color.

### -field rgbGreen

The intensity of green in the color.

### -field rgbRed

The intensity of red in the color.

### -field rgbReserved

This member is reserved and must be zero.

## -remarks

The <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure consists of an array of <b>RGBQUAD</b> structures.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibitstodevice">SetDIBitsToDevice</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>