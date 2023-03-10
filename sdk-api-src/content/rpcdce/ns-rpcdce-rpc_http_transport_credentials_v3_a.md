---
UID: NS:rpcdce._RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
title: RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A (rpcdce.h)
description: The RPC_HTTP_TRANSPORT_CREDENTIALS_V3 structure defines additional credentials to authenticate to an RPC proxy server or HTTP proxy server when using RPC/HTTP.RPC_HTTP_TRANSPORT_CREDENTIALS_V3 extends RPC_HTTP_TRANSPORT_CREDENTIALS_V2 by allowing arbitrary credential forms to be used. (ANSI)
helpviewer_keywords: ["*PRPC_HTTP_TRANSPORT_CREDENTIALS_V3_A","PRPC_HTTP_TRANSPORT_CREDENTIALS_V3","PRPC_HTTP_TRANSPORT_CREDENTIALS_V3 structure pointer [RPC]","RPC_C_HTTP_AUTHN_SCHEME_BASIC","RPC_C_HTTP_AUTHN_SCHEME_DIGEST","RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE","RPC_C_HTTP_AUTHN_SCHEME_NTLM","RPC_C_HTTP_AUTHN_SCHEME_PASSPORT","RPC_C_HTTP_AUTHN_TARGET_PROXY","RPC_C_HTTP_AUTHN_TARGET_SERVER","RPC_C_HTTP_FLAG_USE_FIRST_AUTH_SCHEME","RPC_C_HTTP_FLAG_USE_SSL","RPC_HTTP_TRANSPORT_CREDENTIALS_V3","RPC_HTTP_TRANSPORT_CREDENTIALS_V3 structure [RPC]","RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A","RPC_HTTP_TRANSPORT_CREDENTIALS_V3_W","_RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A","_RPC_HTTP_TRANSPORT_CREDENTIALS_V3_W","rpc.rpc_http_transport_credentials_v3","rpcdce/PRPC_HTTP_TRANSPORT_CREDENTIALS_V3","rpcdce/RPC_HTTP_TRANSPORT_CREDENTIALS_V3"]
old-location: rpc\rpc_http_transport_credentials_v3.htm
tech.root: Rpc
ms.assetid: 1d9d53bc-f1e2-4a8d-a9c1-5b2192ceec56
ms.date: 12/05/2018
ms.keywords: '*PRPC_HTTP_TRANSPORT_CREDENTIALS_V3_A, PRPC_HTTP_TRANSPORT_CREDENTIALS_V3, PRPC_HTTP_TRANSPORT_CREDENTIALS_V3 structure pointer [RPC], RPC_C_HTTP_AUTHN_SCHEME_BASIC, RPC_C_HTTP_AUTHN_SCHEME_DIGEST, RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE, RPC_C_HTTP_AUTHN_SCHEME_NTLM, RPC_C_HTTP_AUTHN_SCHEME_PASSPORT, RPC_C_HTTP_AUTHN_TARGET_PROXY, RPC_C_HTTP_AUTHN_TARGET_SERVER, RPC_C_HTTP_FLAG_USE_FIRST_AUTH_SCHEME, RPC_C_HTTP_FLAG_USE_SSL, RPC_HTTP_TRANSPORT_CREDENTIALS_V3, RPC_HTTP_TRANSPORT_CREDENTIALS_V3 structure [RPC], RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A, RPC_HTTP_TRANSPORT_CREDENTIALS_V3_W, _RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A, _RPC_HTTP_TRANSPORT_CREDENTIALS_V3_W, rpc.rpc_http_transport_credentials_v3, rpcdce/PRPC_HTTP_TRANSPORT_CREDENTIALS_V3, rpcdce/RPC_HTTP_TRANSPORT_CREDENTIALS_V3'
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A, *PRPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
 - rpcdce/_RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
 - PRPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
 - rpcdce/PRPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
 - RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
 - rpcdce/RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_HTTP_TRANSPORT_CREDENTIALS_V3
 - RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A
 - RPC_HTTP_TRANSPORT_CREDENTIALS_V3_W
---

# RPC_HTTP_TRANSPORT_CREDENTIALS_V3_A structure


## -description

The <b>RPC_HTTP_TRANSPORT_CREDENTIALS_V3</b> structure defines additional credentials to authenticate to an  RPC proxy server or HTTP proxy server when using RPC/HTTP.

