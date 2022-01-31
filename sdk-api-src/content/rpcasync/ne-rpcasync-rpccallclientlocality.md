---
UID: NE:rpcasync.tagRpcCallClientLocality
title: RpcCallClientLocality (rpcasync.h)
description: Specifies the set of possible RPC client localities.
helpviewer_keywords: ["RpcCallClientLocality","RpcCallClientLocality enumeration [RPC]","rcclClientUnknownLocality","rcclInvalid","rcclLocal","rcclRemote","rpc.rpccallclientlocality","rpcasync/RpcCallClientLocality","rpcasync/rcclClientUnknownLocality","rpcasync/rcclInvalid","rpcasync/rcclLocal","rpcasync/rcclRemote"]
old-location: rpc\rpccallclientlocality.htm
tech.root: Rpc
ms.assetid: bdb60917-575e-47d1-a5a7-42159aac2d35
ms.date: 12/05/2018
ms.keywords: RpcCallClientLocality, RpcCallClientLocality enumeration [RPC], rcclClientUnknownLocality, rcclInvalid, rcclLocal, rcclRemote, rpc.rpccallclientlocality, rpcasync/RpcCallClientLocality, rpcasync/rcclClientUnknownLocality, rpcasync/rcclInvalid, rpcasync/rcclLocal, rpcasync/rcclRemote
req.header: rpcasync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: RpcCallClientLocality
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRpcCallClientLocality
 - rpcasync/tagRpcCallClientLocality
 - RpcCallClientLocality
 - rpcasync/RpcCallClientLocality
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RpcAsync.h
api_name:
 - RpcCallClientLocality
---

# RpcCallClientLocality enumeration


## -description

The <b>RpcCallClientLocality</b> enumeration specifies the set of possible RPC client localities.

## -enum-fields

### -field rcclInvalid:0

The RPC client locality is invalid.

### -field rcclLocal

The RPC client is local.

### -field rcclRemote

The RPC client is remote.

### -field rcclClientUnknownLocality

The RPC client has an unknown locality.

## -see-also

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a>
