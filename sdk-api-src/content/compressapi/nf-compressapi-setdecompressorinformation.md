---
UID: NF:compressapi.SetDecompressorInformation
title: SetDecompressorInformation function (compressapi.h)
author: windows-sdk-content
description: Sets information in a decompressor for a particular compression algorithm.
old-location: cmpapi\setdecompressorinformation.htm
tech.root: cmpapi
ms.assetid: 804B73D3-E68E-43A3-8F23-6A46ABDECB23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetDecompressorInformation, SetDecompressorInformation function [Compression API], cmpapi.setdecompressorinformation, compressapi/SetDecompressorInformation
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
 - SetDecompressorInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDecompressorInformation function


## -description


Sets information in a decompressor for a particular compression algorithm.


## -parameters




### -param DecompressorHandle [in]

Handle to the decompressor.


### -param CompressInformationClass [in]

A value that identifies the type of information. of the  enumeration that identifies the type of information.


### -param CompressInformation [in]

The information being set read as bytes. The maximum size in bytes is given by <i>CompressInformationSize</i>.


### -param CompressInformationSize [in]

Maximum size  of the information in bytes.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>. If the system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the compression algorithm does not allow changing the value of this information class, the error can be <b>ERROR_NOT_SUPPORTED</b>. If the compression algorithm does not allow the information class, the error can be <b>ERROR_UNSUPPORTED_TYPE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6A617444-23E5-4920-8D6B-602BCCDCC9E0">Compression API Functions</a>
 

 

