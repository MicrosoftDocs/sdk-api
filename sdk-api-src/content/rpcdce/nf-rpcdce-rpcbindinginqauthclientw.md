---
UID: NF:rpcdce.RpcBindingInqAuthClientW
title: RpcBindingInqAuthClientW function (rpcdce.h)
description: The RpcBindingInqAuthClientW (Unicode) function (rpcdce.h) gets the principal name or privilege attributes of the client that made the remote procedure call.
helpviewer_keywords: ["RpcBindingInqAuthClient", "RpcBindingInqAuthClient function [RPC]", "RpcBindingInqAuthClientW", "_rpc_rpcbindinginqauthclient", "rpc.rpcbindinginqauthclient", "rpcdce/RpcBindingInqAuthClient", "rpcdce/RpcBindingInqAuthClientW"]
old-location: rpc\rpcbindinginqauthclient.htm
tech.root: Rpc
ms.assetid: 2834a6a8-8bd6-4829-84ea-e3f35c917ab7
ms.date: 08/16/2022
ms.keywords: RpcBindingInqAuthClient, RpcBindingInqAuthClient function [RPC], RpcBindingInqAuthClientA, RpcBindingInqAuthClientW, _rpc_rpcbindinginqauthclient, rpc.rpcbindinginqauthclient, rpcdce/RpcBindingInqAuthClient, rpcdce/RpcBindingInqAuthClientA, rpcdce/RpcBindingInqAuthClientW
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingInqAuthClientW (Unicode) and RpcBindingInqAuthClientA (ANSI)
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
 - RpcBindingInqAuthClientW
 - rpcdce/RpcBindingInqAuthClientW
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
 - RpcBindingInqAuthClient
 - RpcBindingInqAuthClientA
 - RpcBindingInqAuthClientW
---

# RpcBindingInqAuthClientW function


## -description

A server application calls the 
<b>RpcBindingInqAuthClient</b> function to obtain the principal name or privilege attributes of the authenticated client that made the remote procedure call.

## -parameters

### -param ClientBinding

Client binding handle of the client that made the remote procedure call. This value can be zero. See Remarks.

### -param Privs

Returns a pointer to a handle to the privileged information for the client application that made the remote procedure call on the <i>ClientBinding</i> binding handle. For <b>ncalrpc</b> calls, <i>Privs</i> contains a string with the client's principal name.

The data referenced by this parameter is read-only and should not be modified by the server application. If the server wants to preserve any of the returned data, the server must copy the data into server-allocated memory.

The data that the <i>Privs</i> parameter points to comes directly from the SSP. Therefore, the format of the data is specific to the SSP. For more information on SSPs, see 
<a href="/windows/desktop/Rpc/security-support-providers-ssps-">Security Support Providers (SSPs)</a>.

### -param ServerPrincName

Returns a pointer to a pointer to the server principal name specified by the server application that called the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo">RpcServerRegisterAuthInfo</a> function. The content of the returned name and its syntax are defined by the authentication service in use. For the SCHANNEL SSP, the principal name is in Microsoft-standard (msstd) format. For further information on msstd format, see 
<a href="/windows/desktop/Rpc/principal-names">Principal Names</a>.

Specify a null value to prevent 
<b>RpcBindingInqAuthClient</b> from returning the <i>ServerPrincName</i> parameter. In this case, the application does not call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function.

### -param AuthnLevel

Returns a pointer set to the level of authentication requested by the client application that made the remote procedure call on the <i>ClientBinding</i> binding handle.

Specify a null value to prevent 
<b>RpcBindingInqAuthClient</b> from returning the <i>AuthnLevel</i> parameter.

### -param AuthnSvc

Returns a pointer set to the authentication service requested by the client application that made the remote procedure call on the <i>ClientBinding</i> binding handle. For a list of the RPC-supported authentication levels, see 
<a href="/windows/desktop/Rpc/authentication-level-constants">Authentication-Level Constants</a>.

Specify a null value to prevent 
<b>RpcBindingInqAuthClient</b> from returning the <i>AuthnSvc</i> parameter.

### -param AuthzSvc

Returns a pointer set to the authorization service requested by the client application that made the remote procedure call on the <i>ClientBinding</i> binding handle.

Specify a null value to prevent 
<b>RpcBindingInqAuthClient</b> from returning the <i>AuthzSvc</i> parameter. This parameter is not used by the RPC_C_AUTHN_WINNT authentication service. The returned value will always be RPC_C_AUTHZ_NONE.

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
<dt><b>RPC_S_BINDING_HAS_NO_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Binding has no authentication information.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A server application calls the 
<b>RpcBindingInqAuthClient</b> function to obtain the principal name or privilege attributes of the authenticated client that made the remote procedure call. In addition, 
<b>RpcBindingInqAuthClient</b> returns the authentication service, authentication level, and server principal name specified by the client. The server can use the returned data for authorization purposes.

The RPC run-time library allocates memory for the returned <i>ServerPrincName</i> parameter. The application is responsible for calling the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> function for the returned argument string.

For synchronous RPC calls, the server application can use zero as the value for the <i>ClientBinding</i> parameter. Using zero retrieves the authentication and authorization information from the currently executing remote procedure call.





> [!NOTE]
> The rpcdce.h header defines RpcBindingInqAuthClient as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo">RpcBindingSetAuthInfo</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>
