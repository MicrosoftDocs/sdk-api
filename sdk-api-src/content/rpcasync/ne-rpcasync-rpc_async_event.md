---
UID: NE:rpcasync._RPC_ASYNC_EVENT
title: RPC_ASYNC_EVENT (rpcasync.h)
description: The RPC_ASYNC_EVENT enumerated type describes the asynchronous notification events that an RPC application can receive.
helpviewer_keywords: ["RPC_ASYNC_EVENT","RPC_ASYNC_EVENT enumeration [RPC]","RpcCallComplete","RpcClientCancel","RpcClientDisconnect","RpcReceiveComplete","RpcSendComplete","_rpc_rpc_async_event","rpc.rpc_async_event","rpcasync/RPC_ASYNC_EVENT","rpcasync/RpcCallComplete","rpcasync/RpcClientCancel","rpcasync/RpcClientDisconnect","rpcasync/RpcReceiveComplete","rpcasync/RpcSendComplete"]
old-location: rpc\rpc_async_event.htm
tech.root: Rpc
ms.assetid: 6b173ec8-2b58-4a99-87cd-cdf1f92a35ad
ms.date: 12/05/2018
ms.keywords: RPC_ASYNC_EVENT, RPC_ASYNC_EVENT enumeration [RPC], RpcCallComplete, RpcClientCancel, RpcClientDisconnect, RpcReceiveComplete, RpcSendComplete, _rpc_rpc_async_event, rpc.rpc_async_event, rpcasync/RPC_ASYNC_EVENT, rpcasync/RpcCallComplete, rpcasync/RpcClientCancel, rpcasync/RpcClientDisconnect, rpcasync/RpcReceiveComplete, rpcasync/RpcSendComplete
req.header: rpcasync.h
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
req.typenames: RPC_ASYNC_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_ASYNC_EVENT
 - rpcasync/_RPC_ASYNC_EVENT
 - RPC_ASYNC_EVENT
 - rpcasync/RPC_ASYNC_EVENT
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
 - RPC_ASYNC_EVENT
---

# RPC_ASYNC_EVENT enumeration


## -description

The 
<b>RPC_ASYNC_EVENT</b> enumerated type describes the asynchronous notification events that an RPC application can receive.

## -enum-fields

### -field RpcCallComplete

The remote procedure call has completely executed.

### -field RpcSendComplete

The RPC run-time library finished transmitting some of the data provided by the user. A portion, but not necessarily all of the data being sent, has been transmitted. Only applications using DCE pipes will receive this notification.

### -field RpcReceiveComplete

The RPC run-time library finished receiving data. Only applications using DCE pipes will receive this notification.

### -field RpcClientDisconnect

The RPC client has disconnected from the service.

### -field RpcClientCancel

Windows Vista or later: The RPC client has cancelled the asynchronous procedure call.

