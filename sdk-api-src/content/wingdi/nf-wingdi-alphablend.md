---
UID: NF:wingdi.AlphaBlend
title: AlphaBlend function
author: windows-sdk-content
description: The AlphaBlend function displays bitmaps that have transparent or semitransparent pixels.
old-location: gdi\alphablend.htm
tech.root: gdi
ms.assetid: 4624aa31-7e19-4506-ac70-9b3c98a8215d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AlphaBlend, AlphaBlend function [Windows GDI], _win32_AlphaBlend, gdi.alphablend, wingdi/AlphaBlend
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
req.lib: Msimg32.lib
req.dll: Msimg32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msimg32.dll
 - ext-ms-win-msimg-draw-l1-1-0.dll
api_name:
 - AlphaBlend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AlphaBlend function


## -description


The <b>AlphaBlend</b> function displays bitmaps that have transparent or semitransparent pixels.


## -parameters




### -param hdcDest [in]

A handle to the destination device context.


### -param xoriginDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.


### -param yoriginDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.


### -param wDest [in]

The width, in logical units, of the destination rectangle.


### -param hDest [in]

The height, in logical units, of the destination rectangle.


### -param hdcSrc [in]

A handle to the source device context.


### -param xoriginSrc [in]

The x-coordinate, in logical units, of the upper-left corner of the source rectangle.


### -param yoriginSrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source rectangle.


### -param wSrc [in]

The width, in logical units, of the source rectangle.


### -param hSrc [in]

The height, in logical units, of the source rectangle.


### -param ftn [in]

The alpha-blending function for source and destination bitmaps, a global alpha value to be applied to the entire source bitmap, and format information for the source bitmap. The source and destination blend functions are currently limited to AC_SRC_OVER. See the <a href="https://msdn.microsoft.com/d1371d72-c408-4484-845e-d4ea2bc3115d">BLENDFUNCTION</a> and <a href="https://msdn.microsoft.com/3270d8ed-a174-4d77-a9a7-3e3f0cab2a23">EMRALPHABLEND</a> structures.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



If the source rectangle and destination rectangle are not the same size, the source bitmap is stretched to match the destination rectangle. If the <a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a> function is used, the <i>iStretchMode</i> value is automatically converted to COLORONCOLOR for this function (that is, BLACKONWHITE, WHITEONBLACK, and HALFTONE are changed to COLORONCOLOR).

The destination coordinates are transformed by using the transformation currently specified for the destination device context. The source coordinates are transformed by using the transformation currently specified for the source device context.

An error occurs (and the function returns <b>FALSE</b>) if the source device context identifies an enhanced metafile device context.

If destination and source bitmaps do not have the same color format, <b>AlphaBlend</b> converts the source bitmap to match the destination bitmap.

<b>AlphaBlend</b> does not support mirroring. If either the width or height of the source or destination is negative, this call will fail.

When rendering to a printer, first call <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> with SHADEBLENDCAPS to determine if the printer supports blending with <b>AlphaBlend</b>. Note that, for a display DC, all blending operations are supported and these flags represent whether the operations are accelerated.

If the source and destination are the same surfacethat is, they are both the screen or the same memory bitmap and the source and destination rectangles overlap, an error occurs and the function returns <b>FALSE</b>.

The source rectangle must lie completely within the source surface, otherwise an error occurs and the function returns <b>FALSE</b>.

<b>AlphaBlend</b> fails if the width or height of the source or destination is negative.

The <b>SourceConstantAlpha</b> member of <a href="https://msdn.microsoft.com/d1371d72-c408-4484-845e-d4ea2bc3115d">BLENDFUNCTION</a> specifies an alpha transparency value to be used on the entire source bitmap. The <b>SourceConstantAlpha</b> value is combined with any per-pixel alpha values. If <b>SourceConstantAlpha</b> is 0, it is assumed that the image is transparent. Set the <b>SourceConstantAlpha</b> value to 255 (which indicates that the image is opaque) when you only want to use per-pixel alpha values.




## -see-also




<a href="https://msdn.microsoft.com/d1371d72-c408-4484-845e-d4ea2bc3115d">BLENDFUNCTION</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/3270d8ed-a174-4d77-a9a7-3e3f0cab2a23">EMRALPHABLEND</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>
 

 

