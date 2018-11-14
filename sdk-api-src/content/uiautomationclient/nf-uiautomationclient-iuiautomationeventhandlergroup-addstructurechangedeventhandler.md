---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddStructureChangedEventHandler
title: IUIAutomationEventHandlerGroup::AddStructureChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles structure-changed events.
old-location: winauto\uiauto_iuiautomationeventhandlergroup_addstructurechangedeventhandler.htm
tech.root: WinAuto
ms.assetid: E559FF67-3A64-4F2A-B129-FDF8771E3E6A
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AddStructureChangedEventHandler, AddStructureChangedEventHandler method [Windows Accessibility], AddStructureChangedEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddStructureChangedEventHandler method, IUIAutomationEventHandlerGroup.AddStructureChangedEventHandler, IUIAutomationEventHandlerGroup::AddStructureChangedEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddStructureChangedEventHandler, winauto.uiauto_iuiautomationeventhandlergroup_addstructurechangedeventhandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationEventHandlerGroup.AddStructureChangedEventHandler
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
- IUIAutomationEventHandlerGroup.AddStructureChangedEventHandler
: 
---

# IUIAutomationEventHandlerGroup::AddStructureChangedEventHandler


## -description


Registers a method that handles structure-changed events.
<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters




### -param arg1 [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

A pointer to the object that handles the structure-changed event.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>
 

 

