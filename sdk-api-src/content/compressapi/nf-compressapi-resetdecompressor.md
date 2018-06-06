---
UID: NF:compressapi.ResetDecompressor
title: ResetDecompressor function
author: windows-sdk-content
description: Prepares the decompressor for the decompression of a new stream.
old-location: cmpapi\resetdecompressor.htm
old-project: cmpapi
ms.assetid: 45243dac-bf07-4fee-aaf3-1482f4f009d9
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: ResetDecompressor, ResetDecompressor function [Compression API], cmpapi.resetdecompressor, compressapi/ResetDecompressor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: COMPRESS_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - cabinet.dll
api_name:
 - ResetDecompressor
product: Windows
targetos: Windows
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
---

# ResetDecompressor function


## -description


Prepares the decompressor for the decompression of a new stream. 


## -parameters




### -param DecompressorHandle [in]

Handle to the decompressor returned by <a href="https://msdn.microsoft.com/a30b3ebe-24ef-4615-a555-a0383b46cd15">CreateDecompressor</a>.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6A617444-23E5-4920-8D6B-602BCCDCC9E0">Compression API Functions</a>
 

 

