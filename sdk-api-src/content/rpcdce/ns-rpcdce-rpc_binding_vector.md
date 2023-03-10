---
UID: NS:rpcdce._RPC_BINDING_VECTOR
title: RPC_BINDING_VECTOR (rpcdce.h)
description: The RPC_BINDING_VECTOR structure contains a list of binding handles over which a server application can receive remote procedure calls.
helpviewer_keywords: ["RPC_BINDING_VECTOR","RPC_BINDING_VECTOR structure [RPC]","_rpc_rpc_binding_vector","rpc.rpc_binding_vector","rpcdce/RPC_BINDING_VECTOR"]
old-location: rpc\rpc_binding_vector.htm
tech.root: Rpc
ms.assetid: 16a0a595-ed4f-4871-a1a3-268c6bed0305
ms.date: 12/05/2018
ms.keywords: RPC_BINDING_VECTOR, RPC_BINDING_VECTOR structure [RPC], _rpc_rpc_binding_vector, rpc.rpc_binding_vector, rpcdce/RPC_BINDING_VECTOR
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_BINDING_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_BINDING_VECTOR
 - rpcdce/_RPC_BINDING_VECTOR
 - RPC_BINDING_VECTOR
 - rpcdce/RPC_BINDING_VECTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_BINDING_VECTOR
---

# RPC_BINDING_VECTOR structure


## -description

The 
<b>RPC_BINDING_VECTOR</b> structure contains a list of binding handles over which a server application can receive remote procedure calls.

## -struct-fields

### -field Count

Number of binding handles present in the binding-handle array <b>BindingH</b>.

### -field BindingH

Array of binding handles that contains <b>Count</b> elements.

## -remarks

The binding vector contains a count member (<b>Count</b>), followed by an array of binding-handle (<b>BindingH</b>) elements.

The RPC run-time library creates binding handles when a server application registers protocol sequences. To obtain a binding vector, a server application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>.

A client application obtains a binding vector of compatible servers from the name-service database by calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>.

In both routines, the RPC run-time library allocates memory for the binding vector. An application calls 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a> to free the binding vector.

To remove an individual binding handle from the vector, the application must set the value in the vector to <b>NULL</b>. When setting a vector element to <b>NULL</b>, the application must:

<ul>
<li>Free the individual binding.</li>
<li>Not change the value of <b>Count</b>.</li>
</ul>
Calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfree">RpcBindingFree</a> allows an application to free all binding handles in the vector.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingvectorfree">RpcBindingVectorFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext">RpcNsBindingLookupNext</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingselect">RpcNsBindingSelect</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinqbindings">RpcServerInqBindings</a>