---
UID: NF:wingdi.GetStretchBltMode
title: GetStretchBltMode function (wingdi.h)
author: windows-sdk-content
description: The GetStretchBltMode function retrieves the current stretching mode. The stretching mode defines how color data is added to or removed from bitmaps that are stretched or compressed when the StretchBlt function is called.
old-location: gdi\getstretchbltmode.htm
tech.root: gdi
ms.assetid: a4408e28-d7ac-44e9-905d-efa75c60e503
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStretchBltMode, GetStretchBltMode function [Windows GDI], _win32_GetStretchBltMode, gdi.getstretchbltmode, wingdi/GetStretchBltMode
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetStretchBltMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetStretchBltMode function


## -description


The <b>GetStretchBltMode</b> function retrieves the current stretching mode. The stretching mode defines how color data is added to or removed from bitmaps that are stretched or compressed when the <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> function is called.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is the current stretching mode. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>BLACKONWHITE</td>
<td>Performs a Boolean AND operation using the color values for the eliminated and existing pixels. If the bitmap is a monochrome bitmap, this mode preserves black pixels at the expense of white pixels.</td>
</tr>
<tr>
<td>COLORONCOLOR</td>
<td>Deletes the pixels. This mode deletes all eliminated lines of pixels without trying to preserve their information.</td>
</tr>
<tr>
<td>HALFTONE</td>
<td>Maps pixels from the source rectangle into blocks of pixels in the destination rectangle. The average color over the destination block of pixels approximates the color of the source pixels.</td>
</tr>
<tr>
<td>STRETCH_ANDSCANS</td>
<td>Same as BLACKONWHITE.</td>
</tr>
<tr>
<td>STRETCH_DELETESCANS</td>
<td>Same as COLORONCOLOR.</td>
</tr>
<tr>
<td>STRETCH_HALFTONE</td>
<td>Same as HALFTONE.</td>
</tr>
<tr>
<td>STRETCH_ORSCANS</td>
<td>Same as WHITEONBLACK.</td>
</tr>
<tr>
<td>WHITEONBLACK</td>
<td>Performs a Boolean OR operation using the color values for the eliminated and existing pixels. If the bitmap is a monochrome bitmap, this mode preserves white pixels at the expense of black pixels.</td>
</tr>
</table>
 

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>
 

 

