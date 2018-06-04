---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Compress function


## -description


Takes a block of information and compresses it. 


## -parameters




### -param CompressorHandle [in]

Handle to a compressor returned by <a href="https://msdn.microsoft.com/782b3c08-158a-4bbd-89a5-c20666cbfb94">CreateCompressor</a>.


### -param UncompressedData [in]

Contains the block of information that is to be compressed. The size in bytes of the uncompressed block is given by <i>UncompressedDataSize</i>.


### -param UncompressedDataSize [in]

Size in bytes  of the uncompressed information.


### -param CompressedBuffer [out]

The buffer that receives the compressed information. The maximum size in bytes of the buffer is given by <i>CompressedBufferSize</i>.


### -param CompressedBufferSize [in]

Maximum size  in bytes of the buffer that receives the compressed information.


### -param CompressedDataSize [out]

Actual size  in bytes of the compressed information received.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the compression algorithm fails for some internal reason, the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_FUNCTION_FAILED</b>.    If the  system cannot locate the compression algorithm handle, the error can be <b>ERROR_INVALID_HANDLE</b>. If the output buffer is too small to hold the compressed data, the error can be <b>ERROR_INSUFFICIENT_BUFFER</b>.

If <i>CompressedBuffer</i> output buffer is too small to hold the compressed data, the function fails and the error from <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be <b>ERROR_INSUFFICIENT_BUFFER</b>. In this case, the <i>CompressedDataSize</i> parameter receives with the size that the  <i>CompressedBuffer</i> needs to be to guarantee success for that input buffer. You can set <i>CompressedBufferSize</i> to zero to determine the size of the output buffer to allocate.




## -see-also




<a href="https://msdn.microsoft.com/6A617444-23E5-4920-8D6B-602BCCDCC9E0">Compression API Functions</a>
 

 

