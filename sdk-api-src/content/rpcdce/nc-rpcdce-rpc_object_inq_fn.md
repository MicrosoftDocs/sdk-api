---
UID: NC:rpcdce.RPC_OBJECT_INQ_FN
title: RPC_OBJECT_INQ_FN (rpcdce.h)
description: The RPC_OBJECT_INQ_FN function is a prototype for a function that facilitates replacement of the default object UUID to type UUID mapping.
helpviewer_keywords: ["RPC_OBJECT_INQ_FN","RPC_OBJECT_INQ_FN callback","RPC_OBJECT_INQ_FN callback function [RPC]","RpcObjectInqFn","_rpc_rpc_object_inq_fn","rpc.rpc_object_inq_fn","rpcdce/RPC_OBJECT_INQ_FN"]
old-location: rpc\rpc_object_inq_fn.htm
tech.root: Rpc
ms.assetid: 163a5160-1b47-4b65-8f6c-8b009f548ed9
ms.date: 12/05/2018
ms.keywords: RPC_OBJECT_INQ_FN, RPC_OBJECT_INQ_FN callback, RPC_OBJECT_INQ_FN callback function [RPC], RpcObjectInqFn, _rpc_rpc_object_inq_fn, rpc.rpc_object_inq_fn, rpcdce/RPC_OBJECT_INQ_FN
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPC_OBJECT_INQ_FN
 - rpcdce/RPC_OBJECT_INQ_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rpcdce.h
api_name:
 - RPC_OBJECT_INQ_FN
---

# RPC_OBJECT_INQ_FN callback function


## -description

The 
<b>RPC_OBJECT_INQ_FN</b> function is a prototype for a function that facilitates replacement of the default object UUID to type UUID mapping.

## -parameters

### -param ObjectUuid

Pointer to the variable that specifies the object 
<a href="https://msdn.microsoft.com/">UUID</a> that is to be mapped to a type UUID.

### -param TypeUuid

Pointer to the address of the variable that is to contain the type UUID derived from the object UUID. The type UUID is returned by the function.

### -param Status

Pointer to a return value for the function.

## -remarks

You can replace the default mapping function that maps object UUIDs to type UUIDs by calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsetinqfn">RpcObjectSetInqFn</a> and supplying a pointer to a function of type RPC_OBJECT_INQ_FN. The supplied function must match the function prototype specified by the type definition: a function with three parameters and the function return value of void.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcobjectsetinqfn">RpcObjectSetInqFn</a>
