---
UID: NF:vfw.ICDrawBegin
title: ICDrawBegin function (vfw.h)
description: The ICDrawBegin function initializes the renderer and prepares the drawing destination for drawing.
helpviewer_keywords: ["ICDrawBegin","ICDrawBegin function [Windows Multimedia]","_win32_ICDrawBegin","multimedia.icdrawbegin","vfw/ICDrawBegin"]
old-location: multimedia\icdrawbegin.htm
tech.root: Multimedia
ms.assetid: 52a43888-9839-45a3-b139-e84943c345c2
ms.date: 12/05/2018
ms.keywords: ICDrawBegin, ICDrawBegin function [Windows Multimedia], _win32_ICDrawBegin, multimedia.icdrawbegin, vfw/ICDrawBegin
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
 - ICDrawBegin
 - vfw/ICDrawBegin
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
 - ICDrawBegin
---

# ICDrawBegin function


## -description

The <b>ICDrawBegin</b> function initializes the renderer and prepares the drawing destination for drawing.

## -parameters

### -param hic

Handle to the decompressor to use.

### -param dwFlags

Decompression flags. The following values are defined.
            

<table>
<tr>
<th>Value
                </th>
<th>Meaning
                </th>
</tr>
<tr>
<td><b>ICDRAW_ANIMATE</b></td>
<td>Application can animate the palette.</td>
</tr>
<tr>
<td><b>ICDRAW_CONTINUE</b></td>
<td>Drawing is a continuation of the previous frame.</td>
</tr>
<tr>
<td><b>ICDRAW_FULLSCREEN</b></td>
<td>Draws the decompressed data on the full screen.</td>
</tr>
<tr>
<td><b>ICDRAW_HDC</b></td>
<td>Draws the decompressed data to a window or a DC.</td>
</tr>
<tr>
<td><b>ICDRAW_MEMORYDC</b></td>
<td>DC is off-screen.</td>
</tr>
<tr>
<td><b>ICDRAW_QUERY</b></td>
<td>Determines if the decompressor can decompress the data. The driver does not decompress the data.</td>
</tr>
<tr>
<td><b>ICDRAW_UPDATING</b></td>
<td>Current frame is being updated rather than played.</td>
</tr>
</table>

### -param hpal

Handle to the palette used for drawing.

### -param hwnd

Handle to the window used for drawing.

### -param hdc

DC used for drawing.

### -param xDst

The x-coordinate of the upper right corner of the destination rectangle.

### -param yDst

The y-coordinate of the upper right corner of the destination rectangle.

### -param dxDst

Width of the destination rectangle.

### -param dyDst

Height of the destination rectangle.

### -param lpbi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the format of the input data to be decompressed.

### -param xSrc

The x-coordinate of the upper right corner of the source rectangle.

### -param ySrc

The y-coordinate of the upper right corner of the source rectangle.

### -param dxSrc

Width of the source rectangle.

### -param dySrc

Height of the source rectangle.

### -param dwRate

Frame rate numerator. The frame rate, in frames per second, is obtained by dividing <i>dwRate</i> by <i>dwScale</i>.

### -param dwScale

Frame rate denominator. The frame rate, in frames per second, is obtained by dividing <i>dwRate</i> by <i>dwScale</i>.

## -returns

Returns ICERR_OK if the renderer can decompress the data or <b>ICERR_UNSUPPORTED</b> otherwise.

## -remarks

The <b>ICDRAW_HDC</b> and <b>ICDRAW_FULLSCREEN</b> flags are mutually exclusive. If an application sets the ICDRAW_HDC flag in dwFlags, the decompressor uses <i>hwnd</i>, <i>hdc</i>, and the parameters defining the destination rectangle (<i>xDst</i>, <i>yDst</i>, <i>dxDst</i>, and <i>dyDst)</i>. Your application should set these parameters to the size of the destination rectangle. Specify destination rectangle values relative to the current window or DC.

If an application sets the <b>ICDRAW_FULLSCREEN</b> flag in <i>dwFlags</i>, the <i>hwnd</i> and <i>hdc</i> parameters are not used and should be set to <b>NULL</b>. Also, the destination rectangle is not used and its parameters can be set to zero.

The source rectangle is relative to the full video frame. The portion of the video frame specified by the source rectangle is stretched or shrunk to fit the destination rectangle.

The <i>dwRate</i> and <i>dwScale</i> parameters specify the decompression rate. The integer value specified for <i>dwRate</i> divided by the integer value specified for <i>dwScale</i> defines the frame rate in frames per second. This value is used by the renderer when it is responsible for timing frames during playback.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>