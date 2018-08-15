---
UID: NE:http._HTTP_AUTH_STATUS
title: "_HTTP_AUTH_STATUS"
author: windows-sdk-content
description: Defines the authentication state of a request.
old-location: http\http_auth_status.htm
old-project: http
ms.assetid: 1290fbbe-6c8e-40dc-b47c-32976d85afca
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_AUTH_STATUS, *PHTTP_AUTH_STATUS enumeration [HTTP], HTTP_AUTH_STATUS, HTTP_AUTH_STATUS enumeration [HTTP], HttpAuthStatusFailure, HttpAuthStatusNotAuthenticated, HttpAuthStatusSuccess, _HTTP_AUTH_STATUS, http.http_auth_status, http/*PHTTP_AUTH_STATUS, http/HTTP_AUTH_STATUS, http/HttpAuthStatusFailure, http/HttpAuthStatusNotAuthenticated, http/HttpAuthStatusSuccess"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: http.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: HTTP_AUTH_STATUS, *PHTTP_AUTH_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_AUTH_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

