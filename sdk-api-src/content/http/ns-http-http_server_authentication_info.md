---
UID: NS:http._HTTP_SERVER_AUTHENTICATION_INFO
title: HTTP_SERVER_AUTHENTICATION_INFO (http.h)
description: Used to enable server-side authentication on a URL group or server session.
helpviewer_keywords: ["*PHTTP_SERVER_AUTHENTICATION_INFO","*PHTTP_SERVER_AUTHENTICATION_INFO structure [HTTP]","HTTP_AUTH_ENABLE_ALL","HTTP_AUTH_ENABLE_BASIC","HTTP_AUTH_ENABLE_DIGEST","HTTP_AUTH_ENABLE_KERBEROS","HTTP_AUTH_ENABLE_NEGOTIATE","HTTP_AUTH_ENABLE_NTLM","HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL","HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING","HTTP_SERVER_AUTHENTICATION_INFO","HTTP_SERVER_AUTHENTICATION_INFO structure [HTTP]","http.http_server_authentication_info","http/*PHTTP_SERVER_AUTHENTICATION_INFO","http/HTTP_SERVER_AUTHENTICATION_INFO"]
old-location: http\http_server_authentication_info.htm
tech.root: http
ms.assetid: 4f408115-c073-4e9f-b316-8ad3f03acf53
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVER_AUTHENTICATION_INFO, *PHTTP_SERVER_AUTHENTICATION_INFO structure [HTTP], HTTP_AUTH_ENABLE_ALL, HTTP_AUTH_ENABLE_BASIC, HTTP_AUTH_ENABLE_DIGEST, HTTP_AUTH_ENABLE_KERBEROS, HTTP_AUTH_ENABLE_NEGOTIATE, HTTP_AUTH_ENABLE_NTLM, HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL, HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING, HTTP_SERVER_AUTHENTICATION_INFO, HTTP_SERVER_AUTHENTICATION_INFO structure [HTTP], http.http_server_authentication_info, http/*PHTTP_SERVER_AUTHENTICATION_INFO, http/HTTP_SERVER_AUTHENTICATION_INFO'
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
req.typenames: HTTP_SERVER_AUTHENTICATION_INFO, *PHTTP_SERVER_AUTHENTICATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVER_AUTHENTICATION_INFO
 - http/_HTTP_SERVER_AUTHENTICATION_INFO
 - PHTTP_SERVER_AUTHENTICATION_INFO
 - http/PHTTP_SERVER_AUTHENTICATION_INFO
 - HTTP_SERVER_AUTHENTICATION_INFO
 - http/HTTP_SERVER_AUTHENTICATION_INFO
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
 - HTTP_SERVER_AUTHENTICATION_INFO
---

# HTTP_SERVER_AUTHENTICATION_INFO structure


## -description

The <b>HTTP_SERVER_AUTHENTICATION_INFO</b> structure is used to enable server-side authentication on a URL group or server session. This structure is also used to query the existing authentication schemes enabled for a URL group or server session.

This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServerAuthenticationProperty</a> on a URL group, or server session.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure that specifies if the property is present.

### -field AuthSchemes

The supported authentication schemes. This can be one or more of the following:

<table>
<tr>
<th>Authentication Scheme</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_AUTH_ENABLE_BASIC"></a><a id="http_auth_enable_basic"></a><dl>
<dt><b>HTTP_AUTH_ENABLE_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Basic authentication is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_AUTH_ENABLE_DIGEST"></a><a id="http_auth_enable_digest"></a><dl>
<dt><b>HTTP_AUTH_ENABLE_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
Digest authentication is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_AUTH_ENABLE_NTLM"></a><a id="http_auth_enable_ntlm"></a><dl>
<dt><b>HTTP_AUTH_ENABLE_NTLM</b></dt>
</dl>
</td>
<td width="60%">
NTLM authentication is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="_HTTP_AUTH_ENABLE_NEGOTIATE"></a><a id="_http_auth_enable_negotiate"></a><dl>
<dt><b> HTTP_AUTH_ENABLE_NEGOTIATE</b></dt>
</dl>
</td>
<td width="60%">
Negotiate authentication is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_AUTH_ENABLE_KERBEROS"></a><a id="http_auth_enable_kerberos"></a><dl>
<dt><b>HTTP_AUTH_ENABLE_KERBEROS</b></dt>
</dl>
</td>
<td width="60%">
Kerberos authentication is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="_HTTP_AUTH_ENABLE_ALL"></a><a id="_http_auth_enable_all"></a><dl>
<dt><b> HTTP_AUTH_ENABLE_ALL</b></dt>
</dl>
</td>
<td width="60%">
All types of authentication are enabled.

</td>
</tr>
</table>

### -field ReceiveMutualAuth

A Boolean value that indicates, if <b>True</b>, that the client application receives the server credentials for mutual authentication with the authenticated request. If <b>False</b>, the client application does not receive the credentials.

Be aware that this option is set for all  requests served by the associated request queue.

### -field ReceiveContextHandle

A Boolean value that indicates, if <b>True</b>, that the finalized client context is serialized and passed to the application with the request. If <b>False</b>, the application does not receive the context. This handle can be used to query context attributes.

### -field DisableNTLMCredentialCaching

A Boolean value that indicates, if <b>True</b>, that the NTLM credentials are not cached. If <b>False</b>, the default behavior is preserved.

By default,  HTTP caches the client context for Keep Alive (KA) connections for the NTLM scheme if the request did not originate from a proxy.

### -field ExFlags

Optional authentication flags. Can be one or more of the following possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></a><a id="http_auth_ex_flag_enable_kerberos_credential_caching"></a><dl>
<dt><b>HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING</b></dt>
</dl>
</td>
<td width="60%">
If set, the Kerberos authentication credentials are cached. Kerberos or Negotiate authentication must be enabled by <b>AuthSchemes</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></a><a id="http_auth_ex_flag_capture_credential"></a><dl>
<dt><b>HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL</b></dt>
</dl>
</td>
<td width="60%">
 If set, the HTTP Server API captures the caller's credentials and uses them for Kerberos or Negotiate authentication. Kerberos or Negotiate authentication must be enabled by <b>AuthSchemes</b>.

</td>
</tr>
</table>

### -field DigestParams

The <a href="/windows/desktop/api/http/ns-http-http_server_authentication_digest_params">HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS</a> structure that provides the domain and realm for the digest challenge.

### -field BasicParams

The <a href="/windows/desktop/api/http/ns-http-http_server_authentication_basic_params">HTTP_SERVER_AUTHENTICATION_BASIC_PARAMS</a> structure that provides the realm for the basic challenge.

## -remarks

The <b>HTTP_SERVER_AUTHENTICATION_INFO</b> structure is included in the HTTP request if authentication has been configured on the associated URL group. The original HTTP authentication header received from the client is always included in the HTTP request, regardless of the authentication status.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/Http/http-auth-enable--constants">HTTP_AUTH_ENABLE</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>