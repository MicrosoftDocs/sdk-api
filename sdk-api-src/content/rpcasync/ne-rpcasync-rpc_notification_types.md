---
UID: NE:rpcasync._RPC_NOTIFICATION_TYPES
title: RPC_NOTIFICATION_TYPES (rpcasync.h)
description: The RPC_NOTIFICATION_TYPES enumerated type contains values that specify the method of asynchronous notification that a client program will use.
helpviewer_keywords: ["RPC_NOTIFICATION_TYPES","RPC_NOTIFICATION_TYPES enumeration [RPC]","RpcNotificationTypeApc","RpcNotificationTypeCallback","RpcNotificationTypeEvent","RpcNotificationTypeHwnd","RpcNotificationTypeIoc","RpcNotificationTypeNone","_rpc_rpc_notification_types","rpc.rpc_notification_types","rpcasync/RPC_NOTIFICATION_TYPES","rpcasync/RpcNotificationTypeApc","rpcasync/RpcNotificationTypeCallback","rpcasync/RpcNotificationTypeEvent","rpcasync/RpcNotificationTypeHwnd","rpcasync/RpcNotificationTypeIoc","rpcasync/RpcNotificationTypeNone"]
old-location: rpc\rpc_notification_types.htm
tech.root: Rpc
ms.assetid: 3c6fcba5-ea74-47ee-8fb9-6393d1ea62fc
ms.date: 12/05/2018
ms.keywords: RPC_NOTIFICATION_TYPES, RPC_NOTIFICATION_TYPES enumeration [RPC], RpcNotificationTypeApc, RpcNotificationTypeCallback, RpcNotificationTypeEvent, RpcNotificationTypeHwnd, RpcNotificationTypeIoc, RpcNotificationTypeNone, _rpc_rpc_notification_types, rpc.rpc_notification_types, rpcasync/RPC_NOTIFICATION_TYPES, rpcasync/RpcNotificationTypeApc, rpcasync/RpcNotificationTypeCallback, rpcasync/RpcNotificationTypeEvent, rpcasync/RpcNotificationTypeHwnd, rpcasync/RpcNotificationTypeIoc, rpcasync/RpcNotificationTypeNone
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
req.typenames: RPC_NOTIFICATION_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_NOTIFICATION_TYPES
 - rpcasync/_RPC_NOTIFICATION_TYPES
 - RPC_NOTIFICATION_TYPES
 - rpcasync/RPC_NOTIFICATION_TYPES
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
 - RPC_NOTIFICATION_TYPES
---

# RPC_NOTIFICATION_TYPES enumeration


## -description

The 
<b>RPC_NOTIFICATION_TYPES</b> enumerated type contains values that specify the method of asynchronous notification that a client program will use.

## -enum-fields

### -field RpcNotificationTypeNone

The client does not require notification of the completion of an asynchronous remote procedure call.

### -field RpcNotificationTypeEvent

Notify the client program by signaling an event object. See 
<a href="/windows/desktop/Sync/event-objects">Event Objects</a>.

### -field RpcNotificationTypeApc

Use an asynchronous procedure call to notify the client that the remote procedure call is complete.

### -field RpcNotificationTypeIoc

Send the asynchronous RPC notification to the client through an I/O completion port.

### -field RpcNotificationTypeHwnd

Post a notification message to the specified window handle.

### -field RpcNotificationTypeCallback

Invoke a callback function provided by the client program.

## -see-also

<a href="/windows/desktop/Rpc/making-the-asynchronous-call">Making the Asynchronous Call</a>