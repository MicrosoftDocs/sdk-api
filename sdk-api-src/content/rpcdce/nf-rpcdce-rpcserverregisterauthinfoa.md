---
UID: NF:rpcdce.RpcServerRegisterAuthInfoA
title: RpcServerRegisterAuthInfoA function (rpcdce.h)
description: The RpcServerRegisterAuthInfo function registers authentication information with the RPC run-time library. (RpcServerRegisterAuthInfoA)
helpviewer_keywords: ["RpcServerRegisterAuthInfoA", "rpcdce/RpcServerRegisterAuthInfoA"]
old-location: rpc\rpcserverregisterauthinfo.htm
tech.root: Rpc
ms.assetid: b7a7b57e-540b-460b-9eec-6246cc1fd9d3
ms.date: 12/05/2018
ms.keywords: RpcServerRegisterAuthInfo, RpcServerRegisterAuthInfo function [RPC], RpcServerRegisterAuthInfoA, RpcServerRegisterAuthInfoW, _rpc_rpcserverregisterauthinfo, rpc.rpcserverregisterauthinfo, rpcdce/RpcServerRegisterAuthInfo, rpcdce/RpcServerRegisterAuthInfoA, rpcdce/RpcServerRegisterAuthInfoW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcServerRegisterAuthInfoW (Unicode) and RpcServerRegisterAuthInfoA (ANSI)
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
 - RpcServerRegisterAuthInfoA
 - rpcdce/RpcServerRegisterAuthInfoA
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
 - RpcServerRegisterAuthInfo
 - RpcServerRegisterAuthInfoA
 - RpcServerRegisterAuthInfoW
---

# RpcServerRegisterAuthInfoA function


## -description

The 
<b>RpcServerRegisterAuthInfo</b> function registers authentication information with the RPC run-time library.

## -parameters

### -param ServerPrincName

Pointer to the principal name to use for the server when authenticating remote procedure calls using the service specified by the <i>AuthnSvc</i> parameter. The content of the name and its syntax are defined by the authentication service in use. For more information, see 
<a href="/windows/desktop/Rpc/principal-names">Principal Names</a>.

### -param AuthnSvc

Authentication service to use when the server receives a request for a remote procedure call.

### -param GetKeyFn

Address of a server-application-provided routine that returns encryption keys. See 
<a href="/windows/desktop/api/rpcdce/nc-rpcdce-rpc_auth_key_retrieval_fn">RPC_AUTH_KEY_RETRIEVAL_FN</a>. 




Specify a <b>NULL</b> parameter value to use the default method of encryption-key acquisition. In this case, the authentication service specifies the default behavior. Set this parameter to <b>NULL</b> when using the RPC_C_AUTHN_WINNT authentication service.

<table>
<tr>
<th>Authentication service</th>
<th>GetKeyFn</th>
<th>Arg</th>
<th>Run-time behavior</th>
</tr>
<tr>
<td>RPC_C_AUTHN_DPA</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_GSS_KERBEROS</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_GSS_NEGOTIATE</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_GSS_SCHANNEL</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_MQ</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_MSN</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_WINNT</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Does not support</td>
</tr>
<tr>
<td>RPC_C_AUTHN_DCE_PRIVATE</td>
<td><b>NULL</b></td>
<td>Non-<b>null</b></td>
<td>Uses default method of encryption-key acquisition from specified key table; specified argument is passed to default acquisition function.</td>
</tr>
<tr>
<td>RPC_C_AUTHN_DCE_PRIVATE</td>
<td>Non-<b>null</b></td>
<td><b>NULL</b></td>
<td>Uses specified encryption-key acquisition function to obtain keys from default key table.</td>
</tr>
<tr>
<td>RPC_C_AUTHN_DCE_PRIVATE</td>
<td>Non-<b>null</b></td>
<td>Non-<b>null</b></td>
<td>Uses specified encryption-key acquisition function to obtain keys from specified key table; specified argument is passed to acquisition function.</td>
</tr>
<tr>
<td>RPC_C_AUTHN_DEC_PUBLIC</td>
<td>Ignored</td>
<td>Ignored</td>
<td>Reserved for future use.</td>
</tr>
</table>
 


<div> </div>


The RPC run-time library passes the <i>ServerPrincName</i> parameter value from 
<b>RpcServerRegisterAuthInfo</b> as the <i>ServerPrincName</i> parameter value to the <i>GetKeyFn</i> acquisition function. The RPC run-time library automatically provides a value for the key version (<i>KeyVer</i>) parameter. For a <i>KeyVer</i> parameter value of zero, the acquisition function must return the most recent key available. The retrieval function returns the authentication key in the <i>Key</i> parameter.

If the acquisition function called from 
<b>RpcServerRegisterAuthInfo</b> returns a status other than RPC_S_OK, then this function fails and returns an error code to the server application. If the acquisition function called by the RPC run-time library while authenticating a client's remote procedure call request returns a status other than RPC_S_OK, the request fails and the RPC run-time library returns an error code to the client application.

### -param Arg

Pointer to a parameter to pass to the <i>GetKeyFn</i> routine, if specified. This parameter can also be used to pass a pointer to an 
<a href="/windows/desktop/api/schannel/ns-schannel-schannel_cred">SCHANNEL_CRED</a> structure to specify explicit credentials if the authentication service is set to SCHANNEL. 


If the <i>Arg</i> parameter is set to <b>NULL</b>, this function will use the default certificate or credential if it has been set up in the directory service.

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
<dt><b>RPC_S_UNKNOWN_AUTHN_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
The authentication service is unknown.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server application calls 
<b>RpcServerRegisterAuthInfo</b> to register an authentication service to use for authenticating remote procedure calls. A server calls this routine once for each authentication service the server wants to register. If the server calls this function more than once for a given authentication service, the results are undefined.

The authentication service that a client application specifies (using 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a> or 
<b>RpcServerRegisterAuthInfo</b>) must be one of the authentication services specified by the server application. Otherwise, the client's remote procedure call fails and an RPC_S_UNKNOWN_AUTHN_SERVICE status code is returned.





> [!NOTE]
> The rpcdce.h header defines RpcServerRegisterAuthInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a>
