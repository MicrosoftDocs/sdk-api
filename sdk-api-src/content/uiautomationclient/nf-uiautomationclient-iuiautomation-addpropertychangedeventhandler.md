---
UID: NF:uiautomationclient.IUIAutomation.AddPropertyChangedEventHandler
title: IUIAutomation::AddPropertyChangedEventHandler (uiautomationclient.h)
description: Registers a method that handles and array of property-changed events.
helpviewer_keywords: ["AddPropertyChangedEventHandler","AddPropertyChangedEventHandler method [Windows Accessibility]","AddPropertyChangedEventHandler method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","AddPropertyChangedEventHandler method","IUIAutomation.AddPropertyChangedEventHandler","IUIAutomation::AddPropertyChangedEventHandler","uiauto.uiauto_IUIAutomation_AddPropertyChangedEventHandler","uiauto_IUIAutomation_AddPropertyChangedEventHandler","uiautomationclient/IUIAutomation::AddPropertyChangedEventHandler","winauto.uiauto_IUIAutomation_AddPropertyChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation_AddPropertyChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 2623a48e-8818-486c-9bde-b218cde49189
ms.date: 12/05/2018
ms.keywords: AddPropertyChangedEventHandler, AddPropertyChangedEventHandler method [Windows Accessibility], AddPropertyChangedEventHandler method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],AddPropertyChangedEventHandler method, IUIAutomation.AddPropertyChangedEventHandler, IUIAutomation::AddPropertyChangedEventHandler, uiauto.uiauto_IUIAutomation_AddPropertyChangedEventHandler, uiauto_IUIAutomation_AddPropertyChangedEventHandler, uiautomationclient/IUIAutomation::AddPropertyChangedEventHandler, winauto.uiauto_IUIAutomation_AddPropertyChangedEventHandler
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
 - IUIAutomation::AddPropertyChangedEventHandler
 - uiautomationclient/IUIAutomation::AddPropertyChangedEventHandler
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
 - IUIAutomation.AddPropertyChangedEventHandler
---

# IUIAutomation::AddPropertyChangedEventHandler


## -description

Registers a method that handles and array of property-changed events. 
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and children.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler">IUIAutomationPropertyChangedEventHandler</a>*</b>

A pointer to the object that handles the event.

### -param propertyArray [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the UI Automation properties of interest. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The UI item specified by <i>element</i> might not support the properties specified by the <i>propertyArray</i> parameter. 
			

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray">AddPropertyChangedEventHandlerNativeArray</a>



<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler">RemovePropertyChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/uiauto-eventsforclients">Subscribing to UI Automation Events</a>



<a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>