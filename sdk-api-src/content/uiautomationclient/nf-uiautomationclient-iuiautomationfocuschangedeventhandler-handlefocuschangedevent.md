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
 

 

