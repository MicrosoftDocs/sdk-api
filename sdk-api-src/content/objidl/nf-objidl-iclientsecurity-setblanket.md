---
UID: NF:objidl.IClientSecurity.SetBlanket
title: IClientSecurity::SetBlanket (objidl.h)
description: Sets the authentication information (the security blanket) that will be used to make calls on the specified proxy.
helpviewer_keywords: ["IClientSecurity interface [COM]","SetBlanket method","IClientSecurity.SetBlanket","IClientSecurity::SetBlanket","SetBlanket","SetBlanket method [COM]","SetBlanket method [COM]","IClientSecurity interface","_com_iclientsecurity_setblanket","com.iclientsecurity_setblanket","objidlbase/IClientSecurity::SetBlanket"]
old-location: com\iclientsecurity_setblanket.htm
tech.root: com
ms.assetid: adb35089-2846-4782-8c96-d3d1e14beed9
ms.date: 12/05/2018
ms.keywords: IClientSecurity interface [COM],SetBlanket method, IClientSecurity.SetBlanket, IClientSecurity::SetBlanket, SetBlanket, SetBlanket method [COM], SetBlanket method [COM],IClientSecurity interface, _com_iclientsecurity_setblanket, com.iclientsecurity_setblanket, objidlbase/IClientSecurity::SetBlanket
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IClientSecurity::SetBlanket
 - objidl/IClientSecurity::SetBlanket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IClientSecurity.SetBlanket
---

# IClientSecurity::SetBlanket


## -description

Sets the authentication information (the security blanket) that will be used to make calls on the specified proxy.

This setting overrides the process default settings for the specified proxy. Calling this method changes the security values for all other users of the specified proxy.

## -parameters

### -param pProxy [in]

A pointer to the proxy.

### -param dwAuthnSvc [in]

The authentication service. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authentication-service-constants">authentication service constants</a>. If no authentication is required, use RPC_C_AUTHN_NONE. If RPC_C_AUTHN_DEFAULT is specified, COM will pick an authentication service following its normal security blanket negotiation algorithm.

### -param dwAuthzSvc [in]

The authorization service. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authorization-constants">authorization constants</a>. If RPC_C_AUTHZ_DEFAULT is specified, COM will pick an authorization service following its normal security blanket negotiation algorithm. If NTLMSSP, Kerberos, or Schannel is used as the authentication service, RPC_C_AUTHZ_NONE should be used as the authorization service.

### -param pServerPrincName [in]

The server principal name. If COLE_DEFAULT_PRINCIPAL is specified, DCOM will pick a principal name using its security blanket negotiation algorithm. If Kerberos is used as the authentication service, this parameter must be the correct principal name of the server or the call will fail.

If Schannel is used as the authentication service, this value must be one of the msstd or fullsic forms described in <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>, or <b>NULL</b> if you do not want mutual authentication.

Generally, specifying <b>NULL</b> will not reset server principal name on the proxy, rather, the previous setting will be retained. You must exercise care when using <b>NULL</b> as <i>pServerPrincName</i> when selecting a different authentication service for the proxy, because there is no guarantee that the previously set principal name would be valid for the newly selected authentication service.

### -param dwAuthnLevel [in]

The authentication level. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authentication-level-constants">authentication level constants</a>. If RPC_C_AUTHN_LEVEL_DEFAULT is specified, COM will pick an authentication level following its normal security blanket negotiation algorithm. If this value is set to RPC_C_AUTHN_LEVEL_NONE, the authentication service must be RPC_C_AUTHN_NONE. Each authentication service may choose to use a higher security authentication level than the one specified.

### -param dwImpLevel [in]

The impersonation level. This will be a single value taken from the list of <a href="/windows/desktop/com/com-impersonation-level-constants">impersonation level constants</a>. If RPC_C_IMP_LEVEL_DEFAULT is specified, COM will pick an impersonation level following its normal security blanket negotiation algorithm. If you are using NTLMSSP remotely, this value must be RPC_C_IMP_LEVEL_IMPERSONATE or RPC_C_IMP_LEVEL_IDENTIFY. When using NTLMSSP on the same computer, RPC_C_IMP_LEVEL_DELEGATE is also supported. For Kerberos, this value can be RPC_C_IMP_LEVEL_IDENTIFY, RPC_C_IMP_LEVEL_IMPERSONATE, or RPC_C_IMP_LEVEL_DELEGATE. For Schannel, this value must be RPC_C_IMP_LEVEL_IMPERSONATE.

### -param pAuthInfo [in]

An RPC_AUTH_IDENTITY_HANDLE value that indicates the identity of the client. This parameter is not used for calls on the same computer. If <i>pAuthInfo</i> is <b>NULL</b>, COM uses the current proxy identity, which is either the process token, the impersonation token, or the authentication identity from the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> function. If the handle is not <b>NULL</b>, that identity is used. The format of the structure referred to by the handle depends on the provider of the authentication service.

For NTLMSSP or Kerberos, the structure is a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If the client obtains the credentials set on the proxy by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>, it must ensure that the memory remains valid and unchanged until a different identity is set on the proxy or all proxies on the object are released.

If this parameter is <b>NULL</b>, COM uses the current proxy identity (which is either the process token or the impersonation token). If the handle refers to a structure, that identity is used.

