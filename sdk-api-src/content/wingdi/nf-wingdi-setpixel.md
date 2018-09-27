---
UID: NF:wingdi.SetPixel
title: SetPixel function
author: windows-sdk-content
description: The SetPixel function sets the pixel at the specified coordinates to the specified color.
old-location: gdi\setpixel.htm
tech.root: gdi
ms.assetid: 652e2e7a-79ae-4668-b269-153ee08a5de9
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetPixel, SetPixel function [Windows GDI], _win32_SetPixel, gdi.setpixel, wingdi/SetPixel
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
 - SetPixel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetPixel function


## -description


The <b>SetPixel</b> function sets the pixel at the specified coordinates to the specified color.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The x-coordinate, in logical units, of the point to be set.


### -param y [in]

The y-coordinate, in logical units, of the point to be set.


### -param color [in]

The color to be used to paint the point. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value is the RGB value that the function sets the pixel to. This value may differ from the color specified by <i>crColor</i>; that occurs when an exact match for the specified color cannot be found.

If the function fails, the return value is -1.

This can be the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
</table>
 




## -remarks



The function fails if the pixel coordinates lie outside of the current clipping region.

Not all devices support the <b>SetPixel</b> function. For more information, see <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/46d17e95-93ce-4a43-b86c-489d6e3afe12">GetPixel</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/638f0ffd-3771-4390-b335-0517be5312fd">SetPixelV</a>
 

 

