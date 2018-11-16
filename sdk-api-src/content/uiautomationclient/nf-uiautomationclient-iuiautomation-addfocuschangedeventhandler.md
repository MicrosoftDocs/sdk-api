---
UID: NF:uiautomationclient.IUIAutomation.AddFocusChangedEventHandler
title: IUIAutomation::AddFocusChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles focus-changed events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
old-location: winauto\uiauto_IUIAutomation_AddFocusChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 469e9c3e-366f-4c13-8c27-58fdb705d4d9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddFocusChangedEventHandler, AddFocusChangedEventHandler method [Windows Accessibility], AddFocusChangedEventHandler method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],AddFocusChangedEventHandler method, IUIAutomation.AddFocusChangedEventHandler, IUIAutomation::AddFocusChangedEventHandler, uiauto.uiauto_IUIAutomation_AddFocusChangedEventHandler, uiauto_IUIAutomation_AddFocusChangedEventHandler, uiautomationclient/IUIAutomation::AddFocusChangedEventHandler, winauto.uiauto_IUIAutomation_AddFocusChangedEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.AddFocusChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomation.AddFocusChangedEventHandler
: 
---

# IUIAutomation::AddFocusChangedEventHandler


## -description


Registers a method that handles focus-changed events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div><div> </div>

## -parameters




### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/5dcc6ab0-02c1-4168-96f1-a71a00268527">IUIAutomationFocusChangedEventHandler</a>*</b>

A pointer to the object that handles the event.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Focus-changed events are system-wide; you cannot set a narrower scope.

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.


#### Examples

The following example function creates an object that implements <a href="https://msdn.microsoft.com/5dcc6ab0-02c1-4168-96f1-a71a00268527">IUIAutomationFocusChangedEventHandler</a> and subscribes to the event by adding the handler.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT AddFocusHandler(IUIAutomation* pAutomation)
{ 
    // CFocusHandler is a class that implements IUIAutomationFocusChangedEventHandler. 
    CFocusHandler* pFocusHandler = new CFocusHandler();
    if (!pFocusHandler)
    {
        return E_OUTOFMEMORY;
    }
    IUIAutomationFocusChangedEventHandler* pHandler;
    pFocusHandler-&gt;QueryInterface(IID_IUIAutomationFocusChangedEventHandler, (void**)&amp;pHandler);
    HRESULT hr = pAutomation-&gt;AddFocusChangedEventHandler(NULL, pHandler);
    pFocusHandler-&gt;Release();
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/948b3bb9-75a9-4197-9680-e6fe7bb86feb">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/5dcc6ab0-02c1-4168-96f1-a71a00268527">IUIAutomationFocusChangedEventHandler</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>



<a href="https://msdn.microsoft.com/96913631-76e0-405a-888d-ac7f6485a18e">RemoveFocusChangedEventHandler</a>



<a href="https://msdn.microsoft.com/7019ecb8-6123-4e00-926c-6725d7e71385">Subscribing to UI Automation Events</a>



<a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>
 

 

