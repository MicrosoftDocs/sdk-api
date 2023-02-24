---
UID: NS:vfw.ICDECOMPRESS
title: ICDECOMPRESS (vfw.h)
description: The ICDECOMPRESS structure contains decompression parameters used with the ICM_DECOMPRESS message.
helpviewer_keywords: ["ICDECOMPRESS","ICDECOMPRESS structure [Windows Multimedia]","ICDECOMPRESS_HURRYUP","ICDECOMPRESS_NOTKEYFRAME","ICDECOMPRESS_NULLFRAME","ICDECOMPRESS_PREROLL","ICDECOMPRESS_UPDATE","multimedia.icdecompress_COLLISION813","multimedia.icdecompress_struct","vfw/ICDECOMPRESS"]
old-location: multimedia\icdecompress_struct.htm
tech.root: Multimedia
ms.assetid: bc9c2416-cc1c-4571-82ee-7d93307f5114
ms.date: 12/05/2018
ms.keywords: ICDECOMPRESS, ICDECOMPRESS structure [Windows Multimedia], ICDECOMPRESS_HURRYUP, ICDECOMPRESS_NOTKEYFRAME, ICDECOMPRESS_NULLFRAME, ICDECOMPRESS_PREROLL, ICDECOMPRESS_UPDATE, multimedia.icdecompress_COLLISION813, multimedia.icdecompress_struct, vfw/ICDECOMPRESS
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
req.typenames: ICDECOMPRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDECOMPRESS
 - vfw/ICDECOMPRESS
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
 - ICDECOMPRESS
---

# ICDECOMPRESS structure


## -description

The <b>ICDECOMPRESS</b> structure contains decompression parameters used with the <a href="/windows/desktop/Multimedia/icm-decompress">ICM_DECOMPRESS</a> message.

## -struct-fields

### -field dwFlags

Applicable flags. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_HURRYUP"></a><a id="icdecompress_hurryup"></a><dl>
<dt><b>ICDECOMPRESS_HURRYUP</b></dt>
</dl>
</td>
<td width="60%">
Tries to decompress at a faster rate. When an application uses this flag, the driver should buffer the decompressed data but not draw the image.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_NOTKEYFRAME"></a><a id="icdecompress_notkeyframe"></a><dl>
<dt><b>ICDECOMPRESS_NOTKEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
Current frame is not a key frame.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_NULLFRAME"></a><a id="icdecompress_nullframe"></a><dl>
<dt><b>ICDECOMPRESS_NULLFRAME</b></dt>
</dl>
</td>
<td width="60%">
Current frame does not contain data and the decompressed image should be left the same.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_PREROLL"></a><a id="icdecompress_preroll"></a><dl>
<dt><b>ICDECOMPRESS_PREROLL</b></dt>
</dl>
</td>
<td width="60%">
Current frame precedes the point in the movie where playback starts and, therefore, will not be drawn.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_UPDATE"></a><a id="icdecompress_update"></a><dl>
<dt><b>ICDECOMPRESS_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Screen is being updated or refreshed.
              

</td>
</tr>
</table>

### -field lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input format.

### -field lpInput

Pointer to a buffer containing the input data.

### -field lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the output format.

### -field lpOutput

Pointer to a buffer where the driver should write the decompressed image.

### -field ckid

Chunk identifier from the AVI file.

## -see-also

<a href="/previous-versions//ms532290(v=vs.85)">BITMAPINFOHEADER</a>



<a href="/windows/desktop/Multimedia/icm-decompress">ICM_DECOMPRESS</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

