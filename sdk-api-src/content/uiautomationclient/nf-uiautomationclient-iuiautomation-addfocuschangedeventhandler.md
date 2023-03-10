---
UID: NF:uiautomationclient.IUIAutomation.AddFocusChangedEventHandler
title: IUIAutomation::AddFocusChangedEventHandler (uiautomationclient.h)
description: Registers a method that handles focus-changed events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
helpviewer_keywords: ["AddFocusChangedEventHandler","AddFocusChangedEventHandler method [Windows Accessibility]","AddFocusChangedEventHandler method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","AddFocusChangedEventHandler method","IUIAutomation.AddFocusChangedEventHandler","IUIAutomation::AddFocusChangedEventHandler","uiauto.uiauto_IUIAutomation_AddFocusChangedEventHandler","uiauto_IUIAutomation_AddFocusChangedEventHandler","uiautomationclient/IUIAutomation::AddFocusChangedEventHandler","winauto.uiauto_IUIAutomation_AddFocusChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation_AddFocusChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 469e9c3e-366f-4c13-8c27-58fdb705d4d9
ms.date: 12/05/2018
ms.keywords: AddFocusChangedEventHandler, AddFocusChangedEventHandler method [Windows Accessibility], AddFocusChangedEventHandler method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],AddFocusChangedEventHandler method, IUIAutomation.AddFocusChangedEventHandler, IUIAutomation::AddFocusChangedEventHandler, uiauto.uiauto_IUIAutomation_AddFocusChangedEventHandler, uiauto_IUIAutomation_AddFocusChangedEventHandler, uiautomationclient/IUIAutomation::AddFocusChangedEventHandler, winauto.uiauto_IUIAutomation_AddFocusChangedEventHandler
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
 - IUIAutomation::AddFocusChangedEventHandler
 - uiautomationclient/IUIAutomation::AddFocusChangedEventHandler
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
 - IUIAutomation.AddFocusChangedEventHandler
---

# IUIAutomation::AddFocusChangedEventHandler


## -description

Registers a method that handles focus-changed events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler">IUIAutomationFocusChangedEventHandler</a>*</b>

A pointer to the object that handles the event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Focus-changed events are system-wide; you cannot set a narrower scope.

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.


#### Examples

The following example function creates an object that implements <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler">IUIAutomationFocusChangedEventHandler</a> and subscribes to the event by adding the handler.


```cpp
HRESULT AddFocusHandler(IUIAutomation* pAutomation)
{ 
    // CFocusHandler is a class that implements IUIAutomationFocusChangedEventHandler. 
    CFocusHandler* pFocusHandler = new CFocusHandler();
    if (!pFocusHandler)
    {
        return E_OUTOFMEMORY;
    }
    IUIAutomationFocusChangedEventHandler* pHandler;
    pFocusHandler->QueryInterface(IID_IUIAutomationFocusChangedEventHandler, (void**)&pHandler);
    HRESULT hr = pAutomation->AddFocusChangedEventHandler(NULL, pHandler);
    pFocusHandler->Release();
    return hr;
}

```

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-cachingforclients">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler">IUIAutomationFocusChangedEventHandler</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler">RemoveFocusChangedEventHandler</a>



<a href="/windows/desktop/WinAuto/uiauto-eventsforclients">Subscribing to UI Automation Events</a>



<a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>