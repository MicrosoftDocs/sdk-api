---
UID: NF:vfw.ICDecompressExBegin
title: ICDecompressExBegin function (vfw.h)
description: The ICDecompressExBegin function prepares a decompressor for decompressing data.
helpviewer_keywords: ["ICDecompressExBegin","ICDecompressExBegin function [Windows Multimedia]","_win32_ICDecompressExBegin","multimedia.icdecompressexbegin","vfw/ICDecompressExBegin"]
old-location: multimedia\icdecompressexbegin.htm
tech.root: Multimedia
ms.assetid: 35277938-6fae-4207-8b91-439af2b481e8
ms.date: 12/05/2018
ms.keywords: ICDecompressExBegin, ICDecompressExBegin function [Windows Multimedia], _win32_ICDecompressExBegin, multimedia.icdecompressexbegin, vfw/ICDecompressExBegin
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDecompressExBegin
 - vfw/ICDecompressExBegin
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
 - ICDecompressExBegin
---

# ICDecompressExBegin function


## -description

The <b>ICDecompressExBegin</b> function prepares a decompressor for decompressing data.

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
<td><b>ICDECOMPRESS_HURRYUP</b></td>
<td>Tries to decompress at a faster rate. When an application uses this flag, the driver should buffer the decompressed data but not draw the image.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_NOTKEYFRAME</b></td>
<td>Current frame is not a key frame.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_NULLFRAME</b></td>
<td>Current frame does not contain data and the decompressed image should be left the same.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_PREROLL</b></td>
<td>Current frame precedes the point in the movie where playback starts and, therefore, will not be drawn.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_UPDATE</b></td>
<td>Screen is being updated or refreshed.</td>
</tr>
</table>

### -param lpbiSrc

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the format of the compressed data.

### -param lpSrc

Pointer to the input data.

### -param xSrc

The x-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.

### -param ySrc

The y-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.

### -param dxSrc

Width of the source rectangle.

### -param dySrc

Height of the source rectangle.

### -param lpbiDst

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the output format.

### -param lpDst

Pointer to a buffer that is large enough to contain the decompressed data.

### -param xDst

The x-coordinate of the destination rectangle for the DIB specified by <i>lpbiDst</i>.

### -param yDst

The y-coordinate of the destination rectangle for the DIB specified by <i>lpbiDst</i>.

### -param dxDst

Width of the destination rectangle.

### -param dyDst

Height of the destination rectangle.

## -returns

Returns <b>ICERR_OK</b> if successful or an error otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>