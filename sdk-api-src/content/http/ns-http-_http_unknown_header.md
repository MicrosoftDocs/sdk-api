---
UID: NS:http._HTTP_UNKNOWN_HEADER
title: "_HTTP_UNKNOWN_HEADER"
author: windows-sdk-content
description: Contains the name and value for a header in an HTTP request or response whose name does not appear in the enumeration.
old-location: http\http_unknown_header.htm
tech.root: http
ms.assetid: 158f2979-58d3-4120-a74a-311b6fc53136
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_UNKNOWN_HEADER, HTTP_UNKNOWN_HEADER, HTTP_UNKNOWN_HEADER structure [HTTP], PHTTP_UNKNOWN_HEADER, PHTTP_UNKNOWN_HEADER structure pointer [HTTP], _HTTP_UNKNOWN_HEADER, _http_http_unknown_header, http.http_unknown_header, http/HTTP_UNKNOWN_HEADER, http/PHTTP_UNKNOWN_HEADER"
ms.prod: windows
ms.technology: windows-sdk
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
 - HTTP_UNKNOWN_HEADER
product: Windows
targetos: Windows
req.typenames: HTTP_UNKNOWN_HEADER, *PHTTP_UNKNOWN_HEADER
req.redist: 
---

# _HTTP_UNKNOWN_HEADER structure


## -description


The 
<b>HTTP_UNKNOWN_HEADER</b> structure contains the name and value for a header in an HTTP request or response whose name does not appear in the enumeration.


## -struct-fields




### -field NameLength

The size, in bytes, of the data pointed to by the <b>pName</b> member not counting a terminating null.


### -field RawValueLength

The size, in bytes, of the data pointed to by the <b>pRawValue</b> member, in bytes.


### -field pName

A pointer to a string of octets that specifies the header name. Use <b>NameLength</b> to determine the end of the string, rather than relying on a terminating <b>null</b>.


### -field pRawValue

A pointer to a string of octets that specifies the values for this header. Use <b>RawValueLength</b> to determine the end of the string, rather than relying on a terminating <b>null</b>.


## -see-also




<a href="https://msdn.microsoft.com/e38f7a05-f966-4853-be3b-5cdbf224719e">HTTP Server API Version 1.0 Structures</a>



<a href="https://msdn.microsoft.com/6c4ccaf0-2a9f-43fe-9f35-cda1dd1fbbdc">HTTP_HEADER_ID</a>



<a href="https://msdn.microsoft.com/a87b9c9c-cba1-4453-a300-7af35da944c9">HTTP_REQUEST_HEADERS</a>



<a href="https://msdn.microsoft.com/e783c27e-d215-4f6d-a080-92d915a7fc33">HTTP_RESPONSE_HEADERS</a>
 

 

