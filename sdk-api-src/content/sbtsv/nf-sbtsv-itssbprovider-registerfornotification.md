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

# ITsSbProvider::RegisterForNotification


## -description


Requests that  Remote Desktop Connection Broker (RD Connection Broker) send notifications about specified events.

Plug-ins can use this method to request notifications about events.


## -parameters




### -param notificationType [in]

The type of notification to receive. To receive notifications for more than one type, specify the enumerations by using a logical <b>OR</b>.



#### TSSB_NOTIFY_TARGET_CHANGE

The owner plug-in has recognized a change in the target's state.



#### TSSB_NOTIFY_SESSION_CHANGE

The owner plug-in has recognized a change in the session's state.



#### TSSB_NOTIFY_CONNECTION_REQUEST_CHANGE

RD Connection Broker has created a connection, or completed a connection request due to a successful logon, time-out, or connection failure.


### -param ResourceToMonitor [in]

This parameter is reserved.


### -param pPluginNotification [in]

A pointer to an <a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a> plug-in notification object that  RD Connection Broker should use for notifications.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>



<a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a>
 

 

