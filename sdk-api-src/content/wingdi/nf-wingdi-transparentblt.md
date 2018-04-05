---
UID: NF:wingdi.TransparentBlt
title: TransparentBlt function
author: windows-driver-content
description: The TransparentBlt function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.
old-location: gdi\transparentblt.htm
old-project: gdi
ms.assetid: 900b2ca3-398d-4128-a1ae-8b4940574327
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: TransparentBlt, TransparentBlt function [Windows GDI], _win32_TransparentBlt, gdi.transparentblt, wingdi/TransparentBlt
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
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msimg32.dll
-	ext-ms-win-msimg-draw-l1-1-0.dll
api_name:
-	TransparentBlt
product: Windows
targetos: Windows
req.lib: Msimg32.lib
req.dll: Msimg32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# TransparentBlt function


## -description


The <b>TransparentBlt</b> function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.


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

The x-coordinate, in logical units, of the source rectangle.


### -param yoriginSrc [in]

The y-coordinate, in logical units, of the source rectangle.


### -param wSrc [in]

The width, in logical units, of the source rectangle.


### -param hSrc [in]

The height, in logical units, of the source rectangle.


### -param crTransparent [in]

The RGB color in the source bitmap to treat as transparent.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



The <b>TransparentBlt</b> function works with compatible bitmaps (DDBs).

The <b>TransparentBlt</b> function supports all formats of source bitmaps. However, for 32 bpp bitmaps, it just copies the alpha value over. Use <a href="https://msdn.microsoft.com/4624aa31-7e19-4506-ac70-9b3c98a8215d">AlphaBlend</a> to specify 32 bits-per-pixel bitmaps with transparency.

If the source and destination rectangles are not the same size, the source bitmap is stretched to match the destination rectangle. When the <a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a> function is used, the <i>iStretchMode</i> modes of BLACKONWHITE and WHITEONBLACK are converted to COLORONCOLOR for the <b>TransparentBlt</b> function.

The destination device context specifies the transformation type for the destination coordinates. The source device context specifies the transformation type for the source coordinates.

<b>TransparentBlt</b> does not mirror a bitmap if either the width or height, of either the source or destination, is negative.


         When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>. To display the DIB to the second device, call <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> or <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>.




## -see-also




<a href="https://msdn.microsoft.com/4624aa31-7e19-4506-ac70-9b3c98a8215d">AlphaBlend</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

