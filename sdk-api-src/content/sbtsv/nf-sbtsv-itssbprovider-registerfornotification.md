---
UID: NF:sbtsv.ITsSbProvider.RegisterForNotification
title: ITsSbProvider::RegisterForNotification
author: windows-sdk-content
description: Requests that Remote Desktop Connection Broker (RD Connection Broker) send notifications about specified events.
old-location: termserv\itssbprovider_registerfornotification.htm
tech.root: TermServ
ms.assetid: 71e55a94-7e15-45f1-a1f3-d3cf8814e0c1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ITsSbProvider interface [Remote Desktop Services],RegisterForNotification method, ITsSbProvider.RegisterForNotification, ITsSbProvider::RegisterForNotification, RegisterForNotification, RegisterForNotification method [Remote Desktop Services], RegisterForNotification method [Remote Desktop Services],ITsSbProvider interface, TSSB_NOTIFY_CONNECTION_REQUEST_CHANGE, TSSB_NOTIFY_SESSION_CHANGE, TSSB_NOTIFY_TARGET_CHANGE, sbtsv/ITsSbProvider::RegisterForNotification, termserv.itssbprovider_registerfornotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.RegisterForNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

