---
UID: NF:uiautomationclient.IUIAutomationEventHandler.HandleAutomationEvent
title: IUIAutomationEventHandler::HandleAutomationEvent
author: windows-sdk-content
description: Handles a Microsoft UI Automation event.
old-location: winauto\uiauto_IUIAutomationEventHandler_HandleAutomationEvent.htm
tech.root: WinAuto
ms.assetid: 56668923-f21a-4d38-9175-95785892388c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: HandleAutomationEvent, HandleAutomationEvent method [Windows Accessibility], HandleAutomationEvent method [Windows Accessibility],IUIAutomationEventHandler interface, IUIAutomationEventHandler interface [Windows Accessibility],HandleAutomationEvent method, IUIAutomationEventHandler.HandleAutomationEvent, IUIAutomationEventHandler::HandleAutomationEvent, uiauto.uiauto_IUIAutomationEventHandler_HandleAutomationEvent, uiauto_IUIAutomationEventHandler_HandleAutomationEvent, uiautomationclient/IUIAutomationEventHandler::HandleAutomationEvent, winauto.uiauto_IUIAutomationEventHandler_HandleAutomationEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
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
 - IUIAutomationEventHandler.HandleAutomationEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationEventHandler::HandleAutomationEvent


## -description


Handles a Microsoft UI Automation event.


## -parameters




### -param sender [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to  the element that raised the event.


### -param eventId [in]

Type: <b>EVENTID</b>

The event identifier. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the application to handle events that it has subscribed to by using <a href="https://msdn.microsoft.com/15ceca71-33e8-4d66-afd6-3d50fe81c127">AddAutomationEventHandler</a>.
			

Adjusting an event handler from within this method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/3b79e085-fb38-403d-b7f1-3e7680f3449f">IUIAutomationEventHandler</a>
 

 

