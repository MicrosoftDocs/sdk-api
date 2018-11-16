---
UID: NF:wingdi.GetPixel
title: GetPixel function
author: windows-sdk-content
description: The GetPixel function retrieves the red, green, blue (RGB) color value of the pixel at the specified coordinates.
old-location: gdi\getpixel.htm
tech.root: gdi
ms.assetid: 46d17e95-93ce-4a43-b86c-489d6e3afe12
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPixel, GetPixel function [Windows GDI], _win32_GetPixel, gdi.getpixel, wingdi/GetPixel
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetPixel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetPixel
: 
---

# GetPixel function


## -description


The <b>GetPixel</b> function retrieves the red, green, blue (RGB) color value of the pixel at the specified coordinates.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The x-coordinate, in logical units, of the pixel to be examined.


### -param y [in]

The y-coordinate, in logical units, of the pixel to be examined.


## -returns



The return value is the <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that specifies the RGB of the pixel. If the pixel is outside of the current clipping region, the return value is CLR_INVALID (0xFFFFFFFF defined in Wingdi.h).




## -remarks



The pixel must be within the boundaries of the current clipping region.

Not all devices support <b>GetPixel</b>. An application should call <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> to determine whether a specified device supports this function.

A bitmap must be selected within the device context, otherwise, CLR_INVALID is returned on all pixels.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/652e2e7a-79ae-4668-b269-153ee08a5de9">SetPixel</a>
 

 

