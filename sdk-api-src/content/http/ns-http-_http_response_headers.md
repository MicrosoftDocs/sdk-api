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

# _HTTP_RESPONSE_HEADERS structure


## -description


The 
<b>HTTP_RESPONSE_HEADERS</b> structure contains the headers sent with an HTTP response.


## -struct-fields




### -field UnknownHeaderCount

A number of unknown headers sent with the HTTP response and contained in the array pointed to by the <b>pUnknownHeaders</b> member. This number cannot exceed 9999.


### -field pUnknownHeaders

A pointer to an array of 
<a href="https://msdn.microsoft.com/158f2979-58d3-4120-a74a-311b6fc53136">HTTP_UNKNOWN_HEADER</a> structures that contains one structure for each of the unknown headers sent in the HTTP response.


### -field TrailerCount

This member is reserved and must be zero.


### -field pTrailers

This member is reserved and must be <b>NULL</b>.


### -field KnownHeaders

Fixed-size array of 
<a href="https://msdn.microsoft.com/3f6c295c-f2c1-4070-a79e-9bb1e684ef92">HTTP_KNOWN_HEADER</a> structures. The 
<a href="https://msdn.microsoft.com/6c4ccaf0-2a9f-43fe-9f35-cda1dd1fbbdc">HTTP_HEADER_ID</a> enumeration provides a mapping from header types to array indexes. If a known header of a given type is included in the HTTP response, the array element at the index that corresponds to that type specifies the header value. Those elements of the array for which no corresponding headers are present contain a zero-valued <b>RawValueLength</b> member. Use <b>RawValueLength</b> to determine the end of the header string pointed to by <b>pRawValue</b>, rather than relying on the string to have a terminating null.


## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/3f6c295c-f2c1-4070-a79e-9bb1e684ef92">HTTP_KNOWN_HEADER</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>



<a href="https://msdn.microsoft.com/158f2979-58d3-4120-a74a-311b6fc53136">HTTP_UNKNOWN_HEADER</a>
 

 

