---
UID: NF:uiautomationclient.IUIAutomation.AddPropertyChangedEventHandlerNativeArray
title: IUIAutomation::AddPropertyChangedEventHandlerNativeArray (uiautomationclient.h)
description: Registers a method that handles a native array of property-changed events.
helpviewer_keywords: ["AddPropertyChangedEventHandlerNativeArray","AddPropertyChangedEventHandlerNativeArray method [Windows Accessibility]","AddPropertyChangedEventHandlerNativeArray method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","AddPropertyChangedEventHandlerNativeArray method","IUIAutomation.AddPropertyChangedEventHandlerNativeArray","IUIAutomation::AddPropertyChangedEventHandlerNativeArray","uiauto.uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray","uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray","uiautomationclient/IUIAutomation::AddPropertyChangedEventHandlerNativeArray","winauto.uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray"]
old-location: winauto\uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray.htm
tech.root: WinAuto
ms.assetid: 0d3cf5c3-5d0e-4214-a9fc-8b0132ad9b77
ms.date: 12/05/2018
ms.keywords: AddPropertyChangedEventHandlerNativeArray, AddPropertyChangedEventHandlerNativeArray method [Windows Accessibility], AddPropertyChangedEventHandlerNativeArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],AddPropertyChangedEventHandlerNativeArray method, IUIAutomation.AddPropertyChangedEventHandlerNativeArray, IUIAutomation::AddPropertyChangedEventHandlerNativeArray, uiauto.uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray, uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray, uiautomationclient/IUIAutomation::AddPropertyChangedEventHandlerNativeArray, winauto.uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray
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
 - IUIAutomation::AddPropertyChangedEventHandlerNativeArray
 - uiautomationclient/IUIAutomation::AddPropertyChangedEventHandlerNativeArray
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
 - IUIAutomation.AddPropertyChangedEventHandlerNativeArray
---

# IUIAutomation::AddPropertyChangedEventHandlerNativeArray


## -description

Registers a method that handles a native array of property-changed events. 
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.

### -param unnamedParam2 [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and children.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler">IUIAutomationPropertyChangedEventHandler</a>*</b>

A pointer to the object that handles the event.

### -param propertyArray [in]

Type: <b>PROPERTYID*</b>

A pointer to the identifiers of the UI Automation properties of interest.  For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param propertyCount [in]

Type: <b>int</b>

The number of property identifiers in <i>propertyArray</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## example

For code examples that show how to implement interfaces that enable clients to receive and handle Microsoft UI Automation events (including AddPropertyChangedEventHandlerNativeArray), see [How to Implement Event Handlers](/windows/win32/winauto/uiauto-howto-implement-event-handlers).

## -remarks

The UI item specified by <i>element</i> might not support the properties specified by the <i>propertyArray</i> parameter. 

This method serves the same purpose as <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">IUIAutomation::AddPropertyChangedEventHandler</a>, but takes a normal array of property identifiers instead of a SAFEARRAY. 
			

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">AddPropertyChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler">RemovePropertyChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/uiauto-eventsforclients">Subscribing to UI Automation Events</a>



<a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>
