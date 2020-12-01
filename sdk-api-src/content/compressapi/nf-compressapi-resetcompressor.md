---
UID: NF:compressapi.ResetCompressor
title: ResetCompressor function (compressapi.h)
description: Prepares the compressor for the compression of a new stream.
helpviewer_keywords: ["ResetCompressor","ResetCompressor function [Compression API]","cmpapi.resetcompressor","compressapi/ResetCompressor"]
old-location: cmpapi\resetcompressor.htm
tech.root: cmpapi
ms.assetid: 1ea542e0-7236-4158-9578-f5d55f8c7f8e
ms.date: 12/05/2018
ms.keywords: ResetCompressor, ResetCompressor function [Compression API], cmpapi.resetcompressor, compressapi/ResetCompressor
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
 - ResetCompressor
 - compressapi/ResetCompressor
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
 - ResetCompressor
---

# ResetCompressor function


## -description

Prepares the compressor for the compression of a new stream. The compressor object retains properties set with <a href="/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation">SetCompressorInformation</a>. The sequence of blocks generated is independent of previous blocks.

## -parameters

### -param CompressorHandle [in]

Handle to the compressor returned by <a href="/windows/desktop/api/compressapi/nf-compressapi-createcompressor">CreateCompressor</a>.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>