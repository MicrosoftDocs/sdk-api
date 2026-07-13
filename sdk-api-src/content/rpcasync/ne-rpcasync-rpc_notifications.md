---
UID: NE:rpcasync._RPC_NOTIFICATIONS
title: RPC_NOTIFICATIONS (rpcasync.h)
description: The RPC_NOTIFICATIONS enumeration specifies the notifications a server can receive from RPC.
helpviewer_keywords: ["RPC_NOTIFICATIONS","RPC_NOTIFICATIONS enumeration [RPC]","RpcNotificationCallCancel","RpcNotificationCallNone","RpcNotificationClientDisconnect","rpc.rpc_notifications","rpcasync/RPC_NOTIFICATIONS","rpcasync/RpcNotificationCallCancel","rpcasync/RpcNotificationCallNone","rpcasync/RpcNotificationClientDisconnect"]
old-location: rpc\rpc_notifications.htm
tech.root: Rpc
ms.assetid: d5074917-837c-4f3c-a582-97f488ed4919
ms.date: 12/05/2018
ms.keywords: RPC_NOTIFICATIONS, RPC_NOTIFICATIONS enumeration [RPC], RpcNotificationCallCancel, RpcNotificationCallNone, RpcNotificationClientDisconnect, rpc.rpc_notifications, rpcasync/RPC_NOTIFICATIONS, rpcasync/RpcNotificationCallCancel, rpcasync/RpcNotificationCallNone, rpcasync/RpcNotificationClientDisconnect
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
req.typenames: RPC_NOTIFICATIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_NOTIFICATIONS
 - rpcasync/_RPC_NOTIFICATIONS
 - RPC_NOTIFICATIONS
 - rpcasync/RPC_NOTIFICATIONS
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
 - RPC_NOTIFICATIONS
---

# RPC_NOTIFICATIONS enumeration


## -description

The <b>RPC_NOTIFICATIONS</b> enumeration specifies the notifications a server can receive from RPC.

## -enum-fields

### -field RpcNotificationCallNone:0

Do not send a notification.

<b>Windows Vista:  </b>Currently, this value is not supported for <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserversubscribefornotification">RpcServerSubscribeForNotification</a> and <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverunsubscribefornotification">RpcServerUnsubscribeForNotification</a>.

### -field RpcNotificationClientDisconnect:1

The client has disconnected.

### -field RpcNotificationCallCancel:2      

The RPC call has been canceled.

## -see-also

<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserversubscribefornotification">RpcServerSubscribeForNotification</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverunsubscribefornotification">RpcServerUnsubscribeForNotification</a>
