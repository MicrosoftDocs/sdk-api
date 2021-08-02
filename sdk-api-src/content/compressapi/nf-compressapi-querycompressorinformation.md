---
UID: NF:compressapi.QueryCompressorInformation
title: QueryCompressorInformation function (compressapi.h)
description: Queries a compressor for information for a particular compression algorithm.
helpviewer_keywords: ["QueryCompressorInformation","QueryCompressorInformation function [Compression API]","cmpapi.querycompressorinformation","compressapi/QueryCompressorInformation"]
old-location: cmpapi\querycompressorinformation.htm
tech.root: cmpapi
ms.assetid: 90b2ef29-c488-4d32-a315-312b25a0e585
ms.date: 12/05/2018
ms.keywords: QueryCompressorInformation, QueryCompressorInformation function [Compression API], cmpapi.querycompressorinformation, compressapi/QueryCompressorInformation
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
 - QueryCompressorInformation
 - compressapi/QueryCompressorInformation
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
 - QueryCompressorInformation
---

# QueryCompressorInformation function


## -description

Queries a compressor for information for a particular compression algorithm.

## -parameters

### -param CompressorHandle [in]

Handle to the compressor being queried for information.

### -param CompressInformationClass [in]

A value of the  <a href="/windows/desktop/api/compressapi/ne-compressapi-compress_information_class">COMPRESS_INFORMATION_CLASS</a> enumeration that identifies the type of information.

### -param CompressInformation [out]

Information for the compression algorithm written as bytes. The maximum size in bytes of this information is given by <i>CompressInformationSize</i>.

### -param CompressInformationSize [in]

Maximum size  in bytes of the information.

## -returns

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>. If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the compression algorithm does not allow the information class, the error can be <b>ERROR_UNSUPPORTED_TYPE</b>. If the buffer is too small to hold the value, the error can be <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>
