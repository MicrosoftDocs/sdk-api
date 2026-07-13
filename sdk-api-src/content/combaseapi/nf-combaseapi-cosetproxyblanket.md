---
UID: NF:combaseapi.CoSetProxyBlanket
title: CoSetProxyBlanket function (combaseapi.h)
description: Sets the authentication information that will be used to make calls on the specified proxy.
helpviewer_keywords: ["CoSetProxyBlanket","CoSetProxyBlanket function [COM]","_com_CoSetProxyBlanket","com.cosetproxyblanket","combaseapi/CoSetProxyBlanket"]
old-location: com\cosetproxyblanket.htm
tech.root: com
ms.assetid: c2e5e681-8fa5-4b02-b59d-ba796eb0dccf
ms.date: 12/05/2018
ms.keywords: CoSetProxyBlanket, CoSetProxyBlanket function [COM], _com_CoSetProxyBlanket, com.cosetproxyblanket, combaseapi/CoSetProxyBlanket
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoSetProxyBlanket
 - combaseapi/CoSetProxyBlanket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoSetProxyBlanket
---

# CoSetProxyBlanket function


## -description

Sets the authentication information that will be used to make calls on the specified proxy. This is a helper function for <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a>.

## -parameters

### -param pProxy [in]

The proxy to be set.

### -param dwAuthnSvc [in]

The authentication service to be used. For a list of possible values, see <a href="/windows/desktop/com/com-authentication-service-constants">Authentication Service Constants</a>. Use RPC_C_AUTHN_NONE if no authentication is required. If RPC_C_AUTHN_DEFAULT is specified, DCOM will pick an authentication service following its normal security blanket negotiation algorithm.

### -param dwAuthzSvc [in]

The authorization service to be used. For a list of possible values, see <a href="/windows/desktop/com/com-authorization-constants">Authorization Constants</a>. If RPC_C_AUTHZ_DEFAULT is specified, DCOM will pick an authorization service following its normal security blanket negotiation algorithm. RPC_C_AUTHZ_NONE should be used as the authorization service if NTLMSSP, Kerberos, or Schannel is used as the authentication service.

### -param pServerPrincName [in, optional]

The server principal name to be used with the authentication service. If COLE_DEFAULT_PRINCIPAL is specified, DCOM will pick a principal name using its security blanket negotiation algorithm. If Kerberos is used as the authentication service, this value must not be <b>NULL</b>. It must be the correct principal name of the server or the call will fail.

If Schannel is used as the authentication service, this value must be one of the msstd or fullsic forms described in <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>, or <b>NULL</b> if you do not want mutual authentication.

Generally, specifying <b>NULL</b> will not reset the server principal name on the proxy; rather, the previous setting will be retained. You must be careful when using <b>NULL</b> as <i>pServerPrincName</i> when selecting a different authentication service for the proxy, because there is no guarantee that the previously set principal name would be valid for the newly selected authentication service.

### -param dwAuthnLevel [in]

The authentication level to be used. For a list of possible values, see <a href="/windows/desktop/com/com-authentication-level-constants">Authentication Level Constants</a>. If RPC_C_AUTHN_LEVEL_DEFAULT is specified, DCOM will pick an authentication level following its normal security blanket negotiation algorithm. If this value is none, the authentication service must also be none.

### -param dwImpLevel [in]

The impersonation level to be used. For a list of possible values, see <a href="/windows/desktop/com/com-impersonation-level-constants">Impersonation Level Constants</a>. If RPC_C_IMP_LEVEL_DEFAULT is specified, DCOM will pick an impersonation level following its normal security blanket negotiation algorithm. If NTLMSSP is the authentication service, this value must be RPC_C_IMP_LEVEL_IMPERSONATE or RPC_C_IMP_LEVEL_IDENTIFY. NTLMSSP also supports delegate-level impersonation (RPC_C_IMP_LEVEL_DELEGATE) on the same computer. If Schannel is the authentication service, this parameter must be RPC_C_IMP_LEVEL_IMPERSONATE.

### -param pAuthInfo [in, optional]

A pointer to an <b>RPC_AUTH_IDENTITY_HANDLE</b> value that establishes the identity of the client. The format of the structure referred to by the handle depends on the provider of the authentication service.

For calls on the same computer, RPC logs on the user with the supplied credentials and uses the resulting token for the method call. 

For NTLMSSP or Kerberos, the structure is a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure.  The client can discard  <i>pAuthInfo</i> after calling the API. RPC does not keep a copy of the <i>pAuthInfo</i> pointer, and the client cannot retrieve it later in the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a> method. 

If this parameter is <b>NULL</b>, DCOM uses the current proxy identity (which is either the process token or the impersonation token). If the handle refers to a structure, that identity is used.

For Schannel, this parameter must be either a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the client's X.509 certificate or is <b>NULL</b> if the client wishes to make an anonymous connection to the server. If a certificate is specified, the caller must not free it as long as any proxy to the object exists in the current apartment.

For Snego, this member is either <b>NULL</b>, points to a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure, or points to a <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If it is <b>NULL</b>, Snego will pick a list of authentication services based on those available on the client computer. If it points to a <b>SEC_WINNT_AUTH_IDENTITY_EX</b> structure, the structure's <b>PackageList</b> member must point to a string containing a comma-separated list of authentication service names and the <b>PackageListLength</b> member must give the number of bytes in the <b>PackageList</b> string. If <b>PackageList</b> is <b>NULL</b>, all calls using Snego will fail.

If COLE_DEFAULT_AUTHINFO is specified for this parameter, DCOM will pick the authentication information following its normal security blanket negotiation algorithm.

<b>CoSetProxyBlanket</b> will fail if <i>pAuthInfo</i> is set and one of the cloaking flags is set in the <i>dwCapabilities</i> parameter.

### -param dwCapabilities [in]

The capabilities of this proxy. For a list of possible values, see the <a href="/windows/desktop/api/objidl/ne-objidl-eole_authentication_capabilities">EOLE_AUTHENTICATION_CAPABILITIES</a> enumeration. The only flags that can be set through this function are EOAC_MUTUAL_AUTH, EOAC_STATIC_CLOAKING, EOAC_DYNAMIC_CLOAKING, EOAC_ANY_AUTHORITY (this flag is deprecated), EOAC_MAKE_FULLSIC, and EOAC_DEFAULT. Either EOAC_STATIC_CLOAKING or EOAC_DYNAMIC_CLOAKING can be set if <i>pAuthInfo</i> is not set and Schannel is not the authentication service. (See <a href="/windows/desktop/com/cloaking">Cloaking</a> for more information.) If any capability flags other than those mentioned here are set, <b>CoSetProxyBlanket</b> will fail.

## -returns

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments is invalid.

</td>
</tr>
</table>

## -remarks

<b>CoSetProxyBlanket</b> sets the authentication information that will be used to make calls on the specified proxy. This function encapsulates the following sequence of common calls (error handling excluded).


```C++
    pProxy->QueryInterface(IID_IClientSecurity, (void**)&pcs);
    pcs->SetBlanket(pProxy, dwAuthnSvc, dwAuthzSvc, pServerPrincName, 
        dwAuthnLevel, dwImpLevel, pAuthInfo, dwCapabilities);
    pcs->Release();

```

This sequence calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the proxy to get a pointer to <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>, and with the resulting pointer, calls <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> and then releases the pointer.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>



<a href="/windows/desktop/com/setting-security-at-the-interface-proxy-level">Setting Security at the Interface Proxy Level</a>
