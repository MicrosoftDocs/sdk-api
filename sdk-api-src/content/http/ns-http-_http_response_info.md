---
UID: NS:http._HTTP_RESPONSE_INFO
title: "_HTTP_RESPONSE_INFO"
author: windows-sdk-content
description: Extends the HTTP_RESPONSE structure with additional information for the response.
old-location: http\http_response_info.htm
tech.root: http
ms.assetid: 29422116-0a33-4553-98aa-785bb926dee0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_RESPONSE_INFO, *PHTTP_RESPONSE_INFO structure [HTTP], HTTP_RESPONSE_INFO, HTTP_RESPONSE_INFO structure [HTTP], _HTTP_RESPONSE_INFO, http.http_response_info, http/*PHTTP_RESPONSE_INFO, http/HTTP_RESPONSE_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - HTTP_RESPONSE_INFO
product: Windows
targetos: Windows
req.typenames: HTTP_RESPONSE_INFO, *PHTTP_RESPONSE_INFO
req.redist: 
---

# _HTTP_RESPONSE_INFO structure


## -description


The <b>HTTP_RESPONSE_INFO</b> structure extends the <a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a> structure  with additional information for the response.


## -struct-fields




### -field Type

A member of the <a href="https://msdn.microsoft.com/2f85e8dd-1693-4a54-a38f-9b70b2a46361">HTTP_RESPONSE_INFO_TYPE</a> enumeration specifying the type of information contained in this structure.


### -field Length

The length, in bytes, of the <b>pInfo</b> member.


### -field pInfo

A pointer to the <a href="https://msdn.microsoft.com/b5e68d55-43a4-422f-b7e3-163739628720">HTTP_MULTIPLE_KNOWN_HEADERS</a> structure when the <b>InfoType</b> member is <b>HttpResponseInfoTypeMultipleKnownHeaders</b>; otherwise <b>NULL</b>.


## -remarks



Starting with the HTTP Server API version 2.0, the HTTP_RESPONSE structure is extended to include an array of <b>HTTP_RESPONSE_INFO</b> structures in the <b>pRequestInfo</b> member. These structures contain additional information for the  response.




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>



<a href="https://msdn.microsoft.com/1900741e-f466-4826-b376-36170176c30a">HTTP_RESPONSE_V2</a>
 

 