<b>RPC_HTTP_TRANSPORT_CREDENTIALS_V3</b> extends <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a">RPC_HTTP_TRANSPORT_CREDENTIALS_V2</a> by allowing arbitrary credential forms to be used.

## -struct-fields

### -field TransportCredentials

A pointer to an opaque authentication handle in the form of an <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> structure.

### -field Flags

A set of flags that can be combined with the bitwise OR operator. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_HTTP_FLAG_USE_SSL"></a><a id="rpc_c_http_flag_use_ssl"></a><dl>
<dt><b>RPC_C_HTTP_FLAG_USE_SSL</b></dt>
</dl>
</td>
<td width="60%">
Instructs RPC to use SSL to communicate with the RPC Proxy.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_HTTP_FLAG_USE_FIRST_AUTH_SCHEME"></a><a id="rpc_c_http_flag_use_first_auth_scheme"></a><dl>
<dt><b>RPC_C_HTTP_FLAG_USE_FIRST_AUTH_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
When set, RPC chooses the first scheme in the <b>AuthnSchemes</b> array and attempts to authenticate to the RPC Proxy. If the RPC Proxy does not support the selected authentication scheme, the call fails. When not set, the RPC client queries the RPC Proxy for supported authentication schemes, and chooses one. 

</td>
</tr>
</table>

### -field AuthenticationTarget

Specifies the authentication target. 

Should be set to one or both of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_C_HTTP_AUTHN_TARGET_SERVER"></a><a id="rpc_c_http_authn_target_server"></a><dl>
<dt><b>RPC_C_HTTP_AUTHN_TARGET_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Authenticate against the RPC Proxy, which is the HTTP Server from an HTTP perspective. This is the most common value.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_C_HTTP_AUTHN_TARGET_PROXY"></a><a id="rpc_c_http_authn_target_proxy"></a><dl>
<dt><b>RPC_C_HTTP_AUTHN_TARGET_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Authenticate against the HTTP Proxy. This value is uncommon.

</td>
</tr>
</table>

### -field NumberOfAuthnSchemes

The number of elements in the <b>AuthnScheme</b> array.

### -field AuthnSchemes

A pointer to an array of authentication schemes the client is willing to use. Each element of the array can contain one of the following constants:

<a id="RPC_C_HTTP_AUTHN_SCHEME_BASIC"></a>
<a id="rpc_c_http_authn_scheme_basic"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_BASIC

<a id="RPC_C_HTTP_AUTHN_SCHEME_NTLM"></a>
<a id="rpc_c_http_authn_scheme_ntlm"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_NTLM

<a id="RPC_C_HTTP_AUTHN_SCHEME_PASSPORT"></a>
<a id="rpc_c_http_authn_scheme_passport"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_PASSPORT

<a id="RPC_C_HTTP_AUTHN_SCHEME_DIGEST"></a>
<a id="rpc_c_http_authn_scheme_digest"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_DIGEST

<a id="RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE"></a>
<a id="rpc_c_http_authn_scheme_negotiate"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE

 RPC_C_HTTP_AUTHN_SCHEME_PASSPORT,  RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE and RPC_C_HTTP_AUTHN_SCHEME_DIGEST are defined as constants, but not currently supported. Callers should not specify them; doing so results in RPC_S_CANNOT_SUPPORT error. Each constant can be specified once. RPC does not verify this restriction for performance reasons, but specifying  a constant more than once produces undefined results.

The algorithm for choosing the actual authentication scheme is as follows:

 If RPC_C_HTTP_FLAG_USE_FIRST_AUTH_SCHEME is specified, the first authentication scheme is chosen. If it is not supported by the server, the connection establishment fails. If RPC_C_HTTP_FLAG_USE_FIRST_AUTH_SCHEME is not specified, the RPC client first attempts anonymous connection to the RPC Proxy. If IIS returns authentication challenge, the RPC client chooses the authentication scheme preferred by the server if it is also in the <b>AuthnScheme</b> array. If the scheme preferred by the server is not in the <b>AuthnScheme</b> array, the <b>AuthnScheme</b> array will be traversed from start to finish, and if a scheme is found that is also supported by the server, that authentication scheme is used.

### -field ServerCertificateSubject

