---
UID: NF:wingdi.SetROP2
title: SetROP2 function (wingdi.h)
description: The SetROP2 function sets the current foreground mix mode.
helpviewer_keywords: ["R2_BLACK","R2_COPYPEN","R2_MASKNOTPEN","R2_MASKPEN","R2_MASKPENNOT","R2_MERGENOTPEN","R2_MERGEPEN","R2_MERGEPENNOT","R2_NOP","R2_NOT","R2_NOTCOPYPEN","R2_NOTMASKPEN","R2_NOTMERGEPEN","R2_NOTXORPEN","R2_WHITE","R2_XORPEN","SetROP2","SetROP2 function [Windows GDI]","_win32_SetROP2","gdi.setrop2","wingdi/SetROP2"]
old-location: gdi\setrop2.htm
tech.root: gdi
ms.assetid: a462a03d-e2c8-403e-aab4-ae03fb96f06f
ms.date: 12/05/2018
ms.keywords: R2_BLACK, R2_COPYPEN, R2_MASKNOTPEN, R2_MASKPEN, R2_MASKPENNOT, R2_MERGENOTPEN, R2_MERGEPEN, R2_MERGEPENNOT, R2_NOP, R2_NOT, R2_NOTCOPYPEN, R2_NOTMASKPEN, R2_NOTMERGEPEN, R2_NOTXORPEN, R2_WHITE, R2_XORPEN, SetROP2, SetROP2 function [Windows GDI], _win32_SetROP2, gdi.setrop2, wingdi/SetROP2
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
 - SetROP2
 - wingdi/SetROP2
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
 - SetROP2
---

# SetROP2 function


## -description

The <b>SetROP2</b> function sets the current foreground mix mode. GDI uses the foreground mix mode to combine pens and interiors of filled objects with the colors already on the screen. The foreground mix mode defines how colors from the brush or pen and the colors in the existing image are to be combined.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param rop2 [in]

The mix mode. This parameter can be one of the following values.

<table>
<tr>
<th>Mix mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="R2_BLACK"></a><a id="r2_black"></a><dl>
<dt><b>R2_BLACK</b></dt>
</dl>
</td>
<td width="60%">
Pixel is always 0.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_COPYPEN"></a><a id="r2_copypen"></a><dl>
<dt><b>R2_COPYPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the pen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MASKNOTPEN"></a><a id="r2_masknotpen"></a><dl>
<dt><b>R2_MASKNOTPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors common to both the screen and the inverse of the pen.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MASKPEN"></a><a id="r2_maskpen"></a><dl>
<dt><b>R2_MASKPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors common to both the pen and the screen.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MASKPENNOT"></a><a id="r2_maskpennot"></a><dl>
<dt><b>R2_MASKPENNOT</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors common to both the pen and the inverse of the screen.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MERGENOTPEN"></a><a id="r2_mergenotpen"></a><dl>
<dt><b>R2_MERGENOTPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the screen color and the inverse of the pen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MERGEPEN"></a><a id="r2_mergepen"></a><dl>
<dt><b>R2_MERGEPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the pen color and the screen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_MERGEPENNOT"></a><a id="r2_mergepennot"></a><dl>
<dt><b>R2_MERGEPENNOT</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the pen color and the inverse of the screen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOP"></a><a id="r2_nop"></a><dl>
<dt><b>R2_NOP</b></dt>
</dl>
</td>
<td width="60%">
Pixel remains unchanged.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOT"></a><a id="r2_not"></a><dl>
<dt><b>R2_NOT</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the screen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTCOPYPEN"></a><a id="r2_notcopypen"></a><dl>
<dt><b>R2_NOTCOPYPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the pen color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTMASKPEN"></a><a id="r2_notmaskpen"></a><dl>
<dt><b>R2_NOTMASKPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the R2_MASKPEN color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTMERGEPEN"></a><a id="r2_notmergepen"></a><dl>
<dt><b>R2_NOTMERGEPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the R2_MERGEPEN color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_NOTXORPEN"></a><a id="r2_notxorpen"></a><dl>
<dt><b>R2_NOTXORPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is the inverse of the R2_XORPEN color.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_WHITE"></a><a id="r2_white"></a><dl>
<dt><b>R2_WHITE</b></dt>
</dl>
</td>
<td width="60%">
Pixel is always 1.

</td>
</tr>
<tr>
<td width="40%"><a id="R2_XORPEN"></a><a id="r2_xorpen"></a><dl>
<dt><b>R2_XORPEN</b></dt>
</dl>
</td>
<td width="60%">
Pixel is a combination of the colors in the pen and in the screen, but not in both.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value specifies the previous mix mode.

If the function fails, the return value is zero.

## -remarks

Mix modes define how GDI combines source and destination colors when drawing with the current pen. The mix modes are binary raster operation codes, representing all possible Boolean functions of two variables, using the binary operations AND, OR, and XOR (exclusive OR), and the unary operation NOT. The mix mode is for raster devices only; it is not available for vector devices.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getrop2">GetROP2</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>