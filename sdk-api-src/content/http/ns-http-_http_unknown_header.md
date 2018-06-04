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
 

 

