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

# _RPC_ASYNC_EVENT enumeration


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

