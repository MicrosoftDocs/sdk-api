---
UID: NF:vfw.AVIMakeCompressedStream
title: AVIMakeCompressedStream function (vfw.h)
description: The AVIMakeCompressedStream function creates a compressed stream from an uncompressed stream and a compression filter, and returns the address of a pointer to the compressed stream. This function supports audio and video compression.
helpviewer_keywords: ["AVIMakeCompressedStream","AVIMakeCompressedStream function [Windows Multimedia]","_win32_AVIMakeCompressedStream","multimedia.avimakecompressedstream","vfw/AVIMakeCompressedStream"]
old-location: multimedia\avimakecompressedstream.htm
tech.root: Multimedia
ms.assetid: 63279d7e-0e64-4708-a29c-60d5fdf75cb2
ms.date: 12/05/2018
ms.keywords: AVIMakeCompressedStream, AVIMakeCompressedStream function [Windows Multimedia], _win32_AVIMakeCompressedStream, multimedia.avimakecompressedstream, vfw/AVIMakeCompressedStream
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
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIMakeCompressedStream
 - vfw/AVIMakeCompressedStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - AVIMakeCompressedStream
---

# AVIMakeCompressedStream function


## -description

The <b>AVIMakeCompressedStream</b> function creates a compressed stream from an uncompressed stream and a compression filter, and returns the address of a pointer to the compressed stream. This function supports audio and video compression.

## -parameters

### -param ppsCompressed

Pointer to a buffer that receives the compressed stream pointer.

### -param ppsSource

Pointer to the stream to be compressed.

### -param lpOptions

Pointer to a structure that identifies the type of compression to use and the options to apply. You can specify video compression by identifying an appropriate handler in the <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structure. For audio compression, specify the compressed data format.

### -param pclsidHandler

Pointer to a class identifier used to create the stream.

## -returns

Returns AVIERR_OK if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_NOCOMPRESSOR</b></dt>
</dl>
</td>
<td width="60%">
A suitable compressor cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Compression is not supported for this type of data. This error might be returned if you try to compress data that is not audio or video.

</td>
</tr>
</table>

## -remarks

Applications can read from or write to the compressed stream.

A <b>PAVISTREAM</b> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>