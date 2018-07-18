---
UID: NF:objidl.IClientSecurity.SetBlanket
title: IClientSecurity::SetBlanket
author: windows-sdk-content
description: Sets the authentication information (the security blanket) that will be used to make calls on the specified proxy.
old-location: com\iclientsecurity_setblanket.htm
old-project: com
ms.assetid: adb35089-2846-4782-8c96-d3d1e14beed9
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IClientSecurity interface [COM],SetBlanket method, IClientSecurity.SetBlanket, IClientSecurity::SetBlanket, SetBlanket, SetBlanket method [COM], SetBlanket method [COM],IClientSecurity interface, _com_iclientsecurity_setblanket, com.iclientsecurity_setblanket, objidlbase/IClientSecurity::SetBlanket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IClientSecurity.SetBlanket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IClientSecurity::SetBlanket


## -description


Sets the authentication information (the security blanket) that will be used to make calls on the specified proxy.

This setting overrides the process default settings for the specified proxy. Calling this method changes the security values for all other users of the specified proxy.


## -parameters




### -param pProxy [in]

A pointer to the proxy.


### -param dwAuthnSvc [in]

The authentication service. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">authentication service constants</a>. If no authentication is required, use RPC_C_AUTHN_NONE. If RPC_C_AUTHN_DEFAULT is specified, COM will pick an authentication service following its normal security blanket negotiation algorithm.


### -param dwAuthzSvc [in]

The authorization service. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">authorization constants</a>. If RPC_C_AUTHZ_DEFAULT is specified, COM will pick an authorization service following its normal security blanket negotiation algorithm. If NTLMSSP, Kerberos, or Schannel is used as the authentication service, RPC_C_AUTHZ_NONE should be used as the authorization service.


### -param pServerPrincName [in]

The server principal name. If COLE_DEFAULT_PRINCIPAL is specified, DCOM will pick a principal name using its security blanket negotiation algorithm. If Kerberos is used as the authentication service, this parameter must be the correct principal name of the server or the call will fail.

If Schannel is used as the authentication service, this value must be one of the msstd or fullsic forms described in <a href="https://msdn.microsoft.com/4d9977f8-0efb-4559-977e-3eba4e277bc0">Principal Names</a>, or <b>NULL</b> if you do not want mutual authentication.

Generally, specifying <b>NULL</b> will not reset server principal name on the proxy, rather, the previous setting will be retained. You must exercise care when using <b>NULL</b> as <i>pServerPrincName</i> when selecting a different authentication service for the proxy, because there is no guarantee that the previously set principal name would be valid for the newly selected authentication service.


### -param dwAuthnLevel [in]

The authentication level. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/06c409e4-3772-45cf-8c31-c64f99aca244">authentication level constants</a>. If RPC_C_AUTHN_LEVEL_DEFAULT is specified, COM will pick an authentication level following its normal security blanket negotiation algorithm. If this value is set to RPC_C_AUTHN_LEVEL_NONE, the authentication service must be RPC_C_AUTHN_NONE. Each authentication service may choose to use a higher security authentication level than the one specified.


### -param dwImpLevel [in]

The impersonation level. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/ea5a3b46-b607-4192-a3cc-b2ec55ca94a6">impersonation level constants</a>. If RPC_C_IMP_LEVEL_DEFAULT is specified, COM will pick an impersonation level following its normal security blanket negotiation algorithm. If you are using NTLMSSP remotely, this value must be RPC_C_IMP_LEVEL_IMPERSONATE or RPC_C_IMP_LEVEL_IDENTIFY. When using NTLMSSP on the same computer, RPC_C_IMP_LEVEL_DELEGATE is also supported. For Kerberos, this value can be RPC_C_IMP_LEVEL_IDENTIFY, RPC_C_IMP_LEVEL_IMPERSONATE, or RPC_C_IMP_LEVEL_DELEGATE. For Schannel, this value must be RPC_C_IMP_LEVEL_IMPERSONATE.


### -param pAuthInfo [in]

An RPC_AUTH_IDENTITY_HANDLE value that indicates the identity of the client. This parameter is not used for calls on the same computer. If <i>pAuthInfo</i> is <b>NULL</b>, COM uses the current proxy identity, which is either the process token, the impersonation token, or the authentication identity from the <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> function. If the handle is not <b>NULL</b>, that identity is used. The format of the structure referred to by the handle depends on the provider of the authentication service.

For NTLMSSP or Kerberos, the structure is a <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="https://msdn.microsoft.com/6b95bce8-5613-4403-9bda-16262596bb1b">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If the client obtains the credentials set on the proxy by calling <a href="https://msdn.microsoft.com/e613e06a-0900-413e-bde2-39ce1612fed1">CoQueryProxyBlanket</a>, it must ensure that the memory remains valid and unchanged until a different identity is set on the proxy or all proxies on the object are released.

If this parameter is <b>NULL</b>, COM uses the current proxy identity (which is either the process token or the impersonation token). If the handle refers to a structure, that identity is used.

For Schannel, this parameter must either be a pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the client's X.509 certificate, or <b>NULL</b> if the client wishes to make an anonymous connection to the server. If a certificate is specified, the caller must not free it as long as any proxy to the object exists in the current apartment.

