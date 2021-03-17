---
UID: NF:rpcasync.RpcServerUnsubscribeForNotification
title: RpcServerUnsubscribeForNotification function (rpcasync.h)
description: Unsubscribes the server from RPC notifications.
helpviewer_keywords: ["RpcServerUnsubscribeForNotification","RpcServerUnsubscribeForNotification function [RPC]","rpc.rpcserverunsubscribefornotification","rpcasync/RpcServerUnsubscribeForNotification"]
old-location: rpc\rpcserverunsubscribefornotification.htm
tech.root: Rpc
ms.assetid: 7ca59f00-41ac-4771-a465-6185e17abe80
ms.date: 12/05/2018
ms.keywords: RpcServerUnsubscribeForNotification, RpcServerUnsubscribeForNotification function [RPC], rpc.rpcserverunsubscribefornotification, rpcasync/RpcServerUnsubscribeForNotification
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcServerUnsubscribeForNotification
 - rpcasync/RpcServerUnsubscribeForNotification
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
 - RpcServerUnsubscribeForNotification
---

# RpcServerUnsubscribeForNotification function


## -description

The <b>RpcServerUnsubscribeForNotification</b> function unsubscribes the server from RPC notifications.

## -parameters

### -param Binding [in]

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a> structure that contains the binding handle for the current RPC call specified in a previous call to <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserversubscribefornotification">RpcServerSubscribeForNotification</a>. If this function is called on the same thread that RPC has dispatched a call on, this parameter can be set to <b>NULL</b>; otherwise, an explicit binding handle must be passed in this parameter.

### -param Notification [in]

A value from the <a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpc_notifications">RPC_NOTIFICATIONS</a> enumeration that specifies the type of notification requested from RPC by the server.  Notifications must be unsubscribed individually, multiple values are not supported.

<b>Windows Vista:  </b>Currently, only <b>RpcNotificationClientDisconnect</b> and <b>RpcNotificationCallCancel</b> are supported. If any other value is specified for this parameter, the RPC_S_CANNOT_SUPPORT error code is returned.

### -param NotificationsQueued [out]

A required pointer to a value that receives the number of notifications that the RPC runtime queued for the specified RPC call. The pointer must be supplied; it is not optional.

Your code should keep track of the number of notifications that it receives. When you unsubscribe from RPC notifications, you should check if the number of notifications that the RPC runtime queued matches the number of notifications that you received. If the numbers do not match, some notifications could still be incoming on another thread.  You should delay cleaning up the notification state until you receive all incoming notifications.

## -returns

This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

<b>RpcServerUnsubscribeForNotification</b> must be called for every RPC binding handle that has also had <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserversubscribefornotification">RpcServerSubscribeForNotification</a> called on it for the associated RPC call. This API must be called before the associated RPC call is completed; otherwise, the results are undefined and could lead to application instability.

Unretrieved notifications may be retrieved after this API returns.

## -see-also

<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserversubscribefornotification">RpcServerSubscribeForNotification</a>