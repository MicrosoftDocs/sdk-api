---
UID: NF:vfw.ICOpenFunction
title: ICOpenFunction function (vfw.h)
description: The ICOpenFunction function opens a compressor or decompressor defined as a function.
helpviewer_keywords: ["ICOpenFunction","ICOpenFunction function [Windows Multimedia]","_win32_ICOpenFunction","multimedia.icopenfunction","vfw/ICOpenFunction"]
old-location: multimedia\icopenfunction.htm
tech.root: Multimedia
ms.assetid: 1dc04649-9fe4-4131-8a7c-598b3fba883c
ms.date: 12/05/2018
ms.keywords: ICOpenFunction, ICOpenFunction function [Windows Multimedia], _win32_ICOpenFunction, multimedia.icopenfunction, vfw/ICOpenFunction
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
 - ICOpenFunction
 - vfw/ICOpenFunction
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
 - ICOpenFunction
---

# ICOpenFunction function


## -description

The <b>ICOpenFunction</b> function opens a compressor or decompressor defined as a function.

## -parameters

### -param fccType

Type of compressor to open. For video, the value of this parameter is ICTYPE_VIDEO.

### -param fccHandler

Preferred handler of the specified type. Typically, this comes from the stream header in an AVI file.

### -param wMode

Flag to define the use of the compressor or decompressor. The following values are defined.

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

### -param lpfnHandler

Pointer to the function used as the compressor or decompressor.

## -returns

Returns a handle to a compressor or decompressor if successful or zero otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>