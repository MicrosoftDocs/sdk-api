---
UID: NF:rpcdce.RpcBindingSetObject
title: RpcBindingSetObject function (rpcdce.h)
description: The RpcBindingSetObject function sets the object UUID value in a binding handle.
helpviewer_keywords: ["RpcBindingSetObject","RpcBindingSetObject function [RPC]","_rpc_rpcbindingsetobject","rpc.rpcbindingsetobject","rpcdce/RpcBindingSetObject"]
old-location: rpc\rpcbindingsetobject.htm
tech.root: Rpc
ms.assetid: 5dcf341f-e392-4608-b741-8fa07cabd50b
ms.date: 12/05/2018
ms.keywords: RpcBindingSetObject, RpcBindingSetObject function [RPC], _rpc_rpcbindingsetobject, rpc.rpcbindingsetobject, rpcdce/RpcBindingSetObject
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
 - RpcBindingSetObject
 - rpcdce/RpcBindingSetObject
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
 - RpcBindingSetObject
---

# RpcBindingSetObject function


## -description

The 
<b>RpcBindingSetObject</b> function sets the object UUID value in a binding handle.

## -parameters

### -param Binding

Server binding into which the <i>ObjectUuid</i> is set.

### -param ObjectUuid

Pointer to the 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> of the object serviced by the server specified in the <i>Binding</i> parameter. <i>ObjectUuid</i> is a unique identifier of an object to which a remote procedure call can be made.

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

An application calls the 
<b>RpcBindingSetObject</b> function to associate an object 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> with a server binding handle. The set-object operation replaces the previously associated object UUID with the UUID in the <i>ObjectUuid</i> parameter.

To set the object 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to the nil UUID, specify a null value or the nil UUID for the <i>ObjectUuid</i> parameter.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding">RpcBindingFromStringBinding</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqobject">RpcBindingInqObject</a>