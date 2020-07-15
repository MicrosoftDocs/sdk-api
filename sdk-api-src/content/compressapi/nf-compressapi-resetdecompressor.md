---
UID: NF:compressapi.ResetDecompressor
title: ResetDecompressor function (compressapi.h)
description: Prepares the decompressor for the decompression of a new stream.
helpviewer_keywords: ["ResetDecompressor","ResetDecompressor function [Compression API]","cmpapi.resetdecompressor","compressapi/ResetDecompressor"]
old-location: cmpapi\resetdecompressor.htm
tech.root: cmpapi
ms.assetid: 45243dac-bf07-4fee-aaf3-1482f4f009d9
ms.date: 12/05/2018
ms.keywords: ResetDecompressor, ResetDecompressor function [Compression API], cmpapi.resetdecompressor, compressapi/ResetDecompressor
f1_keywords:
- compressapi/ResetDecompressor
dev_langs:
- c++
req.header: compressapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- cabinet.dll
api_name:
- ResetDecompressor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResetDecompressor function


## -description


Prepares the decompressor for the decompression of a new stream. 


## -parameters




### -param DecompressorHandle [in]

Handle to the decompressor returned by <a href="https://docs.microsoft.com/windows/desktop/api/compressapi/nf-compressapi-createdecompressor">CreateDecompressor</a>.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>
 

 

