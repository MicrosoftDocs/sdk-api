---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddAutomationEventHandler
title: IUIAutomationEventHandlerGroup::AddAutomationEventHandler (uiautomationclient.h)
description: Registers a method that handles Microsoft UI Automation events.
helpviewer_keywords: ["AddAutomationEventHandler","AddAutomationEventHandler method [Windows Accessibility]","AddAutomationEventHandler method [Windows Accessibility]","IUIAutomationEventHandlerGroup interface","IUIAutomationEventHandlerGroup interface [Windows Accessibility]","AddAutomationEventHandler method","IUIAutomationEventHandlerGroup.AddAutomationEventHandler","IUIAutomationEventHandlerGroup::AddAutomationEventHandler","uiautomationclient/IUIAutomationEventHandlerGroup::AddAutomationEventHandler","winauto.uiauto_iuiautomationeventhandlergroup_addautomationeventhandler"]
old-location: winauto\uiauto_iuiautomationeventhandlergroup_addautomationeventhandler.htm
tech.root: WinAuto
ms.assetid: EEBEDC7B-48B5-4074-8B85-1DC8B47A90AD
ms.date: 12/05/2018
ms.keywords: AddAutomationEventHandler, AddAutomationEventHandler method [Windows Accessibility], AddAutomationEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddAutomationEventHandler method, IUIAutomationEventHandlerGroup.AddAutomationEventHandler, IUIAutomationEventHandlerGroup::AddAutomationEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddAutomationEventHandler, winauto.uiauto_iuiautomationeventhandlergroup_addautomationeventhandler
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
 - IUIAutomationEventHandlerGroup::AddAutomationEventHandler
 - uiautomationclient/IUIAutomationEventHandlerGroup::AddAutomationEventHandler
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
 - IUIAutomationEventHandlerGroup.AddAutomationEventHandler
---

# IUIAutomationEventHandlerGroup::AddAutomationEventHandler


## -description

Registers a method that handles Microsoft UI Automation events.
<div class="alert"><b>Important</b>  UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters

### -param eventId [in]

The identifier of the event that the method handles. For a list of event IDs, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -param scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

A pointer to the object that handles the event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>