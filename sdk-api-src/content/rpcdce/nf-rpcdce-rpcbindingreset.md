---
UID: NF:rpcdce.RpcBindingReset
title: RpcBindingReset function (rpcdce.h)
description: The RpcBindingReset function resets a binding handle so that the host is specified but the server on that host is unspecified.
helpviewer_keywords: ["RpcBindingReset","RpcBindingReset function [RPC]","_rpc_rpcbindingreset","rpc.rpcbindingreset","rpcdce/RpcBindingReset"]
old-location: rpc\rpcbindingreset.htm
tech.root: Rpc
ms.assetid: 2f7a447a-50b1-422e-a49a-00ede3fcf187
ms.date: 12/05/2018
ms.keywords: RpcBindingReset, RpcBindingReset function [RPC], _rpc_rpcbindingreset, rpc.rpcbindingreset, rpcdce/RpcBindingReset
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - RpcBindingReset
 - rpcdce/RpcBindingReset
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
 - RpcBindingReset
---

# RpcBindingReset function


## -description

The 
<b>RpcBindingReset</b> function resets a binding handle so that the host is specified but the server on that host is unspecified.

## -parameters

### -param Binding

Server binding handle to reset.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

A client calls the 
<b>RpcBindingReset</b> function to disassociate a particular server instance from the server binding handle specified in the <i>Binding</i> parameter. The 
<b>RpcBindingReset</b> function dissociates a server instance by removing the endpoint portion of the server address in the binding handle. The host remains unchanged in the binding handle. The result is a partially-bound server binding handle.

<b>RpcBindingReset</b> does not affect the <i>Binding</i> parameter's authentication information, if there is any.

If a client is willing to be serviced by any compatible server instance on the host specified in the binding handle, the client calls the 
<b>RpcBindingReset</b> function before making a remote procedure call using the <i>Binding</i> binding handle. Clients must not call the 
<b>RpcBindingReset</b> function for binding handles on which calls are being executed.

When the client makes the next remote procedure call using the reset (partially-bound) binding, the client's RPC run-time library uses a well-known endpoint from the client's interface specification, if any. Otherwise, the client's run-time library automatically communicates with the endpoint-mapping service on the specified remote host to obtain the endpoint of a compatible server from the endpoint-map database. If a compatible server is located, the RPC run-time library updates the binding with a new endpoint. If a compatible server is not found, the remote procedure call fails. For calls using a connection protocol (ncacn), the EPT_S_NOT_REGISTERED status code is returned to the client. For calls using a datagram protocol (ncadg), the RPC_S_COMM_FAILURE status code is returned to the client.

Server applications should register all binding handles by calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a> and 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a> if the server wants to be available to clients that make a remote procedure call on a reset binding handle.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>