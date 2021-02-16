---
UID: NE:http._HTTP_AUTH_STATUS
title: HTTP_AUTH_STATUS (http.h)
description: Defines the authentication state of a request.
helpviewer_keywords: ["*PHTTP_AUTH_STATUS","*PHTTP_AUTH_STATUS enumeration [HTTP]","HTTP_AUTH_STATUS","HTTP_AUTH_STATUS enumeration [HTTP]","HttpAuthStatusFailure","HttpAuthStatusNotAuthenticated","HttpAuthStatusSuccess","http.http_auth_status","http/*PHTTP_AUTH_STATUS","http/HTTP_AUTH_STATUS","http/HttpAuthStatusFailure","http/HttpAuthStatusNotAuthenticated","http/HttpAuthStatusSuccess"]
old-location: http\http_auth_status.htm
tech.root: http
ms.assetid: 1290fbbe-6c8e-40dc-b47c-32976d85afca
ms.date: 12/05/2018
ms.keywords: '*PHTTP_AUTH_STATUS, *PHTTP_AUTH_STATUS enumeration [HTTP], HTTP_AUTH_STATUS, HTTP_AUTH_STATUS enumeration [HTTP], HttpAuthStatusFailure, HttpAuthStatusNotAuthenticated, HttpAuthStatusSuccess, http.http_auth_status, http/*PHTTP_AUTH_STATUS, http/HTTP_AUTH_STATUS, http/HttpAuthStatusFailure, http/HttpAuthStatusNotAuthenticated, http/HttpAuthStatusSuccess'
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
targetos: Windows
req.typenames: HTTP_AUTH_STATUS, *PHTTP_AUTH_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_AUTH_STATUS
 - http/_HTTP_AUTH_STATUS
 - PHTTP_AUTH_STATUS
 - http/PHTTP_AUTH_STATUS
 - HTTP_AUTH_STATUS
 - http/HTTP_AUTH_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_AUTH_STATUS
---

# HTTP_AUTH_STATUS enumeration


## -description

The <b>HTTP_AUTH_STATUS</b> enumeration defines the authentication state of a request.

This enumeration is used  in the <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> structure.

## -enum-fields

### -field HttpAuthStatusSuccess

The request was successfully authenticated for the authentication type indicated in the <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> structure.

### -field HttpAuthStatusNotAuthenticated

Authentication was configured on the URL group for this request, however, the HTTP Server API did not handle the authentication. This could be because of one of the following reasons:

<ul>
<li>	The scheme defined in the <a href="/windows/desktop/api/http/ne-http-http_header_id">HttpHeaderAuthorization</a> header of the request is not supported by the HTTP Server API, or it is not enabled on the URL Group. If the scheme is not enabled, the <b>AuthType</b> member of <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> is set to the appropriate type, otherwise <b>AuthType</b> will have the value <a href="/windows/desktop/api/http/ne-http-http_request_auth_type">HttpRequestAuthTypeNone</a>. 
</li>
<li>The authorization header is not present, however, authentication is enabled on the URL Group.</li>
</ul>
The application should either proceed with its own authentication or respond with the initial 401 challenge containing the desired set of authentication schemes.

### -field HttpAuthStatusFailure

Authentication for the authentication type listed in the <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a>   structure failed, possibly due to one of the following reasons:<ul>
<li>The Security Service Provider Interface (SSPI) based authentication scheme failed to successfully return from a call to <a href="/previous-versions/windows/embedded/ms937012(v=msdn.10)">AcceptSecurityContext</a>. The error returned <a href="/previous-versions/windows/embedded/ms937012(v=msdn.10)">AcceptSecurityContext</a> is indicated in the <b>SecStatus</b> member of the <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> structure.</li>
<li>The finalized client context is for a Null NTLM session. Null sessions are treated as authentication failures.</li>
<li>The call to  <b>LogonUser</b> failed for the Basic authentication.</li>
</ul>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a>