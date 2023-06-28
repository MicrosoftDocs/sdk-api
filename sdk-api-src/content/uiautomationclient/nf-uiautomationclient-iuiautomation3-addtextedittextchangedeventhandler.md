---
UID: NF:uiautomationclient.IUIAutomation3.AddTextEditTextChangedEventHandler
title: IUIAutomation3::AddTextEditTextChangedEventHandler (uiautomationclient.h)
description: Registers a method that handles programmatic text-edit events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
helpviewer_keywords: ["AddTextEditTextChangedEventHandler","AddTextEditTextChangedEventHandler method [Windows Accessibility]","AddTextEditTextChangedEventHandler method [Windows Accessibility]","IUIAutomation3 interface","IUIAutomation3 interface [Windows Accessibility]","AddTextEditTextChangedEventHandler method","IUIAutomation3.AddTextEditTextChangedEventHandler","IUIAutomation3::AddTextEditTextChangedEventHandler","uiautomationclient/IUIAutomation3::AddTextEditTextChangedEventHandler","winauto.uiauto_IUIAutomation3_AddTextEditTextChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation3_AddTextEditTextChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: E4FBD04E-2E0B-6B87-F589-C3214EF54E5F
ms.date: 12/05/2018
ms.keywords: AddTextEditTextChangedEventHandler, AddTextEditTextChangedEventHandler method [Windows Accessibility], AddTextEditTextChangedEventHandler method [Windows Accessibility],IUIAutomation3 interface, IUIAutomation3 interface [Windows Accessibility],AddTextEditTextChangedEventHandler method, IUIAutomation3.AddTextEditTextChangedEventHandler, IUIAutomation3::AddTextEditTextChangedEventHandler, uiautomationclient/IUIAutomation3::AddTextEditTextChangedEventHandler, winauto.uiauto_IUIAutomation3_AddTextEditTextChangedEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IUIAutomation3::AddTextEditTextChangedEventHandler
 - uiautomationclient/IUIAutomation3::AddTextEditTextChangedEventHandler
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
 - IUIAutomation3.AddTextEditTextChangedEventHandler
---

# IUIAutomation3::AddTextEditTextChangedEventHandler


## -description

Registers a method that handles programmatic text-edit events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param textEditChangeType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-texteditchangetype">TextEditChangeType</a></b>

The specific change type to listen for. Clients register for each text-edit change type separately, so that the UI Automation system can check for registered listeners at run-time and avoid raising events for particular text-edit changes when there are no listeners.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler">IUIAutomationTextEditTextChangedEventHandler</a>*</b>

A pointer to the object that handles the programmatic text-edit event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation3">IUIAutomation3</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler">RemoveTextEditTextChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/uiauto-eventsforclients">Subscribing to UI Automation Events</a>



<a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>