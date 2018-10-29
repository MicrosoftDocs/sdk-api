---
UID: NF:rpcasync.RpcServerSubscribeForNotification
title: RpcServerSubscribeForNotification function
author: windows-sdk-content
description: Subscribes the server for RPC notifications.
old-location: rpc\rpcserversubscribefornotification.htm
tech.root: Rpc
ms.assetid: 544b1e57-7b3c-474d-8b89-d6c62f54b2c2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcServerSubscribeForNotification, RpcServerSubscribeForNotification function [RPC], rpc.rpcserversubscribefornotification, rpcasync/RpcServerSubscribeForNotification
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerSubscribeForNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerSubscribeForNotification function


## -description


The <b>RpcServerSubscribeForNotification</b> function subscribes the server for RPC notifications.


## -parameters




### -param Binding [in]


<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a> structure that contains the binding handle for the current call. If this function is called on the same thread that RPC has dispatched a call on, this parameter can be set to <b>NULL</b>; otherwise, an explicit binding handle must be passed in this parameter.


### -param Notification [in]

Bitwise combination of the <a href="https://msdn.microsoft.com/d5074917-837c-4f3c-a582-97f488ed4919">RPC_NOTIFICATIONS</a> enumeration values that specifies the type of notification requested from RPC by the server.

<b>Windows Vista:  </b>Currently, only <b>RpcNotificationClientDisconnect</b> and <b>RpcNotificationCallCancel</b> are supported. If any other value is specified for this parameter, the RPC_S_CANNOT_SUPPORT error code is returned.


### -param NotificationType [in]


<a href="https://msdn.microsoft.com/3c6fcba5-ea74-47ee-8fb9-6393d1ea62fc">RPC_NOTIFICATION_TYPES</a> enumeration value that specifies the method by which RPC will notify the server.

<b>Windows Vista:  </b><b>RpcNotificationTypeNone</b> is not supported. If this value is specified, the RPC_S_INVALID_ARG error code is returned.


### -param NotificationInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/253f3d23-4cc2-44b3-9d25-c7f26d73ed1e">RPC_ASYNC_NOTIFICATION_INFO</a> union that contains the specific information necessary for RPC to contact the server for notification. The data contained in this union is specific to the method passed to the <i>NotificationType</i> parameter. 

If the <b>RpcNotificationTypeCallback</b> method is specified in <i>NotificationTypes</i>, the <b>NotificationRoutine</b> member of the corresponding branch of the union is set to the binding handle for synchronous calls and the async handle for asynchronous calls.

RPC makes a copy of this parameter during a successful call to this function. The caller can free or update this parameter when the API returns.


## -returns



This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



If the caller specifies any notification type other than <b>RpcNotificationTypeEvent</b>, it can subscribe to both the <b>RpcNotificationClientDisconnect</b> and <b>RpcNotificationCallCancel</b> notifications with a single call. For events, two separate calls to this API are required.

The server application must unsubscribe for notification before the RPC call is completed. If the RPC call is synchronous, it is completed when the server sends a return value to RPC. If the RPC call is asynchronous, it is completed  when the server calls <a href="https://msdn.microsoft.com/76b6bc3a-f5d1-4780-8071-9b221a6fd7d8">RpcAsyncCompleteCall</a> or <a href="https://msdn.microsoft.com/651c53f3-8bb5-4162-a8a8-2da5a0d05d21">RpcAsyncAbortCall</a>, or throws an exeception from the manager routine. If the server fails to unsubscribe for call status change notifications, the results are undefined, and the server may crash at a later time. Note that the subscription applies for one RPC call only. If the server application needs to monitor more than one call, it needs to subscribe for each call specifically.

The server application can expect that it will not be signaled for notifications that it hasn't subscribed for. If it has subscribed for more than one notification, each notification is communicated to the completion method if the selected completion method permits it. If it doesn't permit the communication of notifications, the server application can call on of the RPC server APIs to test whether or not the client has canceled or disconnected. The table below indicates how notification type (call cancel or client disconnect) is communicated to each notification method: 


<table>
<tr>
<th>Notification Method</th>
<th>Event/Notification Type</th>
</tr>
<tr>
<td>RpcNotificationTypeNone</td>
<td>Not allowed for subscription.</td>
</tr>
<tr>
<td>RpcNotificationTypeEvent</td>
<td>The notification type is not available.</td>
</tr>
<tr>
<td>RpcNotificationTypeApc</td>
<td>The notification type is found in the <i>Event</i> parameter of the APC function.</td>
</tr>
<tr>
<td>RpcNotificationTypeIoc</td>
<td>The notification type is not available.</td>
</tr>
<tr>
<td>RpcNotificationTypeCallback</td>
<td>The notification type is found in the <i>Event</i> parameter of the callback function.</td>
</tr>
</table>
 



Note that the table does not imply whether or not a caller can subscribe for notifications using the given notification method; rather, it simply states  the information the caller can obtain when the notification is received, such as the notification type.

The caller must synchronize between <b>RpcServerSubscribeForNotification</b> and <a href="https://msdn.microsoft.com/7ca59f00-41ac-4771-a465-6185e17abe80">RpcServerUnsubscribeForNotification</a> on the same binding handle. If they are called simultaneously, the results are undefined and could incur lost notifications, extra notifications, an incorrect notification count, process crashes, data corruption, and memory leaks. The same concern applies for threads calling <b>RpcServerSubscribeForNotification</b> on the same binding handle.

Calling <b>RpcServerSubscribeForNotification</b> and <a href="https://msdn.microsoft.com/7ca59f00-41ac-4771-a465-6185e17abe80">RpcServerUnsubscribeForNotification</a> on the same binding handle is thread safe. For current notifications, RPC  will notify the server no more than once per call.




## -see-also




<a href="https://msdn.microsoft.com/7ca59f00-41ac-4771-a465-6185e17abe80">RpcServerUnsubscribeForNotification</a>
 

 

