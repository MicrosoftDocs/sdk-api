---
UID: NS:http._HTTP_RESPONSE_HEADERS
title: "_HTTP_RESPONSE_HEADERS"
author: windows-sdk-content
description: Contains the headers sent with an HTTP response.
old-location: http\http_response_headers.htm
tech.root: Http
ms.assetid: e783c27e-d215-4f6d-a080-92d915a7fc33
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_RESPONSE_HEADERS, HTTP_RESPONSE_HEADERS, HTTP_RESPONSE_HEADERS structure [HTTP], PHTTP_RESPONSE_HEADERS, PHTTP_RESPONSE_HEADERS structure pointer [HTTP], _HTTP_RESPONSE_HEADERS, _http_http_response_headers, http.http_response_headers, http/HTTP_RESPONSE_HEADERS, http/PHTTP_RESPONSE_HEADERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_RESPONSE_HEADERS
product: Windows
targetos: Windows
req.typenames: HTTP_RESPONSE_HEADERS, *PHTTP_RESPONSE_HEADERS
req.redist: 
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
 

 

