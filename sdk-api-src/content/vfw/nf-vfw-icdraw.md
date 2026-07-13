---
UID: NF:vfw.ICDraw
title: ICDraw function (vfw.h)
description: The ICDraw function decompresses an image for drawing.
helpviewer_keywords: ["ICDraw","ICDraw function [Windows Multimedia]","_win32_ICDraw","multimedia.icdraw","vfw/ICDraw"]
old-location: multimedia\icdraw.htm
tech.root: Multimedia
ms.assetid: 0bf2c264-6adf-4773-95df-9cd77e73c022
ms.date: 12/05/2018
ms.keywords: ICDraw, ICDraw function [Windows Multimedia], _win32_ICDraw, multimedia.icdraw, vfw/ICDraw
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
 - ICDraw
 - vfw/ICDraw
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
 - ICDraw
---

# ICDraw function


## -description

The <b>ICDraw</b> function decompresses an image for drawing.

## -parameters

### -param hic

Handle to a decompressor.

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
<td><b>ICDRAW_HURRYUP</b></td>
<td>Data is buffered and not drawn to the screen. Use this flag for fastest decompression.</td>
</tr>
<tr>
<td><b>ICDRAW_NOTKEYFRAME</b></td>
<td>Current frame is not a key frame.</td>
</tr>
<tr>
<td><b>ICDRAW_NULLFRAME</b></td>
<td>Current frame does not contain any data and the previous frame should be redrawn.</td>
</tr>
<tr>
<td><b>ICDRAW_PREROLL</b></td>
<td>Current frame of video occurs before playback should start. For example, if playback will begin on frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 are sent to the driver with the <b>ICDRAW_PREROLL</b> flag set. The driver needs this data to display frame 10 properly.</td>
</tr>
<tr>
<td><b>ICDRAW_UPDATE</b></td>
<td>Updates the screen based on previously received data. Set <i>lpData</i> to <b>NULL</b> when this flag is used.</td>
</tr>
</table>

### -param lpFormat

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input format of the data.

### -param lpData

Pointer to the input data.

### -param cbData

Size of the input data, in bytes.

### -param lTime

Time, in samples, to draw this frame. The units for video data are frames. For a definition of the playback rate, see the <b>dwRate</b> and <b>dwScale</b> members of the <a href="/windows/desktop/api/vfw/ns-vfw-icdrawbegin">ICDRAWBEGIN</a> structure.

## -returns

Returns<b> ICERR_OK</b> if successful or an error otherwise.

## -remarks

You can initiate drawing the frames by sending the <a href="/windows/desktop/Multimedia/icm-draw-start">ICM_DRAW_START</a> message (or by using the <a href="/windows/desktop/api/vfw/nf-vfw-icdrawstart">ICDrawStart</a> macro). The application should be sure to buffer the required number of frames before drawing is started. Send the <b>KM_GETBUFFERSWANTED</b> message (or use the <a href="/windows/desktop/api/vfw/nf-vfw-icgetbufferswanted">ICGetBuffersWanted</a> macro) to obtain this value.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>