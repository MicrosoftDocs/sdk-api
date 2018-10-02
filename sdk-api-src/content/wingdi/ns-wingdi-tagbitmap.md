---
UID: NS:wingdi.tagBITMAP
title: tagBITMAP
author: windows-sdk-content
description: The BITMAP structure defines the type, width, height, color format, and bit values of a bitmap.
old-location: gdi\bitmap.htm
tech.root: gdi
ms.assetid: 6ee382da-dd63-442b-80c3-59472defb41f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPBITMAP, *NPBITMAP, *PBITMAP, BITMAP, BITMAP structure [Windows GDI], PBITMAP, PBITMAP structure pointer [Windows GDI], _win32_BITMAP_str, gdi.bitmap, tagBITMAP, wingdi/BITMAP, wingdi/PBITMAP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - BITMAP
product: Windows
targetos: Windows
req.typenames: BITMAP, *PBITMAP, *NPBITMAP, *LPBITMAP
req.redist: 
---

# tagBITMAP structure


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

<pre class="syntax" xml:space="preserve"><code>
    Scan 0 
    Scan 1 
    . 
    . 
    . 
    Scan n-2 
    Scan n-1 
</code></pre>
The pixels on a monochrome device are either black or white. If the corresponding bit in the bitmap is 1, the pixel is set to the foreground color; if the corresponding bit in the bitmap is zero, the pixel is set to the background color.

All devices that have the RC_BITBLT device capability support bitmaps. For more information, see <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>.

Each device has a unique color format. To transfer a bitmap from one device to another, use the <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a> and <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5">CreateBitmapIndirect</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>
 

 

