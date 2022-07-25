---
UID: NF:vfw.DrawDibBegin
title: DrawDibBegin function (vfw.h)
description: The DrawDib function changes parameters of a DrawDib DC or initializes a new DrawDib DC.
helpviewer_keywords: ["DrawDibBegin","DrawDibBegin function [Windows Multimedia]","_win32_DrawDibBegin","multimedia.drawdibbegin","vfw/DrawDibBegin"]
old-location: multimedia\drawdibbegin.htm
tech.root: Multimedia
ms.assetid: 89178e33-e440-49fe-9900-0baea229d289
ms.date: 12/05/2018
ms.keywords: DrawDibBegin, DrawDibBegin function [Windows Multimedia], _win32_DrawDibBegin, multimedia.drawdibbegin, vfw/DrawDibBegin
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawDibBegin
 - vfw/DrawDibBegin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibBegin
---

# DrawDibBegin function


## -description

The <b>DrawDib</b> function changes parameters of a DrawDib DC or initializes a new DrawDib DC.

## -parameters

### -param hdd

Handle to a DrawDib DC.

### -param hdc

Handle to a DC for drawing. This parameter is optional.

### -param dxDst

Width, in <b>MM_TEXT</b> client units, of the destination rectangle.

### -param dyDst

Height, in <b>MM_TEXT</b> client units, of the destination rectangle.

### -param lpbi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the image format. The color table for the DIB follows the image format and the <b>biHeight</b> member must be a positive value.

### -param dxSrc

Width, in pixels, of the source rectangle.

### -param dySrc

Height, in pixels, of the source rectangle.

### -param wFlags

Applicable flags for the function. The following values are defined.
            

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>DDF_ANIMATE</td>
<td>Allows palette animation. If this value is present, DrawDib reserves as many entries as possible by setting <b>PC_RESERVED</b> in the <b>palPalEntry</b> array entries of the <a href="/previous-versions//ms532642(v=vs.85)">LOGPALETTE</a> structure, and the palette can be animated by using the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibchangepalette">DrawDibChangePalette</a> function. If your application uses the <b>DrawDibBegin</b> function with the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a> function, set this value with <b>DrawDibBegin</b> rather than <b>DrawDibDraw</b>.</td>
</tr>
<tr>
<td>DDF_BACKGROUNDPAL</td>
<td>Realizes the palette used for drawing as a background task, leaving the current palette used for the display unchanged. (This value is mutually exclusive of <b>DDF_SAME_HDC</b>.)</td>
</tr>
<tr>
<td>DDF_BUFFER</td>
<td>Causes DrawDib to try to use an off-screen buffer so <b>DDF_UPDATE</b> can be used. This disables decompression and drawing directly to the screen. If DrawDib is unable to create an off-screen buffer, it will decompress or draw directly to the screen. For more information, see the <b>DDF_UPDATE</b> and <b>DDF_DONTDRAW</b> values described for <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a>.</td>
</tr>
<tr>
<td>DDF_DONTDRAW</td>
<td>Current image is not drawn, but is decompressed. <b>DDF_UPDATE</b> can be used later to draw the image. This flag supersedes the <b>DDF_PREROLL</b> flag.</td>
</tr>
<tr>
<td>DDF_FULLSCREEN</td>
<td>Not supported.</td>
</tr>
<tr>
<td>DDF_HALFTONE</td>
<td>Always dithers the DIB to a standard palette regardless of the palette of the DIB. If your application uses <b>DrawDibBegin</b> with <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a>, set this value with <b>DrawDibBegin</b> rather than <b>DrawDibDraw</b>.</td>
</tr>
<tr>
<td>DDF_JUSTDRAWIT</td>
<td>Draws the image by using GDI. Prohibits DrawDib functions from decompressing, stretching, or dithering the image. This strips DrawDib of capabilities that differentiate it from the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> function.</td>
</tr>
<tr>
<td>DDF_SAME_DRAW</td>
<td>Use the current drawing parameters for <a href="/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a>. Use this value only if <i>lpbi</i>, <i>dxDest</i>, <i>dyDest</i>, <i>dxSrc</i>, and <i>dySrc</i> have not changed since using <b>DrawDibDraw</b> or <b>DrawDibBegin</b>. This flag supersedes the <b>DDF_SAME_DIB</b> and <b>DDF_SAME_SIZE</b> flags.</td>
</tr>
<tr>
<td>DDF_SAME_HDC</td>
<td>Use the current DC handle and the palette currently associated with the DC.</td>
</tr>
<tr>
<td>DDF_UPDATE</td>
<td>Last buffered bitmap needs to be redrawn. If drawing fails with this value, a buffered image is not available and a new image needs to be specified before the display can be updated.</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

This function prepares to draw a DIB specified by <i>lpbi</i> to the DC. The image is stretched to the size specified by <i>dxDest</i> and <i>dyDest</i>. If <i>dxDest</i> and <i>dyDest</i> are set to −1, the DIB is drawn to a 1:1 scale without stretching.

You can update the flags of a DrawDib DC by reissuing <b>DrawDibBegin</b>, specifying the new flags, and changing at least one of the following settings: <i>dxDest</i>, <i>dyDest</i>, <i>lpbi</i>, <i>dxSrc</i>, or <i>dySrc</i>.

If the parameters of <b>DrawDibBegin</b> have not changed, subsequent calls to the function have no effect.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>