---
UID: NF:rpcdce.RpcBindingServerFromClient
title: RpcBindingServerFromClient function (rpcdce.h)
description: An application calls RpcBindingServerFromClient to convert a client binding handle into a partially-bound server binding handle.
helpviewer_keywords: ["RpcBindingServerFromClient","RpcBindingServerFromClient function [RPC]","_rpc_rpcbindingserverfromclient","rpc.rpcbindingserverfromclient","rpcdce/RpcBindingServerFromClient"]
old-location: rpc\rpcbindingserverfromclient.htm
tech.root: Rpc
ms.assetid: 9fdcdb99-be6c-4a3b-97dd-8d0eadd2754d
ms.date: 12/05/2018
ms.keywords: RpcBindingServerFromClient, RpcBindingServerFromClient function [RPC], _rpc_rpcbindingserverfromclient, rpc.rpcbindingserverfromclient, rpcdce/RpcBindingServerFromClient
req.header: rpcdce.h
req.include-header: Rpc.h
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcBindingServerFromClient
 - rpcdce/RpcBindingServerFromClient
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
 - RpcBindingServerFromClient
---

# RpcBindingServerFromClient function


## -description

An application calls 
<b>RpcBindingServerFromClient</b> to convert a client binding handle into a partially-bound server binding handle.

## -parameters

### -param ClientBinding

Client binding handle to convert to a server binding handle. If a value of zero is specified, the server impersonates the client that is being served by this server thread.

<div class="alert"><b>Note</b>  This parameter cannot be <b>NULL</b> in Windows NT 4.0.</div>
<div> </div>

### -param ServerBinding

Returns a server binding handle.

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
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Cannot determine the client's host. See Remarks for a list of supported protocol sequences.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The following protocol sequences support 
<b>RpcBindingServerFromClient</b>:

<ul>
<li>
<a href="/windows/desktop/Midl/ncadg-ip-udp">ncadg_ip_udp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/">ncadg_ipx</a>
</li>
<li>
<a href="/windows/desktop/Midl/ncacn-ip-tcp">ncacn_ip_tcp</a>
</li>
<li>
<a href="/windows/desktop/Midl/ncacn-spx">ncacn_spx</a>.</li>
<li>
<a href="/windows/desktop/Midl/ncacn-np">ncacn_np</a> (effective with Windows 2000)</li>
<li>
<a href="https://msdn.microsoft.com/">ncacn_http</a>
</li>
<li>ncalrpc</li>
</ul>
An application gets a client binding handle from the RPC run-time. When the remote procedure call arrives at a server, the run-time creates a client binding handle that contains information about the calling client. The run-time passes this handle to the server manager function as the first argument.

Calling 
<b>RpcBindingServerFromClient</b> converts this client handle to a server handle that has these properties:

<ul>
<li>The server handle is a partially-bound handle. It contains a network address for the calling client, but lacks an endpoint.</li>
<li>The server handle contains the same object 
<a href="https://msdn.microsoft.com/">UUID</a> used by the calling client. This can be the nil UUID. For more information on how a client specifies an object UUID for a call, see 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingsetObject</a>, 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a>, 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>, and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>.</li>
<li>The server handle contains no authentication information.</li>
</ul>
The server application must call 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a> to free the resources used by the server binding handle once it is no longer needed.

<div class="alert"><b>Note</b>  To query a client's address, an application starts by calling the RpcBindingServerFromClient function to obtain a partially bound server binding handle.  The server binding handle can be used to obtain a string binding by invoking RpcBindingToStringBinding.  The server can then call RpcStringBindingParse to extract the client's network address from the string binding.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingSetObject</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina">RpcNsBindingLookupBegin</a>