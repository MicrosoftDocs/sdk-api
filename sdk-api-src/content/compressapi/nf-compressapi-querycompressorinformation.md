---
UID: NF:compressapi.QueryCompressorInformation
title: QueryCompressorInformation function
author: windows-sdk-content
description: Queries a compressor for information for a particular compression algorithm.
old-location: cmpapi\querycompressorinformation.htm
old-project: cmpapi
ms.assetid: 90b2ef29-c488-4d32-a315-312b25a0e585
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: QueryCompressorInformation, QueryCompressorInformation function [Compression API], cmpapi.querycompressorinformation, compressapi/QueryCompressorInformation
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
 - QueryCompressorInformation
product: Windows
targetos: Windows
req.lib: Cabinet.lib
req.dll: Cabinet.dll
req.irql: 
---

# QueryCompressorInformation function


## -description


Queries a compressor for information for a particular compression algorithm.


## -parameters




### -param CompressorHandle [in]

Handle to the compressor being queried for information.


### -param CompressInformationClass [in]

A value of the  <a href="https://msdn.microsoft.com/ebdcbe03-b7fb-4dec-b906-086f8fe9be4c">COMPRESS_INFORMATION_CLASS</a> enumeration that identifies the type of information.


### -param CompressInformation [out]

Information for the compression algorithm written as bytes. The maximum size in bytes of this information is given by <i>CompressInformationSize</i>.


### -param CompressInformationSize [in]

Maximum size  in bytes of the information.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the compression algorithm does not allow the information class, the error can be <b>ERROR_UNSUPPORTED_TYPE</b>. If the buffer is to small to hold the value, the error can be <b>ERROR_INSUFFICIENT_BUFFER</b>.




## -see-also




<a href="https://msdn.microsoft.com/6A617444-23E5-4920-8D6B-602BCCDCC9E0">Compression API Functions</a>
 

 

