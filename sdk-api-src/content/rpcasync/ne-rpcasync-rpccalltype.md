---
UID: NE:rpcasync.tagRpcCallType
title: RpcCallType (rpcasync.h)
description: Specifies the set of RPC call types.
helpviewer_keywords: ["RpcCallType","RpcCallType enumeration [RPC]","rctGuaranteed","rctInvalid","rctNormal","rctTraining","rpc.rpccalltype","rpcasync/RpcCallType","rpcasync/rctGuaranteed","rpcasync/rctInvalid","rpcasync/rctNormal","rpcasync/rctTraining"]
old-location: rpc\rpccalltype.htm
tech.root: Rpc
ms.assetid: b7b95f51-ced4-423f-88b7-b1ec705af66f
ms.date: 12/05/2018
ms.keywords: RpcCallType, RpcCallType enumeration [RPC], rctGuaranteed, rctInvalid, rctNormal, rctTraining, rpc.rpccalltype, rpcasync/RpcCallType, rpcasync/rctGuaranteed, rpcasync/rctInvalid, rpcasync/rctNormal, rpcasync/rctTraining
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: RpcCallType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRpcCallType
 - rpcasync/tagRpcCallType
 - RpcCallType
 - rpcasync/RpcCallType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RpcCallType
---

# RpcCallType enumeration


## -description

The <b>RpcCallType</b> enumeration specifies the set of RPC call types.

## -enum-fields

### -field rctInvalid:0

The remote procedure call is invalid.

### -field rctNormal

The remote procedure call has no special properties.

### -field rctTraining

The remote procedure call is used for "training" RPC.

### -field rctGuaranteed

The remote procedure call has guaranteed execution.

## -see-also

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a>
