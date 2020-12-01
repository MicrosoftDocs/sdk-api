---
UID: NF:compressapi.Decompress
title: Decompress function (compressapi.h)
description: Takes a block of compressed information and decompresses it.
helpviewer_keywords: ["Decompress","Decompress function [Compression API]","cmpapi.decompress","compressapi/Decompress"]
old-location: cmpapi\decompress.htm
tech.root: cmpapi
ms.assetid: 654b88c7-14f2-43d4-8850-675ea303b439
ms.date: 12/05/2018
ms.keywords: Decompress, Decompress function [Compression API], cmpapi.decompress, compressapi/Decompress
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
 - Decompress
 - compressapi/Decompress
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
 - Decompress
---

# Decompress function


## -description

Takes a block of compressed information and decompresses it.

## -parameters

### -param DecompressorHandle [in]

Handle to a decompressor returned by <a href="/windows/desktop/api/compressapi/nf-compressapi-createdecompressor">CreateDecompressor</a>.

### -param CompressedData [in]

Contains the block of information that is to be decompressed. The size in bytes of the compressed block is given by <i>CompressedDataSize</i>.

### -param CompressedDataSize [in]

The size in bytes  of the compressed information.

### -param UncompressedBuffer [out]

The buffer that receives the uncompressed information. The size in bytes of the buffer is given by <i>UncompressedBufferSize</i>.

### -param UncompressedBufferSize [in]

Size  in bytes of the buffer that receives the uncompressed information.

### -param UncompressedDataSize [out]

Actual size  in bytes of the uncompressed information received.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the block of compressed data pointed to by <i>CompressedData</i> is corrupted, the function can fail and the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_BAD_COMPRESSION_BUFFER</b>. It is also possible that the function will produce  a block of uncompressed data that does not match the original data.  

It is recommended that compressors and decompressors not use the <b>COMPRESS_RAW</b> flag. If the compressor is created with the <b>COMPRESS_RAW</b> flag,  the decompressor must also be created with the <b>COMPRESS_RAW</b> flag. 

 If the compressor and decompressor are created using the <b>COMPRESS_RAW</b> flag, the value of <i>UncompressedBufferSize</i> must be exactly equal to the original size of the uncompressed data and not just the size of the output buffer. This means you should save the exact original size of the uncompressed data, as well as the   compressed data and compressed size, when using the <b>COMPRESS_RAW</b> flag. If  <i>UncompressedBufferSize</i> does not equal the original size of the uncompressed data, the uncompressed data will not match the original data. In this case, the function can return success or it can return <b>ERROR_BAD_COMPRESSION_BUFFER</b>. 

If the <b>COMPRESS_RAW</b> flag is not used, <i>UncompressedBufferSize</i> is not required to be exactly equal to the original size of the uncompressed data.  In this case, <i>UncompressedDataSize</i> returns the original size of the uncompressed data. If <i>UncompressedBufferSize</i> is smaller than the original data size, the function will fail and set <i>UncompressedDataSize</i> to the size of the original data and the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is <b>ERROR_INSUFFICIENT_BUFFER</b>.

To determine how large the <i>UncompressedBuffer</i> needs to be, call the function with <i>UncompressedBufferSize</i> set to zero.  In this case, the function will fail and set <i>UncompressedDataSize</i> to the size of the original data and the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is <b>ERROR_INSUFFICIENT_BUFFER</b>.  Note that the original size returned by the function is extracted from the buffer itself and should be treated as untrusted and tested against reasonable limits.

If the function is called with the <i>CompressedDataSize</i> parameter set to zero, the function fails and the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is <b>ERROR_INSUFFICIENT_BUFFER</b>. When it fails the function returns with <i>UncompressedDataSize</i> set to a value that you can use to avoid allocating too large a buffer for the compressed data. You must know the maximum possible size of the original data to use this method.

If you set <i>CompressedDataSize</i> to zero, and set <i>UncompressedBufferSize</i> to the maximum possible size of the original uncompressed data, the <b>Decompress</b> function will fail as described and the value of <i>UncompressedDataSize</i> will be set to the maximum size for the compressed data buffer.

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.     If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the output buffer is too small to hold the uncompressed data, the error can be <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>