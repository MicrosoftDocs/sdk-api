---
UID: NF:uiautomationclient.IUIAutomationProxyFactoryEntry.GetWinEventsForAutomationEvent
title: IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent (uiautomationclient.h)
description: Retrieves the list of WinEvents that are mapped to a specific Microsoft UI Automation event. If an element represented by this proxy raises one the listed WinEvents, the proxy handles it.
helpviewer_keywords: ["GetWinEventsForAutomationEvent","GetWinEventsForAutomationEvent method [Windows Accessibility]","GetWinEventsForAutomationEvent method [Windows Accessibility]","IUIAutomationProxyFactoryEntry interface","IUIAutomationProxyFactoryEntry interface [Windows Accessibility]","GetWinEventsForAutomationEvent method","IUIAutomationProxyFactoryEntry.GetWinEventsForAutomationEvent","IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent","uiauto.uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent","uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent","uiautomationclient/IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent","winauto.uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent"]
old-location: winauto\uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent.htm
tech.root: WinAuto
ms.assetid: f8daa90f-9fad-48c7-8f22-e8c673fca330
ms.date: 12/05/2018
ms.keywords: GetWinEventsForAutomationEvent, GetWinEventsForAutomationEvent method [Windows Accessibility], GetWinEventsForAutomationEvent method [Windows Accessibility],IUIAutomationProxyFactoryEntry interface, IUIAutomationProxyFactoryEntry interface [Windows Accessibility],GetWinEventsForAutomationEvent method, IUIAutomationProxyFactoryEntry.GetWinEventsForAutomationEvent, IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent, uiauto.uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent, uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent, uiautomationclient/IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent, winauto.uiauto_IUIAutomationProxyFactoryEntry_GetWinEventsForAutomationEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent
 - uiautomationclient/IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationProxyFactoryEntry.GetWinEventsForAutomationEvent
---

# IUIAutomationProxyFactoryEntry::GetWinEventsForAutomationEvent


## -description

Retrieves the list of WinEvents that are mapped to a specific Microsoft UI Automation event. If an element represented by this proxy raises one the listed WinEvents, the proxy handles it.

## -parameters

### -param eventId [in]

Type: <b>EVENTID</b>

The event identifier. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param winEvents [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to the list of WinEvents that map to this event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationproxyfactoryentry">IUIAutomationProxyFactoryEntry</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationproxyfactoryentry-setwineventsforautomationevent">SetWinEventsForAutomationEvent</a>