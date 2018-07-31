---
UID: NF:wingdi.MaskBlt
title: MaskBlt function
author: windows-sdk-content
description: The MaskBlt function combines the color data for the source and destination bitmaps using the specified mask and raster operation.
old-location: gdi\maskblt.htm
old-project: gdi
ms.assetid: 9fd6f0ce-a802-428d-9be5-a66afe39e9b7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MaskBlt, MaskBlt function [Windows GDI], _win32_MaskBlt, gdi.maskblt, wingdi/MaskBlt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - MaskBlt
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# MaskBlt function


## -description


The <b>MaskBlt</b> function combines the color data for the source and destination bitmaps using the specified mask and raster operation.


## -parameters




### -param hdcDest [in]

A handle to the destination device context.


### -param xDest

TBD


### -param yDest

TBD


### -param width

TBD


### -param height

TBD


### -param hdcSrc [in]

A handle to the device context from which the bitmap is to be copied. It must be zero if the <i>dwRop</i> parameter specifies a raster operation that does not include a source.


### -param xSrc

TBD


### -param ySrc

TBD


### -param hbmMask [in]

A handle to the monochrome mask bitmap combined with the color bitmap in the source device context.


### -param xMask [in]

The horizontal pixel offset for the mask bitmap specified by the <i>hbmMask</i> parameter.


### -param yMask [in]

The vertical pixel offset for the mask bitmap specified by the <i>hbmMask</i> parameter.


### -param rop

TBD




#### - dwRop [in]

The foreground and background ternary raster operation codes (ROPs) that the function uses to control the combination of source and destination data. The background raster operation code is stored in the high-order byte of the high-order word of this value; the foreground raster operation code is stored in the low-order byte of the high-order word of this value; the low-order word of this value is ignored, and should be zero. The macro <a href="https://msdn.microsoft.com/9056df62-a636-49c7-9c86-aecc731e8c4f">MAKEROP4</a> creates such combinations of foreground and background raster operation codes.

For a discussion of foreground and background in the context of this function, see the following Remarks section.

For a list of common raster operation codes (ROPs), see the <a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a> function. Note that the CAPTUREBLT ROP generally cannot be used for printing device contexts.


#### - nHeight [in]

The height, in logical units, of the destination rectangle and source bitmap.


#### - nWidth [in]

The width, in logical units, of the destination rectangle and source bitmap.


#### - nXDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.


#### - nXSrc [in]

The x-coordinate, in logical units, of the upper-left corner of the source bitmap.


#### - nYDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.


#### - nYSrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source bitmap.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>MaskBlt</b> function uses device-dependent bitmaps.

A value of 1 in the mask specified by <i>hbmMask</i> indicates that the foreground raster operation code specified by <i>dwRop</i> should be applied at that location. A value of 0 in the mask indicates that the background raster operation code specified by <i>dwRop</i> should be applied at that location.

If the raster operations require a source, the mask rectangle must cover the source rectangle. If it does not, the function will fail. If the raster operations do not require a source, the mask rectangle must cover the destination rectangle. If it does not, the function will fail.

If a rotation or shear transformation is in effect for the source device context when this function is called, an error occurs. However, other types of transformation are allowed.

If the color formats of the source, pattern, and destination bitmaps differ, this function converts the pattern or source format, or both, to match the destination format.

If the mask bitmap is not a monochrome bitmap, an error occurs.

When an enhanced metafile is being recorded, an error occurs (and the function returns <b>FALSE</b>) if the source device context identifies an enhanced-metafile device context.

Not all devices support the <b>MaskBlt</b> function. An application should call the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function with the <i>nIndex</i> parameter as RC_BITBLT to determine whether a device supports this function.

If no mask bitmap is supplied, this function behaves exactly like <a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a>, using the foreground raster operation code.

<b>ICM:</b> No color management is performed when blits occur.

When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap (compatible bitmap, or DDB) to a DIB by calling <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>. To display the DIB to the second device, call <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> or <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>.




## -see-also




<a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/2a56c71b-2e96-418b-8625-a808d76e0c85">PlgBlt</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

