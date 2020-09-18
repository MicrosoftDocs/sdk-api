---
UID: NF:compressapi.Compress
title: Compress function (compressapi.h)
description: Takes a block of information and compresses it.
helpviewer_keywords: ["Compress","Compress function [Compression API]","cmpapi.compress","compressapi/Compress"]
old-location: cmpapi\compress.htm
tech.root: cmpapi
ms.assetid: 0e32501c-5213-43e6-88ca-1e424181d7a2
ms.date: 12/05/2018
ms.keywords: Compress, Compress function [Compression API], cmpapi.compress, compressapi/Compress
req.header: compressapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Compress
 - compressapi/Compress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - cabinet.dll
api_name:
 - Compress
---

# Compress function


## -description

Takes a block of information and compresses it.

## -parameters

### -param CompressorHandle [in]

Handle to a compressor returned by <a href="/windows/desktop/api/compressapi/nf-compressapi-createcompressor">CreateCompressor</a>.

### -param UncompressedData [in]

Contains the block of information that is to be compressed. The size in bytes of the uncompressed block is given by <i>UncompressedDataSize</i>.

### -param UncompressedDataSize [in]

Size in bytes  of the uncompressed information.

### -param CompressedBuffer [out]

The buffer that receives the compressed information. The maximum size in bytes of the buffer is given by <i>CompressedBufferSize</i>.

### -param CompressedBufferSize [in]

Maximum size  in bytes of the buffer that receives the compressed information.

### -param CompressedDataSize [out]

Actual size  in bytes of the compressed information received.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the output buffer is too small to hold the compressed data, the error can be <b>ERROR_INSUFFICIENT_BUFFER</b>.

If <i>CompressedBuffer</i> output buffer is too small to hold the compressed data, the function fails and the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_INSUFFICIENT_BUFFER</b>. In this case, the <i>CompressedDataSize</i> parameter receives with the size that the  <i>CompressedBuffer</i> needs to be to guarantee success for that input buffer. You can set <i>CompressedBufferSize</i> to zero to determine the size of the output buffer to allocate.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>