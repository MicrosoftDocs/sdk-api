---
UID: NF:uiautomationclient.IUIAutomation.RemovePropertyChangedEventHandler
title: IUIAutomation::RemovePropertyChangedEventHandler (uiautomationclient.h)
description: Removes a property-changed event handler.
helpviewer_keywords: ["IUIAutomation interface [Windows Accessibility]","RemovePropertyChangedEventHandler method","IUIAutomation.RemovePropertyChangedEventHandler","IUIAutomation::RemovePropertyChangedEventHandler","RemovePropertyChangedEventHandler","RemovePropertyChangedEventHandler method [Windows Accessibility]","RemovePropertyChangedEventHandler method [Windows Accessibility]","IUIAutomation interface","uiauto.uiauto_IUIAutomation_RemovePropertyChangedEventHandler","uiauto_IUIAutomation_RemovePropertyChangedEventHandler","uiautomationclient/IUIAutomation::RemovePropertyChangedEventHandler","winauto.uiauto_IUIAutomation_RemovePropertyChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation_RemovePropertyChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: d8f7600f-a33e-4f30-ae8e-423f9c71edbe
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],RemovePropertyChangedEventHandler method, IUIAutomation.RemovePropertyChangedEventHandler, IUIAutomation::RemovePropertyChangedEventHandler, RemovePropertyChangedEventHandler, RemovePropertyChangedEventHandler method [Windows Accessibility], RemovePropertyChangedEventHandler method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_RemovePropertyChangedEventHandler, uiauto_IUIAutomation_RemovePropertyChangedEventHandler, uiautomationclient/IUIAutomation::RemovePropertyChangedEventHandler, winauto.uiauto_IUIAutomation_RemovePropertyChangedEventHandler
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
 - IUIAutomation::RemovePropertyChangedEventHandler
 - uiautomationclient/IUIAutomation::RemovePropertyChangedEventHandler
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
 - IUIAutomation.RemovePropertyChangedEventHandler
---

# IUIAutomation::RemovePropertyChangedEventHandler


## -description

Removes a property-changed event handler.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler">IUIAutomationPropertyChangedEventHandler</a>*</b>

A pointer to the interface that was passed to <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">IUIAutomation::AddPropertyChangedEventHandler</a>.

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



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler">RemoveAutomationEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler">RemoveFocusChangedEventHandler</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler">RemoveStructureChangedEventHandler</a>