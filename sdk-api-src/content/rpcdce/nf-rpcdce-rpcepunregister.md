---
UID: NF:rpcdce.RpcEpUnregister
title: RpcEpUnregister function (rpcdce.h)
description: The RpcEpUnregister function removes server-address information from the local endpoint-map database.
helpviewer_keywords: ["RpcEpUnregister","RpcEpUnregister function [RPC]","_rpc_rpcepunregister","rpc.rpcepunregister","rpcdce/RpcEpUnregister"]
old-location: rpc\rpcepunregister.htm
tech.root: Rpc
ms.assetid: bb0485fc-0b25-4fc0-9a18-921a9de428ce
ms.date: 12/05/2018
ms.keywords: RpcEpUnregister, RpcEpUnregister function [RPC], _rpc_rpcepunregister, rpc.rpcepunregister, rpcdce/RpcEpUnregister
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
 - RpcEpUnregister
 - rpcdce/RpcEpUnregister
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
 - RpcEpUnregister
---

# RpcEpUnregister function


## -description

The 
<b>RpcEpUnregister</b> function removes server-address information from the local endpoint-map database.

## -parameters

### -param IfSpec

Interface to unregister from the local endpoint-map database.

### -param BindingVector

Pointer to a vector of binding handles to unregister.

### -param UuidVector

Pointer to an optional vector of object UUIDs to unregister. The server application constructs this vector. 
<b>RpcEpUnregister</b> unregisters all endpoint-map database elements that match the specified <i>IfSpec</i> and <i>BindingVector</i> parameters and the object UUID(s). 




A null parameter value indicates there are no object UUIDs to unregister.

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
<dt><b>RPC_S_NO_BINDINGS</b></dt>
</dl>
</td>
<td width="60%">
No bindings.

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

The 
<b>RpcEpUnregister</b> function removes elements from the local host's endpoint-map database. A server application calls this function only when the server has previously registered endpoints and the server wants to remove that address information from the endpoint-map database.

Specifically, 
<b>RpcEpUnregister</b> allows a server application to remove its own endpoint-map database elements (server-address information) based on the interface specification or on both the interface specification and the object UUID(s) of the resource(s) offered.

The server calls the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a> function to obtain the required <i>BindingVector</i> parameter. To unregister selected endpoints, the server can prune the binding vector prior to calling this function.

<b>RpcEpUnregister</b> creates a cross-product from the <i>IfSpec</i>, <i>BindingVector</i>, and <i>UuidVector</i> parameters and removes each element in the cross-product from the endpoint-map database.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>