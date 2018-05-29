---
UID: NF:rpcasync.RpcServerUnsubscribeForNotification
title: RpcServerUnsubscribeForNotification function
author: windows-sdk-content
description: Unsubscribes the server from RPC notifications.
old-location: rpc\rpcserverunsubscribefornotification.htm
old-project: Rpc
ms.assetid: 7ca59f00-41ac-4771-a465-6185e17abe80
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: RpcServerUnsubscribeForNotification, RpcServerUnsubscribeForNotification function [RPC], rpc.rpcserverunsubscribefornotification, rpcasync/RpcServerUnsubscribeForNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcServerUnsubscribeForNotification
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcServerUnsubscribeForNotification function


## -description


The <b>RpcServerUnsubscribeForNotification</b> function unsubscribes the server from RPC notifications.


## -parameters




### -param Binding [in]


<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a> structure that contains the binding handle for the current RPC call specified in a previous call to <a href="https://msdn.microsoft.com/544b1e57-7b3c-474d-8b89-d6c62f54b2c2">RpcServerSubscribeForNotification</a>. If this function is called on the same thread that RPC has dispatched a call on, this parameter can be set to <b>NULL</b>; otherwise, an explicit binding handle must be passed in this parameter.


### -param Notification [in]

A value from the <a href="https://msdn.microsoft.com/d5074917-837c-4f3c-a582-97f488ed4919">RPC_NOTIFICATIONS</a> enumeration that specifies the type of notification requested from RPC by the server.  Notifications must be unsubscribed individually, multiple values are not supported.

<b>Windows Vista:  </b>Currently, only <b>RpcNotificationClientDisconnect</b> and <b>RpcNotificationCallCancel</b> are supported. If any other value is specified for this parameter, the RPC_S_CANNOT_SUPPORT error code is returned.


### -param NotificationsQueued [out]

A required pointer to a value that receives the number of notifications that the RPC runtime queued for the specified RPC call. The pointer must be supplied; it is not optional.

Your code should keep track of the number of notifications that it receives. When you unsubscribe from RPC notifications, you should check if the number of notifications that the RPC runtime queued matches the number of notifications that you received. If the numbers do not match, some notifications could still be incoming on another thread.  You should delay cleaning up the notification state until you receive all incoming notifications. 


## -returns



This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcServerUnsubscribeForNotification</b> must be called for every RPC binding handle that has also had <a href="https://msdn.microsoft.com/544b1e57-7b3c-474d-8b89-d6c62f54b2c2">RpcServerSubscribeForNotification</a> called on it for the associated RPC call. This API must be called before the associated RPC call is completed; otherwise, the results are undefined and could lead to application instability.

Unretrieved notifications may be retrieved after this API returns.




## -see-also




<a href="https://msdn.microsoft.com/544b1e57-7b3c-474d-8b89-d6c62f54b2c2">RpcServerSubscribeForNotification</a>
 

 