Contains an optional string with the expected server principal name. The principal name is in the same format as that generated for <a href="/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname">RpcCertGeneratePrincipalName</a> (see <a href="/windows/desktop/Rpc/principal-names">Principal Names</a> for more information). This member is used only when SSL is used. In such cases, the server certificate is checked against the generated principal name. If they do not match, an error is returned. This member enables clients to authenticate the RPC Proxy.

### -field ProxyCredentials

A pointer to an opaque authentication handle in the form of an <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a> structure when authenticating against an HTTP proxy server. <b>ProxyCredentials</b> is only valid when <b>AuthenticationTarget</b> contains <b>RPC_C_HTTP_AUTHN_TARGET_PROXY</b>.

### -field NumberOfProxyAuthnSchemes

The number of elements in the <b>ProxyAuthnSchemes</b> array when authenticating against an HTTP proxy server. <b>NumberOfProxyAuthnSchemes</b> is only valid when <b>AuthenticationTarget</b> contains <b>RPC_C_HTTP_AUTHN_TARGET_PROXY</b>.

### -field ProxyAuthnSchemes

A pointer to an array of authentication schemes the client is willing to use when authenticating against an HTTP proxy server. Each element of the array can contain one of the following constants. <b>ProxyAuthnSchemes</b> is only valid when <b>AuthenticationTarget</b> contains <b>RPC_C_HTTP_AUTHN_TARGET_PROXY</b>.

<a id="RPC_C_HTTP_AUTHN_SCHEME_BASIC"></a>
<a id="rpc_c_http_authn_scheme_basic"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_BASIC

<a id="RPC_C_HTTP_AUTHN_SCHEME_NTLM"></a>
<a id="rpc_c_http_authn_scheme_ntlm"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_NTLM

<a id="RPC_C_HTTP_AUTHN_SCHEME_PASSPORT"></a>
<a id="rpc_c_http_authn_scheme_passport"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_PASSPORT

<a id="RPC_C_HTTP_AUTHN_SCHEME_DIGEST"></a>
<a id="rpc_c_http_authn_scheme_digest"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_DIGEST

<a id="RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE"></a>
<a id="rpc_c_http_authn_scheme_negotiate"></a>


#### RPC_C_HTTP_AUTHN_SCHEME_NEGOTIATE

## -remarks

If the <b>TransportCredentials</b> member is <b>NULL</b> and the authentication scheme is NTLM, the credentials of the currently logged on user are used. To avoid exposing user credentials on the network through a weak LM hash, user logon credentials are used only if one or both of the following conditions are true:

<ul>
<li>Caller requested use of SSL and used the <b>ServerCertificateSubject</b> member. This scenario guarantees credentials are protected both in transit and at the final destination, even if a weak hash is used.</li>
<li>The lncompatibilitylevel key is set to 2 or higher. This  causes the NTLM security provider to emit or respond to only the strong NT hash, not the weak LM hash. In addition, customers are encouraged to use level 3 or higher, which will attempt NTLMv2.</li>
</ul>
If the Unicode version of the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a> function is used,  Unicode versions of the <b>RPC_HTTP_TRANSPORT_CREDENTIALS_V3</b> and <a href="/windows/desktop/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structures must also be provided, and the <b>Flags</b> member in <b>TransportCredentials</b> must be set to SEC_WINNT_AUTH_IDENTITY_UNICODE. 
If the ANSI version of the <b>RpcBindingSetAuthInfoEx</b> function is used,  ANSI versions of <b>RPC_HTTP_TRANSPORT_CREDENTIALS_V3</b> and <b>SEC_WINNT_AUTH_IDENTITY</b> structures must be provided, and the <b>Flags</b> member in <b>TransportCredentials</b> must be set to SEC_WINNT_AUTH_IDENTITY_ANSI.

## -see-also

<a href="/windows/desktop/Rpc/principal-names">Principal Names</a>



<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_a">RPC_HTTP_TRANSPORT_CREDENTIALS</a>



<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a">RPC_HTTP_TRANSPORT_CREDENTIALS_V2</a>



<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a>



<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v2_a">RPC_SECURITY_QOS_V2</a>



<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos_v3_a">RPC_SECURITY_QOS_V3</a>



<a href="/windows/desktop/Rpc/remote-procedure-calls-using-rpc-over-http">Remote Procedure Calls Using RPC over HTTP</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a>



<a href="/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname">RpcCertGeneratePrincipalName</a>



<a href="/windows/desktop/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a>