For Schannel, this parameter must either be a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the client's X.509 certificate, or <b>NULL</b> if the client wishes to make an anonymous connection to the server. If a certificate is specified, the caller must not free it as long as any proxy to the object exists in the current apartment.

For Snego, this member is either <b>NULL</b>, points to a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure, or points to a <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If it is <b>NULL</b>, Snego will pick a list of authentication services based on those available on the client computer. If it points to a <b>SEC_WINNT_AUTH_IDENTITY_EX</b> structure, the structure's <b>PackageList</b> member must point to a string containing a comma-separated list of authentication service names and the <b>PackageListLength</b> member must give the number of bytes in the <b>PackageList</b> string. If <b>PackageList</b> is <b>NULL</b>, all calls using Snego will fail.

If COLE_DEFAULT_AUTHINFO is specified, COM will pick the authentication information following its normal security blanket negotiation algorithm.

<b>SetBlanket</b> will return an error if both <i>pAuthInfo</i> is set and one of the cloaking flags is set in <i>dwCapabilities</i>.

### -param dwCapabilities [in]

The capabilities of this proxy. Capability flags are defined in the <a href="/windows/desktop/api/objidl/ne-objidl-eole_authentication_capabilities">EOLE_AUTHENTICATION_CAPABILITIES</a> enumeration. The only flags that can be set through this method are EOAC_MUTUAL_AUTH, EOAC_STATIC_CLOAKING, EOAC_DYNAMIC_CLOAKING, EOAC_ANY_AUTHORITY (this flag is deprecated), EOAC_MAKE_FULLSIC, and EOAC_DEFAULT. Either EOAC_STATIC_CLOAKING or EOAC_DYNAMIC_CLOAKING can be set if <i>pAuthInfo</i> is not set and Schannel is not the authentication service. (See <a href="/windows/desktop/com/cloaking">Cloaking</a> for more information.) If any capability flags other than those mentioned here are indicated, <b>SetBlanket</b> will return an error.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
</table>

## -remarks

<b>SetBlanket</b> sets the authentication information that will be used to make calls on the specified interface proxy. The values specified here override the values chosen by automatic security. Calling this method changes the security values for all other users of the specified proxy. If you want the changes to apply only to a particular instance of a proxy, call <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-copyproxy">IClientSecurity::CopyProxy</a> to make a private copy of the proxy and then call <b>SetBlanket</b> on the copy.

Whenever this method is called, DCOM will set the identity on the proxy, and future calls made using this proxy will use this identity. Calls in progress when <b>SetBlanket</b> is called will use the authentication information on the proxy at the time the call was started. If <i>pAuthInfo</i> is <b>NULL</b>, the proxy identity defaults to the current process token (unless an authentication identity was specified on a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>). See <a href="/windows/desktop/com/cloaking">Cloaking</a> to learn how the cloaking flags affect the proxy when <i>pAuthInfo</i> is <b>NULL</b>.

By default, COM will choose the first available authentication service and authorization service available on both the client and server computers and the principal name that the server registered for that authentication service. Currently, COM will not try another authentication service if the first fails.

When the default constant for <i>dwImpLevel</i> is specified in <b>SetBlanket</b>, the parameter defaults to the value specified to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>. If <b>CoInitializeSecurity</b> is not called, it defaults to RPC_C_IMP_LEVEL_IDENTIFY.

The initial value for dwAuthnLevel on a proxy will be the higher of the value set on the client's call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> and the server's call to <b>CoInitializeSecurity</b>. For any process that did not call <b>CoInitializeSecurity</b>, the default authentication level is RPC_C_AUTHN_CONNECT.

The default authentication and impersonation level for processes that do not call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> can be set with DCOMCNFG.

If EOAC_DEFAULT is specified for <i>dwCapabilities</i>, the valid capabilities from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> will be used. If <b>CoInitializeSecurity</b> was not called, EOAC_NONE will be used for the capabilities flag.

If <b>SetBlanket</b> is called simultaneously on two threads on the same proxy, only one set of changes will be applied. If <b>SetBlanket</b> and <b>CRpcOptions::Set</b> are called simultaneously on two threads on the same proxy, both changes may be applied or only one may be applied.

Security information cannot be set on local interfaces such as the <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> interface. However, since that interface is only supported locally, there is no need for security. <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a> are special cases. The location implementation makes remote calls to support these interfaces. <b>SetBlanket</b> can be used for <b>IUnknown</b>. <b>IMultiQI</b> will use the security settings on <b>IUnknown</b>.

To change one <b>SetBlanket</b> parameter without having to deal with the others, one can specify the default constants for the other parameters. Applications can change a parameter (such as the authentication level) and ignore the other parameters, including the authentication service, by setting all other parameters to the default constants.

Note that it is important to set all unused parameters to the default constants because the default value is often not obvious. In particular, if you set the authentication service to the default, you should set the authentication information and principal name to the default. The reasons for this are twofold: First, the type of the authentication information depends on the authentication service DCOM chooses. Second, because DCOM needs to pass some complex authentication information for certain authentication services, if you set the authentication service to default and the authentication information to <b>NULL</b>, you might get a security setting that will not work.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>