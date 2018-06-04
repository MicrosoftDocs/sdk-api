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

# _HTTP_DATA_CHUNK structure


## -description


The 
<b>HTTP_DATA_CHUNK</b> structure represents an individual block of data either in memory, in a file, or in the HTTP Server API response-fragment cache.


## -struct-fields




### -field DataChunkType

Type of data store. This member can be one of the values from the <b>HTTP_DATA_CHUNK_TYPE</b> enumeration.


### -field FromMemory


### -field FromMemory.pBuffer

Pointer to the starting memory address of the data block.


### -field FromMemory.BufferLength

Length, in bytes, of the data block.


### -field FromFileHandle


### -field FromFileHandle.ByteRange

An 
<a href="https://msdn.microsoft.com/a57d23cd-1e91-401a-b242-6549b1457594">HTTP_BYTE_RANGE</a> structure that specifies all or part of the file. To specify the entire file, set the <b>StartingOffset</b> member to zero and the <b>Length</b> member to <b>HTTP_BYTE_RANGE_TO_EOF</b>.


### -field FromFileHandle.FileHandle

Open handle to the file in question.


### -field FromFragmentCache


### -field FromFragmentCache.FragmentNameLength

Length, in bytes, of the fragment name not including the terminating null character.


### -field FromFragmentCache.pFragmentName

Pointer to a string that contains the fragment name assigned when the fragment was added to the response-fragment cache using 
the <a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a> function.


### -field FromFragmentCacheEx


### -field FromFragmentCacheEx.ByteRange

An <a href="https://msdn.microsoft.com/a57d23cd-1e91-401a-b242-6549b1457594">HTTP_BYTE_RANGE</a> structure specifying the byte range in the cached fragment.


### -field FromFragmentCacheEx.pFragmentName

Pointer to a string that contains the fragment name assigned when the fragment was added to the response-fragment cache using 
the <a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a> function. The length of the string cannot exceed 65532 bytes.

<div class="alert"><b>Note</b>  This string must be NULL terminated.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>



<a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a>



<a href="https://msdn.microsoft.com/f2ff2e40-ef1f-4c35-a615-f31ac63ab738">HttpSendResponseEntityBody</a>
 

 

