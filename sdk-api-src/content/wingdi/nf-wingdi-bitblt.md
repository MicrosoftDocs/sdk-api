---
UID: NF:wingdi.BitBlt
title: BitBlt function (wingdi.h)
description: The BitBlt function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.
helpviewer_keywords: ["BLACKNESS","BitBlt","BitBlt function [Windows GDI]","CAPTUREBLT","DSTINVERT","MERGECOPY","MERGEPAINT","NOMIRRORBITMAP","NOTSRCCOPY","NOTSRCERASE","PATCOPY","PATINVERT","PATPAINT","SRCAND","SRCCOPY","SRCERASE","SRCINVERT","SRCPAINT","WHITENESS","_win32_BitBlt","gdi.bitblt","wingdi/BitBlt"]
old-location: gdi\bitblt.htm
tech.root: gdi
ms.assetid: d6a181e4-b6cf-44b7-bf47-4900272d6d72
ms.date: 12/05/2018
ms.keywords: BLACKNESS, BitBlt, BitBlt function [Windows GDI], CAPTUREBLT, DSTINVERT, MERGECOPY, MERGEPAINT, NOMIRRORBITMAP, NOTSRCCOPY, NOTSRCERASE, PATCOPY, PATINVERT, PATPAINT, SRCAND, SRCCOPY, SRCERASE, SRCINVERT, SRCPAINT, WHITENESS, _win32_BitBlt, gdi.bitblt, wingdi/BitBlt
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
ms.custom: snippet-project
f1_keywords:
 - BitBlt
 - wingdi/BitBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - BitBlt
---

# BitBlt function


## -description

The <b>BitBlt</b> function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.

## -parameters

### -param hdc [in]

A handle to the destination device context.

### -param x [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param y [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param cx [in]

The width, in logical units, of the source and destination rectangles.

### -param cy [in]

The height, in logical units, of the source and the destination rectangles.

### -param hdcSrc [in]

A handle to the source device context.

### -param x1 [in]

The x-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param y1 [in]

The y-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param rop [in]

A raster-operation code. These codes define how the color data for the source rectangle is to be combined with the color data for the destination rectangle to achieve the final color.

The following list shows some common raster operation codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BLACKNESS"></a><a id="blackness"></a><dl>
<dt><b>BLACKNESS</b></dt>
</dl>
</td>
<td width="60%">
Fills the destination rectangle using the color associated with index 0 in the physical palette. (This color is black for the default physical palette.)

</td>
</tr>
<tr>
<td width="40%"><a id="CAPTUREBLT"></a><a id="captureblt"></a><dl>
<dt><b>CAPTUREBLT</b></dt>
</dl>
</td>
<td width="60%">
Includes any windows that are layered on top of your window in the resulting image. By default, the image only contains your window. Note that this generally cannot be used for printing device contexts.

</td>
</tr>
<tr>
<td width="40%"><a id="DSTINVERT"></a><a id="dstinvert"></a><dl>
<dt><b>DSTINVERT</b></dt>
</dl>
</td>
<td width="60%">
Inverts the destination rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="MERGECOPY"></a><a id="mergecopy"></a><dl>
<dt><b>MERGECOPY</b></dt>
</dl>
</td>
<td width="60%">
Merges the colors of the source rectangle with the brush currently selected in <i>hdcDest</i>, by using the Boolean AND operator.

</td>
</tr>
<tr>
<td width="40%"><a id="MERGEPAINT"></a><a id="mergepaint"></a><dl>
<dt><b>MERGEPAINT</b></dt>
</dl>
</td>
<td width="60%">
Merges the colors of the inverted source rectangle with the colors of the destination rectangle by using the Boolean OR operator.

</td>
</tr>
<tr>
<td width="40%"><a id="NOMIRRORBITMAP"></a><a id="nomirrorbitmap"></a><dl>
<dt><b>NOMIRRORBITMAP</b></dt>
</dl>
</td>
<td width="60%">
Prevents the bitmap from being mirrored.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTSRCCOPY"></a><a id="notsrccopy"></a><dl>
<dt><b>NOTSRCCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the inverted source rectangle to the destination.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTSRCERASE"></a><a id="notsrcerase"></a><dl>
<dt><b>NOTSRCERASE</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the source and destination rectangles by using the Boolean OR operator and then inverts the resultant color.

