---
UID: NF:wingdi.PlgBlt
title: PlgBlt function
author: windows-driver-content
description: The PlgBlt function performs a bit-block transfer of the bits of color data from the specified rectangle in the source device context to the specified parallelogram in the destination device context.
old-location: gdi\plgblt.htm
old-project: gdi
ms.assetid: 2a56c71b-2e96-418b-8625-a808d76e0c85
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: PlgBlt, PlgBlt function [Windows GDI], _win32_PlgBlt, gdi.plgblt, wingdi/PlgBlt
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	PlgBlt
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PlgBlt function


## -description


The <b>PlgBlt</b> function performs a bit-block transfer of the bits of color data from the specified rectangle in the source device context to the specified parallelogram in the destination device context. If the given bitmask handle identifies a valid monochrome bitmap, the function uses this bitmap to mask the bits of color data from the source rectangle.


## -parameters




### -param hdcDest [in]

A handle to the destination device context.


### -param lpPoint [in]

A pointer to an array of three points in logical space that identify three corners of the destination parallelogram. The upper-left corner of the source rectangle is mapped to the first point in this array, the upper-right corner to the second point in this array, and the lower-left corner to the third point. The lower-right corner of the source rectangle is mapped to the implicit fourth point in the parallelogram.


### -param hdcSrc [in]

A handle to the source device context.


### -param xSrc

TBD


### -param ySrc

TBD


### -param width

TBD


### -param height

TBD


### -param hbmMask [in]

A handle to an optional monochrome bitmap that is used to mask the colors of the source rectangle.


### -param xMask [in]

The x-coordinate, in logical units, of the upper-left corner of the monochrome bitmap.


### -param yMask [in]

The y-coordinate, in logical units, of the upper-left corner of the monochrome bitmap.


#### - nHeight [in]

The height, in logical units, of the source rectangle.


#### - nWidth [in]

The width, in logical units, of the source rectangle.


#### - nXSrc [in]

The x-coordinate, in logical units, of the upper-left corner of the source rectangle.


#### - nYSrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>PlgBlt</b> function works with device-dependent bitmaps.

The fourth vertex of the parallelogram (D) is defined by treating the first three points (A, B, and C ) as vectors and computing D = B +CA.

If the bitmask exists, a value of one in the mask indicates that the source pixel color should be copied to the destination. A value of zero in the mask indicates that the destination pixel color is not to be changed. If the mask rectangle is smaller than the source and destination rectangles, the function replicates the mask pattern.

Scaling, translation, and reflection transformations are allowed in the source device context; however, rotation and shear transformations are not. If the mask bitmap is not a monochrome bitmap, an error occurs. The stretching mode for the destination device context is used to determine how to stretch or compress the pixels, if that is necessary.

When an enhanced metafile is being recorded, an error occurs if the source device context identifies an enhanced-metafile device context.

The destination coordinates are transformed according to the destination device context; the source coordinates are transformed according to the source device context. If the source transformation has a rotation or shear, an error is returned.

If the destination and source rectangles do not have the same color format, <b>PlgBlt</b> converts the source rectangle to match the destination rectangle.

Not all devices support the <b>PlgBlt</b> function. For more information, see the description of the RC_BITBLT raster capability in the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function.

If the source and destination device contexts represent incompatible devices, <b>PlgBlt</b> returns an error.


         When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>. To display the DIB to the second device, call <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> or <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>.




## -see-also




<a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/9fd6f0ce-a802-428d-9be5-a66afe39e9b7">MaskBlt</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

