---
UID: NF:wingdi.CreateDIBPatternBrushPt
title: CreateDIBPatternBrushPt function (wingdi.h)
description: The CreateDIBPatternBrushPt function creates a logical brush that has the pattern specified by the device-independent bitmap (DIB).
helpviewer_keywords: ["CreateDIBPatternBrushPt","CreateDIBPatternBrushPt function [Windows GDI]","DIB_PAL_COLORS","DIB_RGB_COLORS","_win32_CreateDIBPatternBrushPt","gdi.createdibpatternbrushpt","wingdi/CreateDIBPatternBrushPt"]
old-location: gdi\createdibpatternbrushpt.htm
tech.root: gdi
ms.assetid: 0e34d108-fd35-4512-9eb3-c7710af36e95
ms.date: 12/05/2018
ms.keywords: CreateDIBPatternBrushPt, CreateDIBPatternBrushPt function [Windows GDI], DIB_PAL_COLORS, DIB_RGB_COLORS, _win32_CreateDIBPatternBrushPt, gdi.createdibpatternbrushpt, wingdi/CreateDIBPatternBrushPt
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
 - CreateDIBPatternBrushPt
 - wingdi/CreateDIBPatternBrushPt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreateDIBPatternBrushPt
---

# CreateDIBPatternBrushPt function


## -description

The <b>CreateDIBPatternBrushPt</b> function creates a logical brush that has the pattern specified by the device-independent bitmap (DIB).

## -parameters

### -param lpPackedDIB [in]

A pointer to a packed DIB consisting of a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure immediately followed by an array of bytes defining the pixels of the bitmap.

### -param iUsage [in]

Specifies whether the <b>bmiColors</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure contains a valid color table and, if so, whether the entries in this color table contain explicit red, green, blue (RGB) values or palette indexes. The <i>iUsage</i> parameter must be one of the following values.

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

A brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreateDIBPatternBrushPt</b>, it can select that brush into any device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function.

When you no longer need the brush, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

<b>ICM:</b> No color is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbrushorgex">GetBrushOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a>