</td>
</tr>
<tr>
<td width="40%"><a id="PATCOPY"></a><a id="patcopy"></a><dl>
<dt><b>PATCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the brush currently selected in <i>hdcDest</i>, into the destination bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="PATINVERT"></a><a id="patinvert"></a><dl>
<dt><b>PATINVERT</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the brush currently selected in <i>hdcDest</i>, with the colors of the destination rectangle by using the Boolean XOR operator.

</td>
</tr>
<tr>
<td width="40%"><a id="PATPAINT"></a><a id="patpaint"></a><dl>
<dt><b>PATPAINT</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the brush currently selected in <i>hdcDest</i>, with the colors of the inverted source rectangle by using the Boolean OR operator. The result of this operation is combined with the colors of the destination rectangle by using the Boolean OR operator.

</td>
</tr>
<tr>
<td width="40%"><a id="SRCAND"></a><a id="srcand"></a><dl>
<dt><b>SRCAND</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the source and destination rectangles by using the Boolean AND operator.

</td>
</tr>
<tr>
<td width="40%"><a id="SRCCOPY"></a><a id="srccopy"></a><dl>
<dt><b>SRCCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the source rectangle directly to the destination rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="SRCERASE"></a><a id="srcerase"></a><dl>
<dt><b>SRCERASE</b></dt>
</dl>
</td>
<td width="60%">
Combines the inverted colors of the destination rectangle with the colors of the source rectangle by using the Boolean AND operator.

</td>
</tr>
<tr>
<td width="40%"><a id="SRCINVERT"></a><a id="srcinvert"></a><dl>
<dt><b>SRCINVERT</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the source and destination rectangles by using the Boolean XOR operator.

</td>
</tr>
<tr>
<td width="40%"><a id="SRCPAINT"></a><a id="srcpaint"></a><dl>
<dt><b>SRCPAINT</b></dt>
</dl>
</td>
<td width="60%">
Combines the colors of the source and destination rectangles by using the Boolean OR operator.

</td>
</tr>
<tr>
<td width="40%"><a id="WHITENESS"></a><a id="whiteness"></a><dl>
<dt><b>WHITENESS</b></dt>
</dl>
</td>
<td width="60%">
Fills the destination rectangle using the color associated with index 1 in the physical palette. (This color is white for the default physical palette.)

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>BitBlt</b> only does clipping on the destination DC.

If a rotation or shear transformation is in effect in the source device context, <b>BitBlt</b> returns an error. If other transformations exist in the source device context (and a matching transformation is not in effect in the destination device context), the rectangle in the destination device context is stretched, compressed, or rotated, as necessary.

If the color formats of the source and destination device contexts do not match, the <b>BitBlt</b> function converts the source color format to match the destination format.

When an enhanced metafile is being recorded, an error occurs if the source device context identifies an enhanced-metafile device context.

Not all devices support the <b>BitBlt</b> function. For more information, see the RC_BITBLT raster capability entry in the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function as well as the following functions: <a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-plgblt">PlgBlt</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>.

<b>BitBlt</b> returns an error if the source and destination device contexts represent different devices. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>. To display the DIB to the second device, call <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

<b>ICM:</b> No color management is performed when blits occur.


#### Examples

The following code example demonstrates the use of **BitBlt**.

```cpp
if (!BitBlt(hdcMemDC,
    0, 0,
    rcClient.right - rcClient.left, rcClient.bottom - rcClient.top,
    hdcWindow,
    0, 0,
    SRCCOPY))
{
    MessageBox(hWnd, L"BitBlt has failed", L"Failed", MB_OK);
    goto done;
}
```

To see this example in context, see <a href="/windows/desktop/gdi/capturing-an-image">Capturing an Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-plgblt">PlgBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>