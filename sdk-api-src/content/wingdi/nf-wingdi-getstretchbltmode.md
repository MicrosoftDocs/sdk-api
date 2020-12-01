---
UID: NF:wingdi.GetStretchBltMode
title: GetStretchBltMode function (wingdi.h)
description: The GetStretchBltMode function retrieves the current stretching mode. The stretching mode defines how color data is added to or removed from bitmaps that are stretched or compressed when the StretchBlt function is called.
helpviewer_keywords: ["GetStretchBltMode","GetStretchBltMode function [Windows GDI]","_win32_GetStretchBltMode","gdi.getstretchbltmode","wingdi/GetStretchBltMode"]
old-location: gdi\getstretchbltmode.htm
tech.root: gdi
ms.assetid: a4408e28-d7ac-44e9-905d-efa75c60e503
ms.date: 12/05/2018
ms.keywords: GetStretchBltMode, GetStretchBltMode function [Windows GDI], _win32_GetStretchBltMode, gdi.getstretchbltmode, wingdi/GetStretchBltMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetStretchBltMode
 - wingdi/GetStretchBltMode
dev_langs:
 - c++
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
---

# GetStretchBltMode function


## -description

The <b>GetStretchBltMode</b> function retrieves the current stretching mode. The stretching mode defines how color data is added to or removed from bitmaps that are stretched or compressed when the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> function is called.

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

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>