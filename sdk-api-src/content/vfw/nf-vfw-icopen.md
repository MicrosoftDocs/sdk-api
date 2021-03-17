---
UID: NF:vfw.ICOpen
title: ICOpen function (vfw.h)
description: The ICOpen function opens a compressor or decompressor.
helpviewer_keywords: ["ICOpen","ICOpen function [Windows Multimedia]","_win32_ICOpen","multimedia.icopen","vfw/ICOpen"]
old-location: multimedia\icopen.htm
tech.root: Multimedia
ms.assetid: 2637b6ef-2324-40db-99e4-773fcb6fdbf6
ms.date: 12/05/2018
ms.keywords: ICOpen, ICOpen function [Windows Multimedia], _win32_ICOpen, multimedia.icopen, vfw/ICOpen
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
 - ICOpen
 - vfw/ICOpen
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
 - ICOpen
---

# ICOpen function


## -description

The <b>ICOpen</b> function opens a compressor or decompressor.

## -parameters

### -param fccType

Four-character code indicating the type of compressor or decompressor to open. For video streams, the value of this parameter is "VIDC".

### -param fccHandler

Preferred handler of the specified type. Typically, the handler type is stored in the stream header in an AVI file.

### -param wMode

Flag defining the use of the compressor or decompressor. The following values are defined.

<table>
<tr>
<th>Value
                </th>
<th>Meaning
                </th>
</tr>
<tr>
<td>ICMODE_COMPRESS</td>
<td>Compressor will perform normal compression.</td>
</tr>
<tr>
<td>ICMODE_DECOMPRESS</td>
<td>Decompressor will perform normal decompression.</td>
</tr>
<tr>
<td>ICMODE_DRAW</td>
<td>Decompressor will decompress and draw the data directly to hardware.</td>
</tr>
<tr>
<td>ICMODE_FASTCOMPRESS</td>
<td>Compressor will perform fast (real-time) compression.</td>
</tr>
<tr>
<td>ICMODE_FASTDECOMPRESS</td>
<td>Decompressor will perform fast (real-time) decompression.</td>
</tr>
<tr>
<td>ICMODE_QUERY</td>
<td>Queries the compressor or decompressor for information.</td>
</tr>
</table>

## -returns

Returns a handle to a compressor or decompressor if successful or zero otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>