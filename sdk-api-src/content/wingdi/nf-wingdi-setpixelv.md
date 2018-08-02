---
UID: NF:wingdi.SetPixelV
title: SetPixelV function
author: windows-sdk-content
description: The SetPixelV function sets the pixel at the specified coordinates to the closest approximation of the specified color. The point must be in the clipping region and the visible part of the device surface.
old-location: gdi\setpixelv.htm
old-project: gdi
ms.assetid: 638f0ffd-3771-4390-b335-0517be5312fd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetPixelV, SetPixelV function [Windows GDI], _win32_SetPixelV, gdi.setpixelv, wingdi/SetPixelV
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
 - SetPixelV
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetPixelV function


## -description


The <b>SetPixelV</b> function sets the pixel at the specified coordinates to the closest approximation of the specified color. The point must be in the clipping region and the visible part of the device surface.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x

TBD


### -param y

TBD


### -param color

TBD




#### - X [in]

The x-coordinate, in logical units, of the point to be set.


#### - Y [in]

The y-coordinate, in logical units, of the point to be set.


#### - crColor [in]

The color to be used to paint the point. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Not all devices support the <b>SetPixelV</b> function. For more information, see the description of the RC_BITBLT capability in the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function.

<b>SetPixelV</b> is faster than <a href="https://msdn.microsoft.com/652e2e7a-79ae-4668-b269-153ee08a5de9">SetPixel</a> because it does not need to return the color value of the point actually painted.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/652e2e7a-79ae-4668-b269-153ee08a5de9">SetPixel</a>
 

 

