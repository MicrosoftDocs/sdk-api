---
UID: NF:uiautomationclient.IUIAutomation.AddStructureChangedEventHandler
title: IUIAutomation::AddStructureChangedEventHandler (uiautomationclient.h)
description: Registers a method that handles structure-changed events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
helpviewer_keywords: ["AddStructureChangedEventHandler","AddStructureChangedEventHandler method [Windows Accessibility]","AddStructureChangedEventHandler method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","AddStructureChangedEventHandler method","IUIAutomation.AddStructureChangedEventHandler","IUIAutomation::AddStructureChangedEventHandler","uiauto.uiauto_IUIAutomation_AddStructureChangedEventHandler","uiauto_IUIAutomation_AddStructureChangedEventHandler","uiautomationclient/IUIAutomation::AddStructureChangedEventHandler","winauto.uiauto_IUIAutomation_AddStructureChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation_AddStructureChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 671049a4-50cf-49df-9028-7af38629b7a9
ms.date: 12/05/2018
ms.keywords: AddStructureChangedEventHandler, AddStructureChangedEventHandler method [Windows Accessibility], AddStructureChangedEventHandler method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],AddStructureChangedEventHandler method, IUIAutomation.AddStructureChangedEventHandler, IUIAutomation::AddStructureChangedEventHandler, uiauto.uiauto_IUIAutomation_AddStructureChangedEventHandler, uiauto_IUIAutomation_AddStructureChangedEventHandler, uiautomationclient/IUIAutomation::AddStructureChangedEventHandler, winauto.uiauto_IUIAutomation_AddStructureChangedEventHandler
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
 - IUIAutomation::AddStructureChangedEventHandler
 - uiautomationclient/IUIAutomation::AddStructureChangedEventHandler
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
 - IUIAutomation.AddStructureChangedEventHandler
---

# IUIAutomation::AddStructureChangedEventHandler


## -description

Registers a method that handles structure-changed events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler">IUIAutomationStructureChangedEventHandler</a>*</b>

A pointer to the object that handles the structure-changed event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler">RemoveStructureChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/uiauto-eventsforclients">Subscribing to UI Automation Events</a>



<a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>