---
UID: NS:http._HTTP_RESPONSE_V1
title: "_HTTP_RESPONSE_V1"
author: windows-sdk-content
description: Contains data associated with an HTTP response.
old-location: http\http_response_v1.htm
tech.root: Http
ms.assetid: 9e1bbcca-1b7c-4146-95c7-72660bf31507
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_RESPONSE, *PHTTP_RESPONSE_V1, HTTP_RESPONSE, HTTP_RESPONSE_V1, HTTP_RESPONSE_V1 structure [HTTP], PHTTP_RESPONSE_V1, PHTTP_RESPONSE_V1 structure pointer [HTTP], _HTTP_RESPONSE_V1, http.http_response_v1, http/HTTP_RESPONSE_V1, http/PHTTP_RESPONSE_V1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HTTP_RESPONSE_V1
product: Windows
targetos: Windows
req.typenames: HTTP_RESPONSE_V1, *PHTTP_RESPONSE_V1
req.redist: 
---

# _HTTP_RESPONSE_V1 structure


## -description


The 
<b>HTTP_RESPONSE_V1</b> structure contains data associated with an HTTP response.

Do not use <b>HTTP_RESPONSE_V1</b> directly in your code;  use <a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a> instead to ensure that the proper version, based on the operating system the code is compiled under, is used.


## -struct-fields




### -field Flags

The optional logging flags change the default response behavior.     These  can be one of any of the  <a href="https://msdn.microsoft.com/bcb59457-fd22-4166-8a72-ba85209ec8c7">HTTP_RESPONSE_FLAG</a> values.


### -field Version

This member is ignored; the response is always an HTTP/1.1 response.


### -field StatusCode

Numeric status code that characterizes the result of the HTTP request (for example, 200 signifying "OK" or 404 signifying "Not Found"). For more information and a list of these codes, see Section 10 of 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84048">RFC 2616</a>.

If a request is directed to a URL that is reserved but not registered, indicating that the appropriate application to handle it is not running, then the HTTP Server API itself returns a response with status code 400, signifying "Bad Request". This is transparent to the application. A code 400 is preferred here to 503 ("Server not available") because the latter is interpreted by some smart load balancers as an indication that the server is overloaded.


### -field ReasonLength

Size, in bytes, of the string pointed to by the <b>pReason</b> member not including the terminating null. May be zero.


### -field pReason

A pointer to a human-readable, null-terminated string of printable characters that characterizes the result of the HTTP request (for example, "OK" or "Not Found").


### -field Headers

An 
<a href="https://msdn.microsoft.com/e783c27e-d215-4f6d-a080-92d915a7fc33">HTTP_RESPONSE_HEADERS</a> structure that contains the headers used in this response.


### -field EntityChunkCount

A number of entity-body data blocks specified in the <b>pEntityChunks</b> array. This number cannot exceed 100. If the response has no entity body, this member must be zero.


### -field pEntityChunks

An array of 
<a href="https://msdn.microsoft.com/ae67c066-c8bd-483f-829f-30192f49593d">HTTP_DATA_CHUNK</a> structures that together specify all the data blocks that make up the entity body of the response.


## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/ae67c066-c8bd-483f-829f-30192f49593d">HTTP_DATA_CHUNK</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>



<a href="https://msdn.microsoft.com/e783c27e-d215-4f6d-a080-92d915a7fc33">HTTP_RESPONSE_HEADERS</a>



<a href="https://msdn.microsoft.com/1900741e-f466-4826-b376-36170176c30a">HTTP_RESPONSE_V2</a>



<a href="https://msdn.microsoft.com/0183584f-105e-4fa3-8991-d3f2dfca1d62">HttpSendHttpResponse</a>
 

 

