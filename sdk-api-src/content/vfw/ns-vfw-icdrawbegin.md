---
UID: NS:vfw.ICDRAWBEGIN
title: ICDRAWBEGIN (vfw.h)
description: The ICDRAWBEGIN structure contains decompression parameters used with the ICM_DRAW_BEGIN message.
helpviewer_keywords: ["ICDRAWBEGIN","ICDRAWBEGIN structure [Windows Multimedia]","ICDRAW_ANIMATE","ICDRAW_BUFFER","ICDRAW_CONTINUE","ICDRAW_FULLSCREEN","ICDRAW_HDC","ICDRAW_MEMORYDC","ICDRAW_QUERY","ICDRAW_RENDER","ICDRAW_UPDATING","multimedia.icdrawbegin_COLLISION9","multimedia.icdrawbegin_struct","vfw/ICDRAWBEGIN"]
old-location: multimedia\icdrawbegin_struct.htm
tech.root: Multimedia
ms.assetid: 1ec2309c-7ea8-423e-aee3-5e0c650f0b3d
ms.date: 12/05/2018
ms.keywords: ICDRAWBEGIN, ICDRAWBEGIN structure [Windows Multimedia], ICDRAW_ANIMATE, ICDRAW_BUFFER, ICDRAW_CONTINUE, ICDRAW_FULLSCREEN, ICDRAW_HDC, ICDRAW_MEMORYDC, ICDRAW_QUERY, ICDRAW_RENDER, ICDRAW_UPDATING, multimedia.icdrawbegin_COLLISION9, multimedia.icdrawbegin_struct, vfw/ICDRAWBEGIN
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ICDRAWBEGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDRAWBEGIN
 - vfw/ICDRAWBEGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDRAWBEGIN
---

# ICDRAWBEGIN structure


## -description

The <b>ICDRAWBEGIN</b> structure contains decompression parameters used with the <a href="/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a> message.

## -struct-fields

### -field dwFlags

Applicable flags. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_ANIMATE"></a><a id="icdraw_animate"></a><dl>
<dt><b>ICDRAW_ANIMATE</b></dt>
</dl>
</td>
<td width="60%">
Application can animate the palette.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_BUFFER"></a><a id="icdraw_buffer"></a><dl>
<dt><b>ICDRAW_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Buffers this data off-screen; it will need to be updated.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_CONTINUE"></a><a id="icdraw_continue"></a><dl>
<dt><b>ICDRAW_CONTINUE</b></dt>
</dl>
</td>
<td width="60%">
Drawing is a continuation of the previous frame.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_FULLSCREEN"></a><a id="icdraw_fullscreen"></a><dl>
<dt><b>ICDRAW_FULLSCREEN</b></dt>
</dl>
</td>
<td width="60%">
Draws the decompressed data on the full screen.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_HDC"></a><a id="icdraw_hdc"></a><dl>
<dt><b>ICDRAW_HDC</b></dt>
</dl>
</td>
<td width="60%">
Draws the decompressed data to a window or a DC.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_MEMORYDC"></a><a id="icdraw_memorydc"></a><dl>
<dt><b>ICDRAW_MEMORYDC</b></dt>
</dl>
</td>
<td width="60%">
DC is off-screen.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_QUERY"></a><a id="icdraw_query"></a><dl>
<dt><b>ICDRAW_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Determines if the decompressor can handle the decompression. The driver does not actually decompress the data.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_RENDER"></a><a id="icdraw_render"></a><dl>
<dt><b>ICDRAW_RENDER</b></dt>
</dl>
</td>
<td width="60%">
Renders but does not draw the data.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_UPDATING"></a><a id="icdraw_updating"></a><dl>
<dt><b>ICDRAW_UPDATING</b></dt>
</dl>
</td>
<td width="60%">
Current frame is being updated rather than played.
              

</td>
</tr>
</table>

### -field hpal

Handle to the palette used for drawing.

### -field hwnd

Handle to the window used for drawing.

### -field hdc

Handle to the DC used for drawing. Specify <b>NULL</b> to use a DC associated with the specified window.

### -field xDst

The x-coordinate of the destination rectangle.

### -field yDst

The y-coordinate of the destination rectangle.

### -field dxDst

Width of the destination rectangle.

### -field dyDst

Height of the destination rectangle.

### -field lpbi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input format.

### -field xSrc

The x-coordinate of the source rectangle.

### -field ySrc

The y-coordinate of the source rectangle.

### -field dxSrc

Width of the source rectangle.

### -field dySrc

Height of the source rectangle.

### -field dwRate

Decompression rate in an integer format. To obtain the rate in frames per second, divide this value by the value in <b>dwScale</b>.

### -field dwScale

Value used to scale <b>dwRate</b> to frames per second.

## -see-also

<a href="/windows/desktop/Multimedia/icm-draw-begin">ICM_DRAW_BEGIN</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

