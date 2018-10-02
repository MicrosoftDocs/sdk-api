---
UID: NS:http._HTTP_RESPONSE_V2
title: "_HTTP_RESPONSE_V2"
author: windows-sdk-content
description: Extends the HTTP version 1.0 response structure with more information for the response.
old-location: http\http_response_v2.htm
tech.root: Http
ms.assetid: 1900741e-f466-4826-b376-36170176c30a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_RESPONSE, *PHTTP_RESPONSE_V2, *PHTTP_RESPONSE_V2 structure [HTTP], HTTP_RESPONSE, HTTP_RESPONSE_V2, HTTP_RESPONSE_V2 structure [HTTP], _HTTP_RESPONSE_V2, http.http_response_v2, http/*PHTTP_RESPONSE_V2, http/HTTP_RESPONSE_V2"
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
 - HTTP_RESPONSE_V2
product: Windows
targetos: Windows
req.typenames: HTTP_RESPONSE_V2, *PHTTP_RESPONSE_V2
req.redist: 
---

# _HTTP_RESPONSE_V2 structure


## -description


The <b>HTTP_RESPONSE_V2</b> structure extends the HTTP version 1.0 response structure with more information for the response.

Do not use <b>HTTP_RESPONSE_V2</b> directly in your code;  use <a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a> instead to ensure that the proper version, based on the operating system the code is compiled under, is used.


## -struct-fields




### -field ResponseInfoCount

The number of <a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a> structures in the array pointed to by <b>pResponseInfo</b>.

The count of the HTTP_RESPONSE_INFO elements in the array pointed to by <b>pResponseInfo</b>.


### -field pResponseInfo

A pointer to an array of <a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a> structures containing more information about the request.


### -field _HTTP_RESPONSE_V1

 




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/ae67c066-c8bd-483f-829f-30192f49593d">HTTP_DATA_CHUNK</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>



<a href="https://msdn.microsoft.com/e783c27e-d215-4f6d-a080-92d915a7fc33">HTTP_RESPONSE_HEADERS</a>



<a href="https://msdn.microsoft.com/9e1bbcca-1b7c-4146-95c7-72660bf31507">HTTP_RESPONSE_V1</a>



<a href="https://msdn.microsoft.com/0183584f-105e-4fa3-8991-d3f2dfca1d62">HttpSendHttpResponse</a>
 

 

