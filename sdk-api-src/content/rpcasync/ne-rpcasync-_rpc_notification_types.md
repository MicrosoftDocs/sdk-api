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

# _RPC_NOTIFICATION_TYPES enumeration


## -description


The 
<b>RPC_NOTIFICATION_TYPES</b> enumerated type contains values that specify the method of asynchronous notification that a client program will use.


## -enum-fields




### -field RpcNotificationTypeNone

The client does not require notification of the completion of an asynchronous remote procedure call.


### -field RpcNotificationTypeEvent

Notify the client program by signaling an event object. See 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544323">Event Objects</a>.


### -field RpcNotificationTypeApc

Use an asynchronous procedure call to notify the client that the remote procedure call is complete.


### -field RpcNotificationTypeIoc

Send the asynchronous RPC notification to the client through an I/O completion port.


### -field RpcNotificationTypeHwnd

Post a notification message to the specified window handle.


### -field RpcNotificationTypeCallback

Invoke a callback function provided by the client program.


## -see-also




<a href="https://msdn.microsoft.com/b40308ef-88ae-4c80-9118-29c5ffee77ad">Making the Asynchronous Call</a>
 

 

