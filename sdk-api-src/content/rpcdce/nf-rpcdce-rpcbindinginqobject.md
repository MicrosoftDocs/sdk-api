---
UID: NF:rpcdce.RpcBindingInqObject
title: RpcBindingInqObject function (rpcdce.h)
description: The RpcBindingInqObject function returns the object UUID from a binding handle.
helpviewer_keywords: ["RpcBindingInqObject","RpcBindingInqObject function [RPC]","_rpc_rpcbindinginqobject","rpc.rpcbindinginqobject","rpcdce/RpcBindingInqObject"]
old-location: rpc\rpcbindinginqobject.htm
tech.root: Rpc
ms.assetid: e2d489f9-d976-4dc3-8a91-dfc04f547165
ms.date: 12/05/2018
ms.keywords: RpcBindingInqObject, RpcBindingInqObject function [RPC], _rpc_rpcbindinginqobject, rpc.rpcbindinginqobject, rpcdce/RpcBindingInqObject
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
 - RpcBindingInqObject
 - rpcdce/RpcBindingInqObject
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
 - RpcBindingInqObject
---

# RpcBindingInqObject function


## -description

The 
<b>RpcBindingInqObject</b> function returns the object UUID from a binding handle.

## -parameters

### -param Binding

Client or server binding handle.

### -param ObjectUuid

Returns a pointer to the object 
<a href="https://msdn.microsoft.com/">UUID</a> found in the <i>Binding</i> parameter. <i>ObjectUuid</i> is a unique identifier of an object to which a remote procedure call can be made.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls the 
<b>RpcBindingInqObject</b> function to see the object 
<a href="https://msdn.microsoft.com/">UUID</a> associated with a client or server binding handle.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetobject">RpcBindingSetObject</a>