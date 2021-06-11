---
UID: NF:vfw.DrawDibDraw
title: DrawDibDraw function (vfw.h)
description: The DrawDibDraw function draws a DIB to the screen.
helpviewer_keywords: ["DrawDibDraw","DrawDibDraw function [Windows Multimedia]","_win32_DrawDibDraw","multimedia.drawdibdraw","vfw/DrawDibDraw"]
old-location: multimedia\drawdibdraw.htm
tech.root: Multimedia
ms.assetid: b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4
ms.date: 12/05/2018
ms.keywords: DrawDibDraw, DrawDibDraw function [Windows Multimedia], _win32_DrawDibDraw, multimedia.drawdibdraw, vfw/DrawDibDraw
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
 - DrawDibDraw
 - vfw/DrawDibDraw
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
 - DrawDibDraw
---

# DrawDibDraw function


## -description

The <b>DrawDibDraw</b> function draws a DIB to the screen.

## -parameters

### -param hdd

Handle to a DrawDib DC.

### -param hdc

Handle to the DC.

### -param xDst

The x-coordinate, in <b>MM_TEXT</b> client coordinates, of the upper left corner of the destination rectangle.

### -param yDst

The y-coordinate, in <b>MM_TEXT</b> client coordinates, of the upper left corner of the destination rectangle.

### -param dxDst

Width, in <b>MM_TEXT</b> client coordinates, of the destination rectangle. If <i>dxDst</i> is −1, the width of the bitmap is used.

### -param dyDst

Height, in <b>MM_TEXT</b> client coordinates, of the destination rectangle. If <i>dyDst</i> is −1, the height of the bitmap is used.

### -param lpbi

Pointer to the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the image format. The color table for the DIB within <b>BITMAPINFOHEADER</b> follows the format and the <b>biHeight</b> member must be a positive value; <b>DrawDibDraw</b> will not draw inverted DIBs.

### -param lpBits

Pointer to the buffer that contains the bitmap bits.

### -param xSrc

The x-coordinate, in pixels, of the upper left corner of the source rectangle. The coordinates (0,0) represent the upper left corner of the bitmap.

### -param ySrc

The y-coordinate, in pixels, of the upper left corner of the source rectangle. The coordinates (0,0) represent the upper left corner of the bitmap.

### -param dxSrc

Width, in pixels, of the source rectangle.

### -param dySrc

Height, in pixels, of the source rectangle.

### -param wFlags

Applicable flags for drawing. The following values are defined.
            

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td><b>DDF_BACKGROUNDPAL</b></td>
<td>Realizes the palette used for drawing in the background, leaving the actual palette used for display unchanged. This value is valid only if <b>DDF_SAME_HDC</b> is not set.</td>
</tr>
<tr>
<td><b>DDF_DONTDRAW</b></td>
<td>Current image is decompressed but not drawn. This flag supersedes the <b>DDF_PREROLL</b> flag.</td>
</tr>
<tr>
<td><b>DDF_FULLSCREEN</b></td>
<td>Not supported.</td>
</tr>
<tr>
<td><b>DDF_HALFTONE</b></td>
<td>Always dithers the DIB to a standard palette regardless of the palette of the DIB. If your application uses the <a href="/windows/desktop/api/vfw/nf-vfw-drawdibbegin">DrawDibBegin</a> function, set this value in <b>DrawDibBegin</b> rather than in <b>DrawDibDraw</b>.</td>
</tr>
<tr>
<td><b>DDF_HURRYUP</b></td>
<td>Data does not have to be drawn (that is, it can be dropped) and <b>DDF_UPDATE</b> will not be used to recall this information. DrawDib checks this value only if it is required to build the next frame; otherwise, the value is ignored.This value is usually used to synchronize video and audio. When synchronizing data, applications should send the image with this value in case the driver needs to buffer the frame to decompress subsequent frames.

</td>
</tr>
<tr>
<td><b>DDF_NOTKEYFRAME</b></td>
<td>DIB data is not a key frame.</td>
</tr>
<tr>
<td><b>DDF_SAME_HDC</b></td>
<td>Use the current DC handle and the palette currently associated with the DC.</td>
</tr>
<tr>
<td><b>DDF_SAME_DRAW</b></td>
<td>Use the current drawing parameters for <b>DrawDibDraw</b>. Use this value only if <i>lpbi</i>, <i>dxDst</i>, <i>dyDst</i>, <i>dxSrc</i>, and <i>dySrc</i> have not changed since using <b>DrawDibDraw</b> or <a href="/windows/desktop/api/vfw/nf-vfw-drawdibbegin">DrawDibBegin</a>. <b>DrawDibDraw</b> typically checks the parameters, and if they have changed, <b>DrawDibBegin</b> prepares the DrawDib DC for drawing. This flag supersedes the <b>DDF_SAME_DIB</b> and <b>DDF_SAME_SIZE</b> flags.</td>
</tr>
<tr>
<td><b>DDF_UPDATE</b></td>
<td>Last buffered bitmap is to be redrawn. If drawing fails with this value, a buffered image is not available and a new image needs to be specified before the display can be updated.</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

<b>DDF_DONTDRAW</b> causes <b>DrawDibDraw</b> to decompress but not display an image. A subsequent call to <b>DrawDibDraw</b> specifying <b>DDF_UPDATE</b> displays the image.

If the DrawDib DC does not have an off-screen buffer specified, specifying <b>DDF_DONTDRAW</b> causes the frame to be drawn to the screen immediately. Subsequent calls to <b>DrawDibDraw</b> specifying <b>DDF_UPDATE</b> fail.

Although they are set at different times, <b>DDF_UPDATE</b> and <b>DDF_DONTDRAW</b> can be used together to create composite images off-screen. When the off-screen image is complete, you can display the image by calling <b>DrawDibDraw</b>.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>