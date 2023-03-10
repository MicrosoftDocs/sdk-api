---
UID: NF:wingdi.CreateDIBPatternBrush
title: CreateDIBPatternBrush function (wingdi.h)
description: The CreateDIBPatternBrush function creates a logical brush that has the pattern specified by the specified device-independent bitmap (DIB).
helpviewer_keywords: ["CreateDIBPatternBrush","CreateDIBPatternBrush function [Windows GDI]","DIB_PAL_COLORS","DIB_RGB_COLORS","_win32_CreateDIBPatternBrush","gdi.createdibpatternbrush","wingdi/CreateDIBPatternBrush"]
old-location: gdi\createdibpatternbrush.htm
tech.root: gdi
ms.assetid: d123ef44-e047-4188-a2bc-20e479869dc3
ms.date: 12/05/2018
ms.keywords: CreateDIBPatternBrush, CreateDIBPatternBrush function [Windows GDI], DIB_PAL_COLORS, DIB_RGB_COLORS, _win32_CreateDIBPatternBrush, gdi.createdibpatternbrush, wingdi/CreateDIBPatternBrush
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
 - CreateDIBPatternBrush
 - wingdi/CreateDIBPatternBrush
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
 - CreateDIBPatternBrush
---

# CreateDIBPatternBrush function


## -description

The <b>CreateDIBPatternBrush</b> function creates a logical brush that has the pattern specified by the specified device-independent bitmap (DIB). The brush can subsequently be selected into any device context that is associated with a device that supports raster operations.


<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a> function.</div>
<div> </div>

## -parameters

### -param h [in]

A handle to a global memory object containing a packed DIB, which consists of a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure immediately followed by an array of bytes defining the pixels of the bitmap.

### -param iUsage [in]

Specifies whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure is initialized and, if so, whether this member contains explicit red, green, blue (RGB) values or indexes into a logical palette. The <i>fuColorSpec</i> parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DIB_PAL_COLORS"></a><a id="dib_pal_colors"></a><dl>
<dt><b>DIB_PAL_COLORS</b></dt>
</dl>
</td>
<td width="60%">
A color table is provided and consists of an array of 16-bit indexes into the logical palette of the device context into which the brush is to be selected.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
A color table is provided and contains literal RGB values.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When an application selects a two-color DIB pattern brush into a monochrome device context, the system does not acknowledge the colors specified in the DIB; instead, it displays the pattern brush using the current background and foreground colors of the device context. Pixels mapped to the first color of the DIB (offset 0 in the DIB color table) are displayed using the foreground color; pixels mapped to the second color (offset 1 in the color table) are displayed using the background color.

When you no longer need the brush, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

<b>ICM:</b> No color is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcolor">SetTextColor</a>