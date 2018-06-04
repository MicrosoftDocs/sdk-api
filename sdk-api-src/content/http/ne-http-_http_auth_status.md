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

# _HTTP_AUTH_STATUS enumeration


## -description


The <b>HTTP_AUTH_STATUS</b> enumeration defines the authentication state of a request.

This enumeration is used  in the <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> structure.


## -enum-fields




### -field HttpAuthStatusSuccess

The request was successfully authenticated for the authentication type indicated in the <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> structure.


### -field HttpAuthStatusNotAuthenticated

Authentication was configured on the URL group for this request, however, the HTTP Server API did not handle the authentication. This could be because of one of the following reasons:

<ul>
<li>	The scheme defined in the <a href="https://msdn.microsoft.com/6c4ccaf0-2a9f-43fe-9f35-cda1dd1fbbdc">HttpHeaderAuthorization</a> header of the request is not supported by the HTTP Server API, or it is not enabled on the URL Group. If the scheme is not enabled, the <b>AuthType</b> member of <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> is set to the appropriate type, otherwise <b>AuthType</b> will have the value <a href="https://msdn.microsoft.com/e0147da5-7de2-4ea8-abc5-61c814ee7c55">HttpRequestAuthTypeNone</a>. 
</li>
<li>The authorization header is not present, however, authentication is enabled on the URL Group.</li>
</ul>
The application should either proceed with its own authentication or respond with the initial 401 challenge containing the desired set of authentication schemes.


### -field HttpAuthStatusFailure

Authentication for the authentication type listed in the <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a>   structure failed, possibly due to one of the following reasons:<ul>
<li>The Security Service Provider Interface (SSPI) based authentication scheme failed to successfully return from a call to <a href="Http://go.microsoft.com/fwlink/p/?linkid=83940">AcceptSecurityContext</a>. The error returned <a href="Http://go.microsoft.com/fwlink/p/?linkid=83940">AcceptSecurityContext</a> is indicated in the <b>SecStatus</b> member of the <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> structure.</li>
<li>The finalized client context is for a Null NTLM session. Null sessions are treated as authentication failures.</li>
<li>The call to  <b>LogonUser</b> failed for the Basic authentication.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a>
 

 