For Snego, this member is either <b>NULL</b>, points to a <a href="https://msdn.microsoft.com/a9c9471b-2134-4173-af86-18b277627d2a">SEC_WINNT_AUTH_IDENTITY</a> structure, or points to a <a href="https://msdn.microsoft.com/6b95bce8-5613-4403-9bda-16262596bb1b">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. If it is <b>NULL</b>, Snego will pick a list of authentication services based on those available on the client computer. If it points to a <b>SEC_WINNT_AUTH_IDENTITY_EX</b> structure, the structure's <b>PackageList</b> member must point to a string containing a comma-separated list of authentication service names and the <b>PackageListLength</b> member must give the number of bytes in the <b>PackageList</b> string. If <b>PackageList</b> is <b>NULL</b>, all calls using Snego will fail.

If COLE_DEFAULT_AUTHINFO is specified, COM will pick the authentication information following its normal security blanket negotiation algorithm.

<b>SetBlanket</b> will return an error if both <i>pAuthInfo</i> is set and one of the cloaking flags is set in <i>dwCapabilities</i>.


### -param dwCapabilities [in]

The capabilities of this proxy. Capability flags are defined in the <a href="https://msdn.microsoft.com/cf3396d0-6674-4f12-bd4a-227a8d32bc92">EOLE_AUTHENTICATION_CAPABILITIES</a> enumeration. The only flags that can be set through this method are EOAC_MUTUAL_AUTH, EOAC_STATIC_CLOAKING, EOAC_DYNAMIC_CLOAKING, EOAC_ANY_AUTHORITY (this flag is deprecated), EOAC_MAKE_FULLSIC, and EOAC_DEFAULT. Either EOAC_STATIC_CLOAKING or EOAC_DYNAMIC_CLOAKING can be set if <i>pAuthInfo</i> is not set and Schannel is not the authentication service. (See <a href="https://msdn.microsoft.com/5b97d9d6-8fa9-4da2-8351-64772227d9a2">Cloaking</a> for more information.) If any capability flags other than those mentioned here are indicated, <b>SetBlanket</b> will return an error.


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



<b>SetBlanket</b> sets the authentication information that will be used to make calls on the specified interface proxy. The values specified here override the values chosen by automatic security. Calling this method changes the security values for all other users of the specified proxy. If you want the changes to apply only to a particular instance of a proxy, call <a href="https://msdn.microsoft.com/4664351b-d43b-45dc-800e-574685afd0f6">IClientSecurity::CopyProxy</a> to make a private copy of the proxy and then call <b>SetBlanket</b> on the copy.

Whenever this method is called, DCOM will set the identity on the proxy, and future calls made using this proxy will use this identity. Calls in progress when <b>SetBlanket</b> is called will use the authentication information on the proxy at the time the call was started. If <i>pAuthInfo</i> is <b>NULL</b>, the proxy identity defaults to the current process token (unless an authentication identity was specified on a call to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>). See <a href="https://msdn.microsoft.com/5b97d9d6-8fa9-4da2-8351-64772227d9a2">Cloaking</a> to learn how the cloaking flags affect the proxy when <i>pAuthInfo</i> is <b>NULL</b>.

By default, COM will choose the first available authentication service and authorization service available on both the client and server computers and the principal name that the server registered for that authentication service. Currently, COM will not try another authentication service if the first fails.

When the default constant for <i>dwImpLevel</i> is specified in <b>SetBlanket</b>, the parameter defaults to the value specified to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>. If <b>CoInitializeSecurity</b> is not called, it defaults to RPC_C_IMP_LEVEL_IDENTIFY.

The initial value for dwAuthnLevel on a proxy will be the higher of the value set on the client's call to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> and the server's call to <b>CoInitializeSecurity</b>. For any process that did not call <b>CoInitializeSecurity</b>, the default authentication level is RPC_C_AUTHN_CONNECT.

The default authentication and impersonation level for processes that do not call <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> can be set with DCOMCNFG.

If EOAC_DEFAULT is specified for <i>dwCapabilities</i>, the valid capabilities from <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> will be used. If <b>CoInitializeSecurity</b> was not called, EOAC_NONE will be used for the capabilities flag.

If <b>SetBlanket</b> is called simultaneously on two threads on the same proxy, only one set of changes will be applied. If <b>SetBlanket</b> and <b>CRpcOptions::Set</b> are called simultaneously on two threads on the same proxy, both changes may be applied or only one may be applied.

Security information cannot be set on local interfaces such as the <a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a> interface. However, since that interface is only supported locally, there is no need for security. <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/5e50396f-2931-403f-946a-dc096cb012cc">IMultiQI</a> are special cases. The location implementation makes remote calls to support these interfaces. <b>SetBlanket</b> can be used for <b>IUnknown</b>. <b>IMultiQI</b> will use the security settings on <b>IUnknown</b>.

To change one <b>SetBlanket</b> parameter without having to deal with the others, one can specify the default constants for the other parameters. Applications can change a parameter (such as the authentication level) and ignore the other parameters, including the authentication service, by setting all other parameters to the default constants.

Note that it is important to set all unused parameters to the default constants because the default value is often not obvious. In particular, if you set the authentication service to the default, you should set the authentication information and principal name to the default. The reasons for this are twofold: First, the type of the authentication information depends on the authentication service DCOM chooses. Second, because DCOM needs to pass some complex authentication information for certain authentication services, if you set the authentication service to default and the authentication information to <b>NULL</b>, you might get a security setting that will not work.




## -see-also




<a href="https://msdn.microsoft.com/e613e06a-0900-413e-bde2-39ce1612fed1">CoQueryProxyBlanket</a>



<a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>



<a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a>
 

 

