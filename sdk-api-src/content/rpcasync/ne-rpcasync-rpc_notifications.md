---
UID: NE:rpcasync._RPC_NOTIFICATIONS
title: RPC_NOTIFICATIONS (rpcasync.h)
author: windows-sdk-content
description: The RPC_NOTIFICATIONS enumeration specifies the notifications a server can receive from RPC.
old-location: rpc\rpc_notifications.htm
tech.root: Rpc
ms.assetid: d5074917-837c-4f3c-a582-97f488ed4919
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RPC_NOTIFICATIONS, RPC_NOTIFICATIONS enumeration [RPC], RpcNotificationCallCancel, RpcNotificationCallNone, RpcNotificationClientDisconnect, rpc.rpc_notifications, rpcasync/RPC_NOTIFICATIONS, rpcasync/RpcNotificationCallCancel, rpcasync/RpcNotificationCallNone, rpcasync/RpcNotificationClientDisconnect
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_NOTIFICATIONS
product: Windows
targetos: Windows
req.typenames: RPC_NOTIFICATIONS
req.redist: 
---

# RPC_NOTIFICATIONS enumeration


## -description


The <b>RPC_NOTIFICATIONS</b> enumeration specifies the notifications a server can receive from RPC.


## -enum-fields




### -field RpcNotificationCallNone

Do not send a notification.

<b>Windows Vista:  </b>Currently, this value is not supported for <a href="https://msdn.microsoft.com/544b1e57-7b3c-474d-8b89-d6c62f54b2c2">RpcServerSubscribeForNotification</a> and <a href="https://msdn.microsoft.com/7ca59f00-41ac-4771-a465-6185e17abe80">RpcServerUnsubscribeForNotification</a>.


### -field RpcNotificationClientDisconnect

The client has disconnected.


### -field RpcNotificationCallCancel

The RPC call has been canceled.


## -see-also




<a href="https://msdn.microsoft.com/544b1e57-7b3c-474d-8b89-d6c62f54b2c2">RpcServerSubscribeForNotification</a>



<a href="https://msdn.microsoft.com/7ca59f00-41ac-4771-a465-6185e17abe80">RpcServerUnsubscribeForNotification</a>
 

 

