---
UID: NF:wingdi.SetStretchBltMode
title: SetStretchBltMode function (wingdi.h)
description: The SetStretchBltMode function sets the bitmap stretching mode in the specified device context.
helpviewer_keywords: ["BLACKONWHITE","COLORONCOLOR","HALFTONE","STRETCH_ANDSCANS","STRETCH_DELETESCANS","STRETCH_HALFTONE","STRETCH_ORSCANS","SetStretchBltMode","SetStretchBltMode function [Windows GDI]","WHITEONBLACK","_win32_SetStretchBltMode","gdi.setstretchbltmode","wingdi/SetStretchBltMode"]
old-location: gdi\setstretchbltmode.htm
tech.root: gdi
ms.assetid: 3e5a48dc-ccd5-41ea-a24b-5c40213abf38
ms.date: 12/05/2018
ms.keywords: BLACKONWHITE, COLORONCOLOR, HALFTONE, STRETCH_ANDSCANS, STRETCH_DELETESCANS, STRETCH_HALFTONE, STRETCH_ORSCANS, SetStretchBltMode, SetStretchBltMode function [Windows GDI], WHITEONBLACK, _win32_SetStretchBltMode, gdi.setstretchbltmode, wingdi/SetStretchBltMode
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
 - SetStretchBltMode
 - wingdi/SetStretchBltMode
dev_langs:
 - c++
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
 - SetStretchBltMode
---

# SetStretchBltMode function


## -description

The <b>SetStretchBltMode</b> function sets the bitmap stretching mode in the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param mode [in]

The stretching mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BLACKONWHITE"></a><a id="blackonwhite"></a><dl>
<dt><b>BLACKONWHITE</b></dt>
</dl>
</td>
<td width="60%">
Performs a Boolean AND operation using the color values for the eliminated and existing pixels. If the bitmap is a monochrome bitmap, this mode preserves black pixels at the expense of white pixels.

</td>
</tr>
<tr>
<td width="40%"><a id="COLORONCOLOR"></a><a id="coloroncolor"></a><dl>
<dt><b>COLORONCOLOR</b></dt>
</dl>
</td>
<td width="60%">
Deletes the pixels. This mode deletes all eliminated lines of pixels without trying to preserve their information.

</td>
</tr>
<tr>
<td width="40%"><a id="HALFTONE"></a><a id="halftone"></a><dl>
<dt><b>HALFTONE</b></dt>
</dl>
</td>
<td width="60%">
Maps pixels from the source rectangle into blocks of pixels in the destination rectangle. The average color over the destination block of pixels approximates the color of the source pixels.

After setting the HALFTONE stretching mode, an application must call the <a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a> function to set the brush origin. If it fails to do so, brush misalignment occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="STRETCH_ANDSCANS"></a><a id="stretch_andscans"></a><dl>
<dt><b>STRETCH_ANDSCANS</b></dt>
</dl>
</td>
<td width="60%">
Same as BLACKONWHITE.

</td>
</tr>
<tr>
<td width="40%"><a id="STRETCH_DELETESCANS"></a><a id="stretch_deletescans"></a><dl>
<dt><b>STRETCH_DELETESCANS</b></dt>
</dl>
</td>
<td width="60%">
Same as COLORONCOLOR.

</td>
</tr>
<tr>
<td width="40%"><a id="STRETCH_HALFTONE"></a><a id="stretch_halftone"></a><dl>
<dt><b>STRETCH_HALFTONE</b></dt>
</dl>
</td>
<td width="60%">
Same as HALFTONE.

</td>
</tr>
<tr>
<td width="40%"><a id="STRETCH_ORSCANS"></a><a id="stretch_orscans"></a><dl>
<dt><b>STRETCH_ORSCANS</b></dt>
</dl>
</td>
<td width="60%">
Same as WHITEONBLACK.

</td>
</tr>
<tr>
<td width="40%"><a id="WHITEONBLACK"></a><a id="whiteonblack"></a><dl>
<dt><b>WHITEONBLACK</b></dt>
</dl>
</td>
<td width="60%">
Performs a Boolean OR operation using the color values for the eliminated and existing pixels. If the bitmap is a monochrome bitmap, this mode preserves white pixels at the expense of black pixels.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the previous stretching mode.

If the function fails, the return value is zero.

This function can return the following value.

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

The stretching mode defines how the system combines rows or columns of a bitmap with existing pixels on a display device when an application calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> function.

The BLACKONWHITE (STRETCH_ANDSCANS) and WHITEONBLACK (STRETCH_ORSCANS) modes are typically used to preserve foreground pixels in monochrome bitmaps. The COLORONCOLOR (STRETCH_DELETESCANS) mode is typically used to preserve color in color bitmaps.

The HALFTONE mode is slower and requires more processing of the source image than the other three modes; but produces higher quality images. Also note that <a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a> must be called after setting the HALFTONE mode to avoid brush misalignment.

Additional stretching modes might also be available depending on the capabilities of the device driver.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getstretchbltmode">GetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>