---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent
title: IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent (uiautomationclient.h)
description: Maps Microsoft UI Automation events to WinEvents.
old-location: winauto\uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent.htm
tech.root: WinAuto
ms.assetid: 694cc14b-837c-4e09-b1e7-91bdc237657f
ms.date: 12/05/2018
ms.keywords: IUIAutomationProxyFactoryEntry interface [Windows Accessibility],SetWinEventsForAutomationEvent method, IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent, IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent, SetWinEventsForAutomationEvent, SetWinEventsForAutomationEvent method [Windows Accessibility], SetWinEventsForAutomationEvent method [Windows Accessibility],IUIAutomationProxyFactoryEntry interface, uiauto.uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent, uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent, uiautomationclient/IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent, winauto.uiauto_IUIAutomationProxyFactoryEntry_SetWinEventsForAutomationEvent
f1_keywords:
- uiautomationclient/IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent
dev_langs:
- c++
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
- IUIAutomationProxyFactoryEntry.SetWinEventsForAutomationEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationProxyFactoryEntry::SetWinEventsForAutomationEvent


## -description


Maps Microsoft UI Automation events to WinEvents.


## -parameters




### -param eventId [in]

Type: <b>EVENTID</b>

The event identifier. For a list of event identifiers, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.


### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.


### -param winEvents [in]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

The list of WinEvents that map to this event.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a client application subscribes to a UI Automation event, the UI Automation core also listens for WinEvents that map to this event. For example, suppose that <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-event-ids">UIA_Invoke_InvokedEventId</a> is mapped to <a href="https://docs.microsoft.com/windows/desktop/WinAuto/event-constants">EVENT_OBJECT_INVOKED</a>. When <b>EVENT_OBJECT_INVOKED</b> is raised, the client instantiates the proxy and calls <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iproxyproviderwineventhandler-respondtowinevent">RespondToWinEvent</a> on that proxy. In the implementation of <b>RespondToWinEvent</b>, the proxy calls <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iproxyproviderwineventsink-addautomationevent">AddAutomationEvent</a>. The core then raises the corresponding UI Automation event.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-getwineventsforautomationevent">GetWinEventsForAutomationEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactoryentry">IUIAutomationProxyFactoryEntry</a>



<b>Reference</b>
 

 

