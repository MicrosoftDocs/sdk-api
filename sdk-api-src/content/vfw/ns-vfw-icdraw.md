---
UID: NS:vfw.ICDRAW
title: ICDRAW (vfw.h)
description: The ICDRAW structure contains parameters for drawing video data to the screen. This structure is used with the ICM_DRAW message.
helpviewer_keywords: ["ICDRAW","ICDRAW structure [Windows Multimedia]","ICDRAW_HURRYUP","ICDRAW_NOTKEYFRAME","ICDRAW_NULLFRAME","ICDRAW_PREROLL","ICDRAW_UPDATE","multimedia.icdraw_COLLISION9","multimedia.icdraw_struct","vfw/ICDRAW"]
old-location: multimedia\icdraw_struct.htm
tech.root: Multimedia
ms.assetid: 9b3e2788-176c-41be-8ae3-244ed93ff4f8
ms.date: 12/05/2018
ms.keywords: ICDRAW, ICDRAW structure [Windows Multimedia], ICDRAW_HURRYUP, ICDRAW_NOTKEYFRAME, ICDRAW_NULLFRAME, ICDRAW_PREROLL, ICDRAW_UPDATE, multimedia.icdraw_COLLISION9, multimedia.icdraw_struct, vfw/ICDRAW
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
req.typenames: ICDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDRAW
 - vfw/ICDRAW
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
 - ICDRAW
---

# ICDRAW structure


## -description

The <b>ICDRAW</b> structure contains parameters for drawing video data to the screen. This structure is used with the <a href="/windows/desktop/Multimedia/icm-draw">ICM_DRAW</a> message.

## -struct-fields

### -field dwFlags

Flags from the AVI file index. The following values are defined:
          

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_HURRYUP"></a><a id="icdraw_hurryup"></a><dl>
<dt><b>ICDRAW_HURRYUP</b></dt>
</dl>
</td>
<td width="60%">
Data is buffered and not drawn to the screen. Use this flag for fastest decompression.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_NOTKEYFRAME"></a><a id="icdraw_notkeyframe"></a><dl>
<dt><b>ICDRAW_NOTKEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
Current frame is not a key frame.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_NULLFRAME"></a><a id="icdraw_nullframe"></a><dl>
<dt><b>ICDRAW_NULLFRAME</b></dt>
</dl>
</td>
<td width="60%">
Current frame does not contain any data, and the previous frame should be redrawn.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_PREROLL"></a><a id="icdraw_preroll"></a><dl>
<dt><b>ICDRAW_PREROLL</b></dt>
</dl>
</td>
<td width="60%">
Current frame of video occurs before playback should start. For example, if playback will begin on frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 are sent to the driver with this flag set. The driver needs this data to display frame 10 properly.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDRAW_UPDATE"></a><a id="icdraw_update"></a><dl>
<dt><b>ICDRAW_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Updates the screen based on data previously received. In this case, <b>lpData</b> should be ignored.
              

</td>
</tr>
</table>

### -field lpFormat

Pointer to a structure containing the data format. For video streams, this is a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

### -field lpData

Pointer to the data to render.

### -field cbData

Number of data bytes to render.

### -field lTime

Time, in samples, when this data should be drawn. For video data this is normally a frame number.

## -see-also

<a href="/windows/desktop/Multimedia/icm-draw">ICM_DRAW</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

