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

# _HTTP_MULTIPLE_KNOWN_HEADERS structure


## -description


The <b>HTTP_MULTIPLE_KNOWN_HEADERS</b> structure specifies the headers that are included in an HTTP response when more than one header is required.


## -struct-fields




### -field HeaderId

A member of the <a href="https://msdn.microsoft.com/6c4ccaf0-2a9f-43fe-9f35-cda1dd1fbbdc">HTTP_HEADER_ID</a> enumeration specifying the response header ID.


### -field Flags

The flags corresponding to the response header in the <b>HeaderId</b> member. This member is used only when the WWW-Authenticate header is present. This can be zero or the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_RESPONSE_INFO_FLAGS_PRESERVE_ORDER"></a><a id="http_response_info_flags_preserve_order"></a><dl>
<dt><b>HTTP_RESPONSE_INFO_FLAGS_PRESERVE_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The specified order of authentication schemes is preserved on the challenge response.

</td>
</tr>
</table>
 


### -field KnownHeaderCount

The number of elements in  the array specified in the  <b>KnownHeaders</b> member.


### -field KnownHeaders

A pointer to the first element in the array of <a href="https://msdn.microsoft.com/3f6c295c-f2c1-4070-a79e-9bb1e684ef92">HTTP_KNOWN_HEADER</a> structures.


## -remarks



The HTTP version 1.0 API allows applications to send only one known response header with the response. Starting with the HTTP version 2.0 API, applications are enabled to send multiple known response headers.

The <b>pInfo</b>  member of the <a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a> structure points to this structure when the application provides multiple known headers on a response. The <b>HTTP_RESPONSE_INFO</b> structure extends the <a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a> structure starting with HTTP version 2.0.

The <b>HTTP_MULTIPLE_KNOWN_HEADERS</b> structure enables server applications to send multiple authentication challenges to the client. 




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a>



<a href="https://msdn.microsoft.com/1900741e-f466-4826-b376-36170176c30a">HTTP_RESPONSE_V2</a>
 

 

