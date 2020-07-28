---
UID: NF:uiautomationclient.IUIAutomationNotificationEventHandler.HandleNotificationEvent
title: IUIAutomationNotificationEventHandler::HandleNotificationEvent (uiautomationclient.h)
description: Handles a Microsoft UI Automation notification event.
helpviewer_keywords: ["HandleNotificationEvent","HandleNotificationEvent method [Windows Accessibility]","HandleNotificationEvent method [Windows Accessibility]","IUIAutomationNotificationEventHandler interface","IUIAutomationNotificationEventHandler interface [Windows Accessibility]","HandleNotificationEvent method","IUIAutomationNotificationEventHandler.HandleNotificationEvent","IUIAutomationNotificationEventHandler::HandleNotificationEvent","uiautomationclient/IUIAutomationNotificationEventHandler::HandleNotificationEvent","winauto.IUIAutomationNotificationEventHandler_HandleNotificationEvent"]
old-location: winauto\IUIAutomationNotificationEventHandler_HandleNotificationEvent.htm
tech.root: WinAuto
ms.assetid: A5FC58D4-B624-4EB1-9AC4-CD7C6F3BBFAE
ms.date: 12/05/2018
ms.keywords: HandleNotificationEvent, HandleNotificationEvent method [Windows Accessibility], HandleNotificationEvent method [Windows Accessibility],IUIAutomationNotificationEventHandler interface, IUIAutomationNotificationEventHandler interface [Windows Accessibility],HandleNotificationEvent method, IUIAutomationNotificationEventHandler.HandleNotificationEvent, IUIAutomationNotificationEventHandler::HandleNotificationEvent, uiautomationclient/IUIAutomationNotificationEventHandler::HandleNotificationEvent, winauto.IUIAutomationNotificationEventHandler_HandleNotificationEvent
f1_keywords:
- uiautomationclient/IUIAutomationNotificationEventHandler.HandleNotificationEvent
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
- UIAutomationClient.h
api_name:
- IUIAutomationNotificationEventHandler.HandleNotificationEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationNotificationEventHandler::HandleNotificationEvent


## -description


Handles a Microsoft UI Automation notification event.


## -parameters




### -param sender [in]

A pointer to the element that raised the event.


### -param arg2

The type of notification.


### -param arg3

Indicates how to process notifications.


### -param displayString

A string to display in the notification message.


### -param activityId

A unique non-localized string to identify an action or group of actions. This is used to pass additional information to the event handler.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler">AddNotificationEventHandler</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationnotificationeventhandler">IUIAutomationNotificationEventHandler</a>
 

 

