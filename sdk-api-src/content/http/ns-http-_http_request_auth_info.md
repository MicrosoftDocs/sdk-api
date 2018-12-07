---
UID: NS:http._HTTP_REQUEST_AUTH_INFO
title: "_HTTP_REQUEST_AUTH_INFO"
author: windows-sdk-content
description: Contains the authentication status of the request with a handle to the client token that the receiving process can use to impersonate the authenticated client.
old-location: http\http_request_auth_info.htm
tech.root: http
ms.assetid: 07008290-5277-4ef4-ae55-d335fdb2ba90
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PHTTP_REQUEST_AUTH_INFO, *PHTTP_REQUEST_AUTH_INFO structure [HTTP], HTTP_REQUEST_AUTH_FLAG_TOKEN_FOR_CACHED_CRED, HTTP_REQUEST_AUTH_INFO, HTTP_REQUEST_AUTH_INFO structure [HTTP], _HTTP_REQUEST_AUTH_INFO, http.http_request_auth_info, http/*PHTTP_REQUEST_AUTH_INFO, http/HTTP_REQUEST_AUTH_INFO"
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
 - HTTP_REQUEST_AUTH_INFO
product: Windows
targetos: Windows
req.typenames: HTTP_REQUEST_AUTH_INFO, *PHTTP_REQUEST_AUTH_INFO
req.redist: 
---

# _HTTP_REQUEST_AUTH_INFO structure


## -description


The <b>HTTP_REQUEST_AUTH_INFO</b> structure contains the authentication status of the request with a handle to the  client token that the receiving process can use to impersonate the authenticated client.

This structure is contained in the <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structure.


## -struct-fields




### -field AuthStatus

A member of the <a href="https://msdn.microsoft.com/1290fbbe-6c8e-40dc-b47c-32976d85afca">HTTP_AUTH_STATUS</a> enumeration that indicates the final authentication status of the request.

If the authentication status is not <b>HttpAuthStatusSuccess</b>, applications should disregard members of this structure except <b>AuthStatus</b>, <b>SecStatus</b>, and <b>AuthType</b>.


### -field SecStatus

A <a href="https://msdn.microsoft.com/library/Aa374703(v=VS.85).aspx">SECURITY_STATUS</a> value that indicates the security failure status when the <b>AuthStatus</b> member   is <b>HttpAuthStatusFailure</b>.


### -field Flags

The authentication flags that indicate the following authentication attributes:

<table>
<tr>
<th>Attribute</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_REQUEST_AUTH_FLAG_TOKEN_FOR_CACHED_CRED"></a><a id="http_request_auth_flag_token_for_cached_cred"></a><dl>
<dt><b>HTTP_REQUEST_AUTH_FLAG_TOKEN_FOR_CACHED_CRED</b></dt>
</dl>
</td>
<td width="60%">
The provided token is for  NTLM and is based on a cached credential of a Keep Alive (KA) connection.

</td>
</tr>
</table>
 


### -field AuthType

A member of the <a href="https://msdn.microsoft.com/e0147da5-7de2-4ea8-abc5-61c814ee7c55">HTTP_REQUEST_AUTH_TYPE</a> enumeration that indicates the authentication scheme attempted or established  for the request.


### -field AccessToken

A  handle to the client token that the receiving process can use to impersonate the authenticated client.

The handle to the token should be closed by calling <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> when it is no longer required. This token is valid only for the lifetime of the request. Applications can regenerate the initial 401 challenge to reauthenticate when the token expires.


### -field ContextAttributes

The client context attributes for the access token.


### -field PackedContextLength

The length, in bytes, of the <b>PackedContext</b>.


### -field PackedContextType

The type of context in the <b>PackedContext</b> member.


### -field PackedContext

The security context for the authentication type.

Applications can query the attributes of the packed context by calling the SSPI <a href="https://msdn.microsoft.com/library/Aa379326(v=VS.85).aspx">QueryContextAttributes</a> API. However, applications must acquire a  credential handle for the security package for the indicated AuthType.

Application should call the SSPI <a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> API to free the serialized context when it is no longer required.


### -field MutualAuthDataLength

The length, in bytes, of the <b>pMutualAuthData</b> member.


### -field pMutualAuthData

The Base64 encoded mutual authentication data used in  the WWW-Authenticate header.


### -field PackageNameLength

 


### -field pPackageName

 




## -remarks



Starting with HTTP version 2.0, the <a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure  contains an <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structure. The <b>pVoid</b> member of the <b>HTTP_REQUEST_INFO</b> structure points to the <b>HTTP_REQUEST_AUTH_INFO</b> when the request information type is <b>HttpRequestInfoTypeAuth</b>.

When the application receives a request with this structure and the request has not been authenticated, it can send the initial 401 challenge with the desired set of WWW-Authenticate headers in the <a href="https://msdn.microsoft.com/b5e68d55-43a4-422f-b7e3-163739628720">HTTP_MULTIPLE_KNOWN_HEADERS</a> structure. When the HTTP Server API completes  the authentication handshake, it fills  the <b>HTTP_REQUEST_AUTH_INFO</b> structure and passes it to the application with the request again. The handle to the access token that represents the client identity is provided in this structure by the HTTP Server API.

Context Attributes

 The <b>ContextAttributes</b> member is provided for SSPI based schemes. For example, SSPI applications can determine whether <b>ASC_RET_MUTUAL_AUTH</b> is set for a mutually authenticated session.

The HTTP Server API does not provide the expiration time for the context in the <b>PackedContext</b> member. Applications may require the expiration time  in specific  circumstances, for example, when NTLM credential caching is enabled and the application queries for the expiration time for a cached context. If the server application requires the expiration time for the underlying client context associated with the access token, it can receive the packed context and call <a href="https://msdn.microsoft.com/library/Aa379326(v=VS.85).aspx">QueryContextAttributes</a> with the  <b>SECPKG_ATTR_LIFESPAN</b>.

Mutual Authentication Data

By default, the HTTP Server API ensures that the mutual authentication data is added to the final 200 response; in general, server applications are not responsible for sending the mutual authentication data.

However, applications can receive the mutual authentication data and send it with the final response. When the <b>ReceiveMutualAuth</b> member of the <a href="https://msdn.microsoft.com/4f408115-c073-4e9f-b316-8ad3f03acf53">HTTP_SERVER_AUTHENTICATION_INFO</a> structure is set to true, applications receive the server credentials for mutual authentication along with the authenticated request.

The mutual authentication data provided in the <b>pMutualAuthData</b> member contains the exact value of WWW-Authenticate header without the header name. For example, <b>pMutualAuthData</b> points to "Negotiate ade02938481eca". The application builds the WWW-Authenticate header by appending the provided <b>pMutualAuthData</b> as a response header value.




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/02ac6f4f-ca54-42d5-9acb-5a1e81b2cb1c">HTTP_REQUEST_V2</a>
 

 

