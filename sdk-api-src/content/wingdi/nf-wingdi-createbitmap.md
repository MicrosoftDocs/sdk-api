---
UID: NF:wingdi.CreateBitmap
title: CreateBitmap function
author: windows-driver-content
description: The CreateBitmap function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).
old-location: gdi\createbitmap.htm
old-project: gdi
ms.assetid: b52e1baf-6a81-44bc-a061-4d42e6f4ed64
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CreateBitmap, CreateBitmap function [Windows GDI], _win32_CreateBitmap, gdi.createbitmap, wingdi/CreateBitmap
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
-	Ext-MS-Win-GDI-Draw-l1-1-0.dll
-	Ext-MS-Win-GDI-Draw-l1-1-1.dll
-	ext-ms-win-gdi-draw-l1-1-2.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	CreateBitmap
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateBitmap function


## -description


The <b>CreateBitmap</b> function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).


## -parameters




### -param nWidth [in]

The bitmap width, in pixels.


### -param nHeight [in]

The bitmap height, in pixels.


### -param nPlanes

TBD


### -param nBitCount

TBD


### -param lpBits

TBD




#### - cBitsPerPel [in]

The number of bits required to identify the color of a single pixel.


#### - cPlanes [in]

The number of color planes used by the device.


#### - lpvBits [in]

A pointer to an array of color data used to set the colors in a rectangle of pixels. Each scan line in the rectangle must be word aligned (scan lines that are not word aligned must be padded with zeros). If this parameter is <b>NULL</b>, the contents of the new bitmap is undefined.


## -returns



If the function succeeds, the return value is a handle to a bitmap.

If the function fails, the return value is <b>NULL</b>.

This function can return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The calculated size of the bitmap is less than zero.

</td>
</tr>
</table>
 




## -remarks



The <b>CreateBitmap</b> function creates a device-dependent bitmap.

After a bitmap is created, it can be selected into a device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. However, the bitmap can only be selected into a device context if the bitmap and the DC have the same format.

The <b>CreateBitmap</b> function can be used to create color bitmaps. However, for performance reasons applications should use <b>CreateBitmap</b> to create monochrome bitmaps and <a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a> to create color bitmaps. Whenever a color bitmap returned from <b>CreateBitmap</b> is selected into a device context, the system checks that the bitmap matches the format of the device context it is being selected into. Because <b>CreateCompatibleBitmap</b> takes a device context, it returns a bitmap that has the same format as the specified device context. Thus, subsequent calls to <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> are faster with a color bitmap from <b>CreateCompatibleBitmap</b> than with a color bitmap returned from <b>CreateBitmap</b>.

If the bitmap is monochrome, zeros represent the foreground color and ones represent the background color for the destination device context.

If an application sets the <i>nWidth</i> or <i>nHeight</i> parameters to zero, <b>CreateBitmap</b> returns the handle to a 1-by-1 pixel, monochrome bitmap.

When you no longer need the bitmap, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5">CreateBitmapIndirect</a>



<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/72e8cc6b-d282-451e-b6ec-0473d2daea7c">GetBitmapBits</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/3cab12a6-c408-4552-bec0-5ecfd8374757">SetBitmapBits</a>
 

 

