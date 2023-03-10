---
UID: NF:vfw.ICDecompressExQuery
title: ICDecompressExQuery function (vfw.h)
description: The ICDecompressExQuery function determines if a decompressor can decompress data with a specific format.
helpviewer_keywords: ["ICDecompressExQuery","ICDecompressExQuery function [Windows Multimedia]","_win32_ICDecompressExQuery","multimedia.icdecompressexquery","vfw/ICDecompressExQuery"]
old-location: multimedia\icdecompressexquery.htm
tech.root: Multimedia
ms.assetid: 6a1aa686-7f3d-43be-baaa-d20ea4a33f9b
ms.date: 12/05/2018
ms.keywords: ICDecompressExQuery, ICDecompressExQuery function [Windows Multimedia], _win32_ICDecompressExQuery, multimedia.icdecompressexquery, vfw/ICDecompressExQuery
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
 - ICDecompressExQuery
 - vfw/ICDecompressExQuery
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
 - ICDecompressExQuery
---

# ICDecompressExQuery function


## -description

The <b>ICDecompressExQuery</b> function determines if a decompressor can decompress data with a specific format.

## -parameters

### -param hic

Handle to the decompressor to use.

### -param dwFlags

Reserved; do not use.

### -param lpbiSrc

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the format of the compressed data to decompress.

### -param lpSrc

Reserved; must be <b>NULL</b>.

### -param xSrc

The x-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.

### -param ySrc

The y-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.

### -param dxSrc

Width of the source rectangle.

### -param dySrc

Height of the source rectangle.

### -param lpbiDst

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the output format. If the value of this parameter is <b>NULL</b>, the function determines whether the input format is supported and this parameter is ignored.

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