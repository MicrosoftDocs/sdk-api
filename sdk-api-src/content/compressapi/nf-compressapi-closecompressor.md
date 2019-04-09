---
UID: NF:compressapi.CloseCompressor
title: CloseCompressor function (compressapi.h)
author: windows-sdk-content
description: Call to close an open COMPRESSOR_HANDLE.
old-location: cmpapi\closecompressor.htm
tech.root: cmpapi
ms.assetid: 098cf0b9-cd42-4a40-b30f-d7364d067e41
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseCompressor, CloseCompressor function [Compression API], cmpapi.closecompressor, compressapi/CloseCompressor
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
 - CloseCompressor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseCompressor function


## -description


Call to close an open <b>COMPRESSOR_HANDLE</b>.


## -parameters




### -param CompressorHandle [in]

Handle to the compressor to be closed. This is the handle to the compressor that was returned by <a href="https://msdn.microsoft.com/782b3c08-158a-4bbd-89a5-c20666cbfb94">CreateCompressor</a>.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6A617444-23E5-4920-8D6B-602BCCDCC9E0">Compression API Functions</a>
 

 

