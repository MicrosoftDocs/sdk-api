---
UID: NF:vfw.ICLocate
title: ICLocate function (vfw.h)
description: The ICLocate function finds a compressor or decompressor that can handle images with the specified formats, or finds a driver that can decompress an image with a specified format directly to hardware.
helpviewer_keywords: ["ICLocate","ICLocate function [Windows Multimedia]","ICMODE_COMPRESS","ICMODE_DECOMPRESS","ICMODE_DRAW","ICMODE_FASTCOMPRESS","ICMODE_FASTDECOMPRESS","_win32_ICLocate","multimedia.iclocate","vfw/ICLocate"]
old-location: multimedia\iclocate.htm
tech.root: Multimedia
ms.assetid: df7b14fe-9a6a-41d3-ba61-46b2e1df0b00
ms.date: 12/05/2018
ms.keywords: ICLocate, ICLocate function [Windows Multimedia], ICMODE_COMPRESS, ICMODE_DECOMPRESS, ICMODE_DRAW, ICMODE_FASTCOMPRESS, ICMODE_FASTDECOMPRESS, _win32_ICLocate, multimedia.iclocate, vfw/ICLocate
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
 - ICLocate
 - vfw/ICLocate
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
 - ICLocate
---

# ICLocate function


## -description

The <b>ICLocate</b> function finds a compressor or decompressor that can handle images with the specified formats, or finds a driver that can decompress an image with a specified format directly to hardware.

## -parameters

### -param fccType

Four-character code indicating the type of compressor or decompressor to open. For video streams, the value of this parameter is 'VIDC'.

### -param fccHandler

Preferred handler of the specified type. Typically, the handler type is stored in the stream header in an AVI file. Specify <b>NULL</b> if your application can use any handler type or it does not know the handler type to use.

### -param lpbiIn

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure defining the input format. A compressor handle is not returned unless it supports this format.

### -param lpbiOut

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure defining an optional decompressed format. You can also specify zero to use the default output format associated with the input format.

If this parameter is nonzero, a compressor handle is not returned unless it can create this output format.

### -param wFlags

Flags that describe the search criteria for a compressor or decompressor. The following values are defined:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICMODE_COMPRESS"></a><a id="icmode_compress"></a><dl>
<dt><b>ICMODE_COMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Finds a compressor that can compress an image with a format defined by <i>lpbiIn</i> to the format defined by <i>lpbiOut</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_DECOMPRESS"></a><a id="icmode_decompress"></a><dl>
<dt><b>ICMODE_DECOMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Finds a decompressor that can decompress an image with a format defined by <i>lpbiIn</i> to the format defined by <i>lpbiOut</i>.
          

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_DRAW"></a><a id="icmode_draw"></a><dl>
<dt><b>ICMODE_DRAW</b></dt>
</dl>
</td>
<td width="60%">
Finds a decompressor that can decompress an image with a format defined by <i>lpbiIn</i> and draw it directly to hardware.
          

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_FASTCOMPRESS"></a><a id="icmode_fastcompress"></a><dl>
<dt><b>ICMODE_FASTCOMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Has the same meaning as <b>ICMODE_COMPRESS</b> except the compressor is used for a real-time operation and emphasizes speed over quality.
          

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_FASTDECOMPRESS"></a><a id="icmode_fastdecompress"></a><dl>
<dt><b>ICMODE_FASTDECOMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Has the same meaning as <b>ICMODE_DECOMPRESS</b> except the decompressor is used for a real-time operation and emphasizes speed over quality.
          

</td>
</tr>
</table>

## -returns

Returns a handle to a compressor or decompressor if successful or zero otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>