---
UID: NF:vfw.ICDrawSuggestFormat
title: ICDrawSuggestFormat function (vfw.h)
description: The ICDrawSuggestFormat function notifies the drawing handler to suggest the input data format.
helpviewer_keywords: ["ICDrawSuggestFormat","ICDrawSuggestFormat function [Windows Multimedia]","_win32_ICDrawSuggestFormat","multimedia.icdrawsuggestformat","vfw/ICDrawSuggestFormat"]
old-location: multimedia\icdrawsuggestformat.htm
tech.root: Multimedia
ms.assetid: 748d09a6-52db-4bd0-9006-6ee96f07a74b
ms.date: 12/05/2018
ms.keywords: ICDrawSuggestFormat, ICDrawSuggestFormat function [Windows Multimedia], _win32_ICDrawSuggestFormat, multimedia.icdrawsuggestformat, vfw/ICDrawSuggestFormat
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
 - ICDrawSuggestFormat
 - vfw/ICDrawSuggestFormat
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
 - ICDrawSuggestFormat
---

# ICDrawSuggestFormat function


## -description

The <b>ICDrawSuggestFormat</b> function notifies the drawing handler to suggest the input data format.

## -parameters

### -param hic

Handle to the driver to use.

### -param lpbiIn

Pointer to a structure containing the format of the compressed data. For bitmaps, this is a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

### -param lpbiOut

Pointer to a structure to return the suggested format. The drawing handler can receive and draw data from this format. For bitmaps, this is a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

### -param dxSrc

Width of the source rectangle.

### -param dySrc

Height of the source rectangle.

### -param dxDst

Width of the destination rectangle.

### -param dyDst

Height of the destination rectangle.

### -param hicDecomp

Decompressor that can use the format of data in <i>lpbiIn</i>.

## -returns

Returns <b>ICERR_OK</b> if successful or an error otherwise.

## -remarks

Applications can use this function to determine alternative input formats that a drawing handler can decompress and if the drawing handler can stretch data. If the drawing handler cannot stretch data as requested, the application might have to stretch the data.

If the drawing handler cannot decompress a format provided by an application, use the <a href="/windows/desktop/api/vfw/nf-vfw-icdecompress">ICDecompress</a>, <a href="/windows/desktop/api/vfw/nf-vfw-icdecompressex">ICDecompressEx</a>, j, <a href="/windows/desktop/api/vfw/nf-vfw-icdecompressexquery">ICDecompressExQuery</a>, and <a href="/windows/desktop/api/vfw/nf-vfw-icdecompressopen">ICDecompressOpen</a> functions to obtain alternate formats.

## -see-also

<a href="/windows/desktop/api/vfw/nf-vfw-icdecompressex">ICDecompressEx</a>



<a href="/windows/desktop/api/vfw/nf-vfw-icdecompressexbegin">ICDecompressExBegin</a>



<a href="/windows/desktop/api/vfw/nf-vfw-icdecompressexquery">ICDecompressExQuery</a>



<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>