---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler
title: IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler (uiautomationclient.h)
description: Registers a method that handles a property-changed event.
helpviewer_keywords: ["AddPropertyChangedEventHandler","AddPropertyChangedEventHandler method [Windows Accessibility]","AddPropertyChangedEventHandler method [Windows Accessibility]","IUIAutomationEventHandlerGroup interface","IUIAutomationEventHandlerGroup interface [Windows Accessibility]","AddPropertyChangedEventHandler method","IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler","IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler","uiautomationclient/IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler","winauto.uiauto_iuiautomationeventhandlergroup_addpropertychangedeventhandler"]
old-location: winauto\uiauto_iuiautomationeventhandlergroup_addpropertychangedeventhandler.htm
tech.root: WinAuto
ms.assetid: 186958B6-6D13-41F2-B6E5-A4C36D1B8451
ms.date: 12/05/2018
ms.keywords: AddPropertyChangedEventHandler, AddPropertyChangedEventHandler method [Windows Accessibility], AddPropertyChangedEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddPropertyChangedEventHandler method, IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler, IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler, winauto.uiauto_iuiautomationeventhandlergroup_addpropertychangedeventhandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler
 - uiautomationclient/IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler
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
 - IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler
---

# IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler


## -description

Registers a method that handles a property-changed event. 
<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters

### -param scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and children.

### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

A pointer to the object that handles the event.

### -param propertyArray [in]

A pointer to the UI Automation properties of interest. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param propertyCount

The number of properties being monitored.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>