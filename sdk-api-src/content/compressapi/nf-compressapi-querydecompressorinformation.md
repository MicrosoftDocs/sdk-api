---
UID: NF:compressapi.QueryDecompressorInformation
title: QueryDecompressorInformation function (compressapi.h)
description: Use this function to query information about a particular compression algorithm.
helpviewer_keywords: ["QueryDecompressorInformation","QueryDecompressorInformation function [Compression API]","cmpapi.querydecompressorinformation","compressapi/QueryDecompressorInformation"]
old-location: cmpapi\querydecompressorinformation.htm
tech.root: cmpapi
ms.assetid: 85b39c04-2145-45d2-be59-24615905353d
ms.date: 12/05/2018
ms.keywords: QueryDecompressorInformation, QueryDecompressorInformation function [Compression API], cmpapi.querydecompressorinformation, compressapi/QueryDecompressorInformation
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
 - QueryDecompressorInformation
 - compressapi/QueryDecompressorInformation
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
 - QueryDecompressorInformation
---

# QueryDecompressorInformation function


## -description

Use this function to query information about a particular compression algorithm.

## -parameters

### -param DecompressorHandle [in]

Handle to the decompressor being queried for information.

### -param CompressInformationClass [in]

A value of the  <a href="/windows/desktop/api/compressapi/ne-compressapi-compress_information_class">COMPRESS_INFORMATION_CLASS</a> enumeration that identifies the type of information.

### -param CompressInformation [out]

Information for the compression algorithm written as bytes. The maximum size in bytes of this information is given by <i>CompressInformationSize</i>.

### -param CompressInformationSize [in]

Maximum size  in bytes of the information.

## -returns

Returns <b>TRUE</b> to indicate success and <b>FALSE</b> otherwise. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to determine cause of failure.

## -remarks

If the compression algorithm fails for some internal reason, the error from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the compression algorithm does not allow the information class, the error can be <b>ERROR_UNSUPPORTED_TYPE</b>. If the buffer is too small to hold the value, the error can be <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -see-also

<a href="/windows/desktop/cmpapi/compression-api-functions">Compression API Functions</a>