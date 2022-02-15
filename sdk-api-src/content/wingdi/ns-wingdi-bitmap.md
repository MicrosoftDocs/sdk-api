---
UID: NS:wingdi.tagBITMAP
title: BITMAP (wingdi.h)
description: The BITMAP structure defines the type, width, height, color format, and bit values of a bitmap.
helpviewer_keywords: ["*LPBITMAP","*NPBITMAP","*PBITMAP","BITMAP","BITMAP structure [Windows GDI]","PBITMAP","PBITMAP structure pointer [Windows GDI]","_win32_BITMAP_str","gdi.bitmap","wingdi/BITMAP","wingdi/PBITMAP"]
old-location: gdi\bitmap.htm
tech.root: gdi
ms.assetid: 6ee382da-dd63-442b-80c3-59472defb41f
ms.date: 12/05/2018
ms.keywords: '*LPBITMAP, *NPBITMAP, *PBITMAP, BITMAP, BITMAP structure [Windows GDI], PBITMAP, PBITMAP structure pointer [Windows GDI], _win32_BITMAP_str, gdi.bitmap, wingdi/BITMAP, wingdi/PBITMAP'
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
req.typenames: BITMAP, *PBITMAP, *NPBITMAP, *LPBITMAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBITMAP
 - wingdi/tagBITMAP
 - PBITMAP
 - wingdi/PBITMAP
 - BITMAP
 - wingdi/BITMAP
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
 - BITMAP
---

# BITMAP structure


## -description

The <b>BITMAP</b> structure defines the type, width, height, color format, and bit values of a bitmap.

## -struct-fields

### -field bmType

The bitmap type. This member must be zero.

### -field bmWidth

The width, in pixels, of the bitmap. The width must be greater than zero.

### -field bmHeight

The height, in pixels, of the bitmap. The height must be greater than zero.

### -field bmWidthBytes

The number of bytes in each scan line. This value must be divisible by 2, because the system assumes that the bit values of a bitmap form an array that is word aligned.

### -field bmPlanes

The count of color planes.

### -field bmBitsPixel

The number of bits required to indicate the color of a pixel.

### -field bmBits

A pointer to the location of the bit values for the bitmap. The <b>bmBits</b> member must be a pointer to an array of character (1-byte) values.

## -remarks

The bitmap formats currently used are monochrome and color. The monochrome bitmap uses a one-bit, one-plane format. Each scan is a multiple of 16 bits.

Scans are organized as follows for a monochrome bitmap of height <i>n</i>:


``` syntax

    Scan 0 
    Scan 1 
    . 
    . 
    . 
    Scan n-2 
    Scan n-1 

```

The pixels on a monochrome device are either black or white. If the corresponding bit in the bitmap is 1, the pixel is set to the foreground color; if the corresponding bit in the bitmap is zero, the pixel is set to the background color.

All devices that have the RC_BITBLT device capability support bitmaps. For more information, see <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>.

Each device has a unique color format. To transfer a bitmap from one device to another, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> functions.

## -see-also

<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmapindirect">CreateBitmapIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>
