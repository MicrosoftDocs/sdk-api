---
UID: NF:compressapi.CloseCompressor
title: CloseCompressor function (compressapi.h)
description: Call to close an open COMPRESSOR_HANDLE.
helpviewer_keywords: ["CloseCompressor","CloseCompressor function [Compression API]","cmpapi.closecompressor","compressapi/CloseCompressor"]
old-location: cmpapi\closecompressor.htm
tech.root: cmpapi
ms.assetid: 098cf0b9-cd42-4a40-b30f-d7364d067e41
ms.date: 12/05/2018
ms.keywords: CloseCompressor, CloseCompressor function [Compression API], cmpapi.closecompressor, compressapi/CloseCompressor
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
 - CloseCompressor
 - compressapi/CloseCompressor
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
 - CloseCompressor
---

# CloseCompressor function


## -description

Call to close an open <b>COMPRESSOR_HANDLE</b>.

## -parameters

### -param CompressorHandle [in]

Handle to the compressor to be closed. This is the handle to the compressor that was returned by <a href="/windows/desktop/api/compressapi/nf-compressapi-createcompressor">CreateCompressor</a>.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>