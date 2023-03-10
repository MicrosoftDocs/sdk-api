---
UID: NS:vfw.ICCOMPRESS
title: ICCOMPRESS (vfw.h)
description: The ICCOMPRESS structure contains compression parameters used with the ICM_COMPRESS message.
helpviewer_keywords: ["ICCOMPRESS","ICCOMPRESS structure [Windows Multimedia]","ICCOMPRESS_KEYFRAME","multimedia.iccompress_COLLISION455","multimedia.iccompress_struct","vfw/ICCOMPRESS"]
old-location: multimedia\iccompress_struct.htm
tech.root: Multimedia
ms.assetid: ba6aec9c-b622-484b-88ce-ff5c659bd6d7
ms.date: 12/05/2018
ms.keywords: ICCOMPRESS, ICCOMPRESS structure [Windows Multimedia], ICCOMPRESS_KEYFRAME, multimedia.iccompress_COLLISION455, multimedia.iccompress_struct, vfw/ICCOMPRESS
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
req.typenames: ICCOMPRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICCOMPRESS
 - vfw/ICCOMPRESS
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
 - ICCOMPRESS
---

# ICCOMPRESS structure


## -description

The <b>ICCOMPRESS</b> structure contains compression parameters used with the <a href="/windows/desktop/Multimedia/icm-compress">ICM_COMPRESS</a> message.

## -struct-fields

### -field dwFlags

Flags used for compression. The following value is defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICCOMPRESS_KEYFRAME"></a><a id="iccompress_keyframe"></a><dl>
<dt><b>ICCOMPRESS_KEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
Input data should be treated as a key frame.

</td>
</tr>
</table>

### -field lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the output (compressed) format. The <b>biSizeImage</b> member must contain the size of the compressed data.

### -field lpOutput

Pointer to the buffer where the driver should write the compressed data.

### -field lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input (uncompressed) format.

### -field lpInput

Pointer to the buffer containing input data.

### -field lpckid

Address to contain the chunk identifier for data in the AVI file. If the value of this member is not <b>NULL</b>, the driver should specify a two-character code for the chunk identifier corresponding to the chunk identifier used in the AVI file.

### -field lpdwFlags

Address to contain flags for the AVI index. If the returned frame is a key frame, the driver should set the <b>AVIIF_KEYFRAME</b> flag.

### -field lFrameNum

Number of the frame to compress.

### -field dwFrameSize

Desired maximum size, in bytes, for compressing this frame. The size value is used for compression methods that can make tradeoffs between compressed image size and image quality. Specify zero for this member to use the default setting.

### -field dwQuality

Quality setting.

### -field lpbiPrev

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the format of the previous frame, which is typically the same as the input format.

### -field lpPrev

Pointer to the buffer containing input data of the previous frame.

## -remarks

Drivers that perform temporal compression use data from the previous frame (found in the <b>lpbiPrev</b> and <b>lpPrev</b> members) to prune redundant data from the current frame.

## -see-also

<a href="/windows/desktop/Multimedia/icm-compress">ICM_COMPRESS</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

