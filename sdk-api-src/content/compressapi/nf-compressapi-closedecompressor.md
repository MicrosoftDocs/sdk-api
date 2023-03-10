---
UID: NF:compressapi.CloseDecompressor
title: CloseDecompressor function (compressapi.h)
description: Call to close an open DECOMPRESSOR_HANDLE.
helpviewer_keywords: ["CloseDecompressor","CloseDecompressor function [Compression API]","cmpapi.closedecompressor","compressapi/CloseDecompressor"]
old-location: cmpapi\closedecompressor.htm
tech.root: cmpapi
ms.assetid: bcc4b342-9b84-43c6-aac0-c8f8ea5089c8
ms.date: 12/05/2018
ms.keywords: CloseDecompressor, CloseDecompressor function [Compression API], cmpapi.closedecompressor, compressapi/CloseDecompressor
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
 - CloseDecompressor
 - compressapi/CloseDecompressor
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
 - CloseDecompressor
---

# CloseDecompressor function


## -description

Call to close an open <b>DECOMPRESSOR_HANDLE</b>.

## -parameters

### -param DecompressorHandle [in]

Handle to the decompressor to be closed. This is the handle to the compressor that was returned by <a href="/windows/desktop/api/compressapi/nf-compressapi-createdecompressor">CreateDecompressor</a>.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>