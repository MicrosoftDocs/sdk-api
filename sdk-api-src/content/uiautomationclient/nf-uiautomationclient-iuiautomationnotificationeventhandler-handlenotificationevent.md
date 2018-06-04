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

# IUIAutomationNotificationEventHandler::HandleNotificationEvent


## -description


Handles a Microsoft UI Automation notification event.


## -parameters




### -param sender [in]

A pointer to the element that raised the event.


### -param notificationKind

The type of notification.


### -param notificationProcessing

Indicates how to process notifications.


### -param displayString

A string to display in the notification message.


### -param activityId

A unique non-localized string to identify an action or group of actions. This is used to pass additional information to the event handler.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by calling <a href="https://msdn.microsoft.com/1E6A4683-9439-4212-9EA6-91719A515C4B">AddNotificationEventHandler</a>.




## -see-also




<a href="https://msdn.microsoft.com/7E12B8C2-D6A7-4637-9049-312B78EC01DE">IUIAutomationNotificationEventHandler</a>
 

 

