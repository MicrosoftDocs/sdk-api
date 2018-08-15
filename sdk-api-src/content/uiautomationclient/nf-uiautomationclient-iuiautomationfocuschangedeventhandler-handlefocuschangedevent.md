---
UID: NF:uiautomationclient.IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent
title: IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent
author: windows-sdk-content
description: Handles the event raised when the keyboard focus moves to a different UI Automation element.
old-location: winauto\uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent.htm
old-project: WinAuto
ms.assetid: 7d90982f-4805-4ebb-a9f9-e335dc15d519
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HandleFocusChangedEvent, HandleFocusChangedEvent method [Windows Accessibility], HandleFocusChangedEvent method [Windows Accessibility],IUIAutomationFocusChangedEventHandler interface, IUIAutomationFocusChangedEventHandler interface [Windows Accessibility],HandleFocusChangedEvent method, IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent, IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent, uiauto.uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent, uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent, uiautomationclient/IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent, winauto.uiauto_IUIAutomationFocusChangedEventHandler_HandleFocusChangedEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationFocusChangedEventHandler.HandleFocusChangedEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationFocusChangedEventHandler::HandleFocusChangedEvent


## -description


Handles the event raised when the keyboard focus moves to a different UI Automation element.


## -parameters




### -param sender [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element that has received the focus.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that were subscribed to by using <a href="https://msdn.microsoft.com/469e9c3e-366f-4c13-8c27-58fdb705d4d9">AddFocusChangedEventHandler</a>


The UI Automation element represented by <i>sender</i> might not have any cached properties or control patterns, depending on whether the application subscribed to this event while a cache request was active.

Adjusting an event handler from within this method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/5dcc6ab0-02c1-4168-96f1-a71a00268527">IUIAutomationFocusChangedEventHandler</a>
 

 

