---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _RPC_NOTIFICATIONS enumeration


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
 

 

