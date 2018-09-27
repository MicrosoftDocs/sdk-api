---
UID: NF:compressapi.ResetCompressor
title: ResetCompressor function
author: windows-sdk-content
description: Prepares the compressor for the compression of a new stream.
old-location: cmpapi\resetcompressor.htm
tech.root: cmpapi
ms.assetid: 1ea542e0-7236-4158-9578-f5d55f8c7f8e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ResetCompressor, ResetCompressor function [Compression API], cmpapi.resetcompressor, compressapi/ResetCompressor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ResetCompressor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResetCompressor function


## -description


Prepares the compressor for the compression of a new stream. The compressor object retains properties set with <a href="https://msdn.microsoft.com/f8c2c425-9b21-4fe3-8b81-d8bf3cd8ec5b">SetCompressorInformation</a>. The sequence of blocks generated is independent of previous blocks.


## -parameters




### -param CompressorHandle [in]

Handle to the compressor returned by <a href="https://msdn.microsoft.com/782b3c08-158a-4bbd-89a5-c20666cbfb94">CreateCompressor</a>.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6A617444-23E5-4920-8D6B-602BCCDCC9E0">Compression API Functions</a>
 

 

