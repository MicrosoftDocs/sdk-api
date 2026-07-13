---
UID: NF:rpcdce.RpcBindingSetAuthInfoExW
title: RpcBindingSetAuthInfoExW function (rpcdce.h)
description: The RpcBindingSetAuthInfoEx function sets a binding handle's authentication, authorization, and security quality-of-service information. (Unicode)
helpviewer_keywords: ["RpcBindingSetAuthInfoEx", "RpcBindingSetAuthInfoEx function [RPC]", "RpcBindingSetAuthInfoExW", "_rpc_rpcbindingsetauthinfoex", "rpc.rpcbindingsetauthinfoex", "rpcdce/RpcBindingSetAuthInfoEx", "rpcdce/RpcBindingSetAuthInfoExW"]
old-location: rpc\rpcbindingsetauthinfoex.htm
tech.root: Rpc
ms.assetid: 2438816c-995e-4398-999d-48a3538eec18
ms.date: 12/05/2018
ms.keywords: RpcBindingSetAuthInfoEx, RpcBindingSetAuthInfoEx function [RPC], RpcBindingSetAuthInfoExA, RpcBindingSetAuthInfoExW, _rpc_rpcbindingsetauthinfoex, rpc.rpcbindingsetauthinfoex, rpcdce/RpcBindingSetAuthInfoEx, rpcdce/RpcBindingSetAuthInfoExA, rpcdce/RpcBindingSetAuthInfoExW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingSetAuthInfoExW (Unicode) and RpcBindingSetAuthInfoExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcBindingSetAuthInfoExW
 - rpcdce/RpcBindingSetAuthInfoExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcBindingSetAuthInfoEx
 - RpcBindingSetAuthInfoExA
 - RpcBindingSetAuthInfoExW
---

# RpcBindingSetAuthInfoExW function


## -description

The 
<b>RpcBindingSetAuthInfoEx</b> function sets a binding handle's authentication, authorization, and security quality-of-service information.

## -parameters

### -param Binding

Server binding handle into which authentication and authorization information is set.

### -param ServerPrincName

Pointer to the expected principal name of the server referenced by <i>Binding</i>. The content of the name and its syntax are defined by the authentication service in use.

<div class="alert"><b>Note</b>  For the set of allowable target names for SSPs, please refer to the comments in the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a> documentation.</div>
<div> </div>

### -param AuthnLevel

Level of authentication to be performed on remote procedure calls made using <i>Binding</i>. For a list of the RPC-supported authentication levels, see 
<a href="/windows/desktop/Rpc/authentication-level-constants">Authentication-Level Constants</a>.

### -param AuthnSvc

Authentication service to use.

Specify RPC_C_AUTHN_NONE to turn off authentication for remote procedure calls made using <i>Binding</i>.

If RPC_C_AUTHN_DEFAULT is specified, the RPC run-time library uses the RPC_C_AUTHN_WINNT authentication service for remote procedure calls made using <i>Binding</i>.

### -param AuthIdentity

Handle for the structure that contains the client's authentication and authorization credentials appropriate for the selected authentication and authorization service. 




When using the <a href="/windows/desktop/Rpc/authentication-service-constants">RPC_C_AUTHN_WINNT</a> authentication service <i>AuthIdentity</i> should be a pointer to a 
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure (defined in Rpcdce.h). Kerberos and Negotiate authentication services also use the 
<b>SEC_WINNT_AUTH_IDENTITY</b> structure.

Specify a null value to use the security login context for the current address space. Pass the value RPC_C_NO_CREDENTIALS to use an anonymous log-in context. Note that RPC_C_NO_CREDENTIALS is only valid if RPC_C_AUTHN_GSS_SCHANNEL is selected as the authentication service.

### -param AuthzSvc

Authorization service implemented by the server for the interface of interest. The validity and trustworthiness of authorization data, like any application data, depends on the authentication service and authentication level selected. This parameter is ignored when using the RPC_C_AUTHN_WINNT authentication service. See Note.

### -param SecurityQOS

Pointer to the 
<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a> structure, which defines the security quality-of-service. 




<div class="alert"><b>Note</b>  For a list of the RPC-supported authentication services, see 
<a href="/windows/desktop/Rpc/authentication-service-constants">Authentication-Service Constants</a>.</div>
<div> </div>

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNKNOWN_AUTHN_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
Unknown authentication service.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A client application calls the 
<b>RpcBindingSetAuthInfoEx</b> function to set up a server binding handle for making authenticated remote procedure calls. This function provides the capability to set security quality-of-service information on the binding handle. It is otherwise identical to 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a>.

Unless a client calls 
<b>RpcBindingSetAuthInfoEx</b>, all remote procedure calls on <i>Binding</i> are unauthenticated. A client is not required to call this function.

The 
<b>RpcBindingSetAuthInfoEx</b> function takes a snapshot of the credentials. Therefore, the memory dedicated to the <i>AuthIdentity</i> parameter can be freed before the binding handle. The exception to this is when your application uses 
<b>RpcBindingSetAuthInfoEx</b> with RPC_C_QOS_IDENTITY_DYNAMIC and also specifies a non-<b>NULL</b> value for <i>AuthIdentity</i>.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a> function must not be called on a binding handle while an RPC call on the same handle is in progress. Doing so produces undefined results.</div>
<div> </div>
Due to the varying requirements of different versions of Microsoft RPC, Microsoft recommends that an application maintain a pointer to the <i>AuthIdentity</i> parameter for as long as the binding handle exists. Doing so increases the applications portability.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>For Windows XP SP2 and Windows Server 2003 SP1, the pointer to the <i>AuthIdentity</i> parameter need not be maintained for the life of the binding handle. This pointer must only be maintained if subsequent calls to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthinfo">RpcBindingInqAuthInfo</a> or <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa">RpcBindingInqAuthInfoEx</a> are made.

<div class="alert"><b>Note</b>  The <b>ncalrpc</b> protocol sequence supports only RPC_C_AUTHN_WINNT, but does support mutual authentication; supply an SPN and request mutual authentication through the <i>SecurityQOS</i> parameter to achieve this.</div>
<div> </div>




> [!NOTE]
> The rpcdce.h header defines RpcBindingSetAuthInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos">RPC_SECURITY_QOS</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa">RpcBindingInqAuthInfoEx</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a>
