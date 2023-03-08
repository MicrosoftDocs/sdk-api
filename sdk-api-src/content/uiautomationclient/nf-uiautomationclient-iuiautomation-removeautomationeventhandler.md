---
UID: NF:uiautomationclient.IUIAutomation.RemoveAutomationEventHandler
title: IUIAutomation::RemoveAutomationEventHandler (uiautomationclient.h)
description: Removes the specified UI Automation event handler.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","RemoveAutomationEventHandler method","IUIAutomation.RemoveAutomationEventHandler","IUIAutomation::RemoveAutomationEventHandler","RemoveAutomationEventHandler","RemoveAutomationEventHandler method [Windows Accessibility]","RemoveAutomationEventHandler method [Windows Accessibility]","IUIAutomation interface","uiauto.uiauto_IUIAutomation_RemoveAutomationEventHandler","uiauto_IUIAutomation_RemoveAutomationEventHandler","uiautomationclient/IUIAutomation::RemoveAutomationEventHandler","winauto.uiauto_IUIAutomation_RemoveAutomationEventHandler"]
old-location: winauto\uiauto_IUIAutomation_RemoveAutomationEventHandler.htm
tech.root: WinAuto
ms.assetid: c4ebf7d3-c3c4-424b-af69-b8c13dd7a4dd
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],RemoveAutomationEventHandler method, IUIAutomation.RemoveAutomationEventHandler, IUIAutomation::RemoveAutomationEventHandler, RemoveAutomationEventHandler, RemoveAutomationEventHandler method [Windows Accessibility], RemoveAutomationEventHandler method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_RemoveAutomationEventHandler, uiauto_IUIAutomation_RemoveAutomationEventHandler, uiautomationclient/IUIAutomation::RemoveAutomationEventHandler, winauto.uiauto_IUIAutomation_RemoveAutomationEventHandler
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
 - IUIAutomation::RemoveAutomationEventHandler
 - uiautomationclient/IUIAutomation::RemoveAutomationEventHandler
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
 - IUIAutomation.RemoveAutomationEventHandler
---

# IUIAutomation::RemoveAutomationEventHandler


## -description

Removes the specified UI Automation event handler.

## -parameters

### -param eventId [in]

Type: <b>EVENTID</b>

The identifier of the event being handled. For a list of event IDs, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element that is handling the event.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationeventhandler">IUIAutomationEventHandler</a>*</b>

A pointer to the handler method that was passed to <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addautomationeventhandler">IUIAutomation::AddAutomationEventHandler</a> for the specified event identifier and UI Automation element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, 
if the event is received simultaneously with the request to unsubscribe the event. The best practice 
is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count 
has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an 
access violation if an event is delivered late.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler">RemoveFocusChangedEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler">RemovePropertyChangedEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler">RemoveStructureChangedEventHandler</a>