---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent
title: IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent
author: windows-sdk-content
description: Maps Microsoft UI Automation events to WinEvents.
old-location: winauto\uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent.htm
old-project: WinAuto
ms.assetid: 694cc14b-837c-4e09-b1e7-91bdc237657f
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IUIAutomationProxyFactoryEntry interface [Windows Accessibility],SetWinEventsForAutomationEvent method, IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent, IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent, SetWinEventsForAutomationEvent, SetWinEventsForAutomationEvent method [Windows Accessibility], SetWinEventsForAutomationEvent method [Windows Accessibility],IUIAutomationProxyFactoryEntry interface, uiauto.uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent, uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent, uiautomationclient/IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent, winauto.uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent


## -description


Maps Microsoft UI Automation events to WinEvents.


## -parameters




### -param eventId [in]

Type: <b>EVENTID</b>

The event identifier. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param winEvents [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

The list of WinEvents that map to this event.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a client application subscribes to a UI Automation event, the UI Automation core also listens for WinEvents that map to this event. For example, suppose that <a href="uiauto_event_ids.htm">UIA_Invoke_InvokedEventId</a> is mapped to <a href="event_constants.htm">EVENT_OBJECT_INVOKED</a>. When <b>EVENT_OBJECT_INVOKED</b> is raised, the client instantiates the proxy and calls <a href="https://msdn.microsoft.com/b3a63cb9-3eae-43ec-aba1-2f038ca0896f">RespondToWinEvent</a> on that proxy. In the implementation of <b>RespondToWinEvent</b>, the proxy calls <a href="https://msdn.microsoft.com/c1730b6b-f399-4e1f-91d4-5d5e40835a74">AddAutomationEvent</a>. The core then raises the corresponding UI Automation event.
			




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f8daa90f-9fad-48c7-8f22-e8c673fca330">GetWinEventsForAutomationEvent</a>



<a href="https://msdn.microsoft.com/0507deef-35dc-45bb-a7c1-82b84344ee17">IUIAutomationProxyFactoryEntry</a>



<b>Reference</b>
 

 

