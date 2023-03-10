---
UID: NF:vfw.ICCompress
title: ICCompress function (vfw.h)
description: The ICCompress function compresses a single video image.
helpviewer_keywords: ["AVIIF_KEYFRAME","ICCOMPRESS_KEYFRAME","ICCompress","ICCompress function [Windows Multimedia]","_win32_ICCompress","multimedia.iccompress","vfw/ICCompress"]
old-location: multimedia\iccompress.htm
tech.root: Multimedia
ms.assetid: 99e7d87a-cbf5-42d3-897c-5f5c8860a13a
ms.date: 12/05/2018
ms.keywords: AVIIF_KEYFRAME, ICCOMPRESS_KEYFRAME, ICCompress, ICCompress function [Windows Multimedia], _win32_ICCompress, multimedia.iccompress, vfw/ICCompress
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
 - ICCompress
 - vfw/ICCompress
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
 - ICCompress
---

# ICCompress function


## -description

The <b>ICCompress</b> function compresses a single video image.

## -parameters

### -param hic

Handle to the compressor to use.

### -param dwFlags

Compression flag. The following value is defined:
          



#### ICCOMPRESS_KEYFRAME

Compressor should make this frame a key frame.

### -param lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the output format.

### -param lpData

Pointer to an output buffer large enough to contain a compressed frame.

### -param lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input format.

### -param lpBits

Pointer to the input buffer.

### -param lpckid

Reserved; do not use.

### -param lpdwFlags

Pointer to the return flags used in the AVI index. The following value is defined:
          



#### AVIIF_KEYFRAME

Current frame is a key frame.

### -param lFrameNum

Frame number.

### -param dwFrameSize

Requested frame size, in bytes. Specify a nonzero value if the compressor supports a suggested frame size, as indicated by the presence of the <b>VIDCF_CRUNCH</b> flag returned by the <a href="/windows/desktop/api/vfw/nf-vfw-icgetinfo">ICGetInfo</a> function. If this flag is not set or a data rate for the frame is not specified, specify zero for this parameter.

A compressor might have to sacrifice image quality or make some other trade-off to obtain the size goal specified in this parameter.

### -param dwQuality

Requested quality value for the frame. Specify a nonzero value if the compressor supports a suggested quality value, as indicated by the presence of the <b>VIDCF_QUALITY</b> flag returned by <a href="/windows/desktop/api/vfw/nf-vfw-icgetinfo">ICGetInfo</a>. Otherwise, specify zero for this parameter.

### -param lpbiPrev

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the format of the previous frame.

### -param lpPrev

Pointer to the uncompressed image of the previous frame. This parameter is not used for fast temporal compression. Specify <b>NULL</b> for this parameter when compressing a key frame, if the compressor does not support temporal compression, or if the compressor does not require an external buffer to store the format and data of the previous image.

## -returns

Returns <b>ICERR_OK</b> if successful or an error otherwise.

## -remarks

You can obtain the required by size of the output buffer by sending the <a href="/windows/desktop/Multimedia/icm-compress-get-size">ICM_COMPRESS_GET_SIZE</a> message (or by using the <a href="/windows/desktop/api/vfw/nf-vfw-iccompressgetsize">ICCompressGetSize</a> macro).

The compressor sets the contents of <i>lpdwFlags</i> to <b>AVIIF_KEYFRAME</b> when it creates a key frame. If your application creates AVI files, it should save the information returned for <i>lpckid</i> and <i>lpdwFlags</i> in the file.

Compressors use <i>lpbiPrev</i> and <i>lpPrev</i> to perform temporal compression and require an external buffer to store the format and data of the previous frame. Specify <b>NULL</b> for <i>lpbiPrev</i> and <i>lpPrev</i> when compressing a key frame, when performing fast compression, or if the compressor has its own buffer to store the format and data of the previous image. Specify non-<b>NULL</b> values for these parameters if <a href="/windows/desktop/api/vfw/nf-vfw-icgetinfo">ICGetInfo</a> returns the <b>VIDCF_TEMPORAL</b> flag, the compressor is performing normal compression, and the frame to compress is not a key frame.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>