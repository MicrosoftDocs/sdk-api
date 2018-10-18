---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddTextEditTextChangedEventHandler
title: IUIAutomationEventHandlerGroup::AddTextEditTextChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles programmatic text-edit events.
old-location: winauto\uiauto_iuiautomationeventhandlergroup_addtextedittextchangedeventhandler.htm
tech.root: WinAuto
ms.assetid: D26780A1-AF5E-42E9-BBDA-4685AA184BD1
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: AddTextEditTextChangedEventHandler, AddTextEditTextChangedEventHandler method [Windows Accessibility], AddTextEditTextChangedEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddTextEditTextChangedEventHandler method, IUIAutomationEventHandlerGroup.AddTextEditTextChangedEventHandler, IUIAutomationEventHandlerGroup::AddTextEditTextChangedEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddTextEditTextChangedEventHandler, winauto.uiauto_iuiautomationeventhandlergroup_addtextedittextchangedeventhandler
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
 - IUIAutomationEventHandlerGroup.AddTextEditTextChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationEventHandlerGroup::AddTextEditTextChangedEventHandler


## -description


Registers a method that handles programmatic text-edit events.
<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

A pointer to the object that handles the programmatic text-edit event.



#### - scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


#### - textEditChangeType [in]

The specific change type to listen for. Clients register for each text-edit change type separately, so that the UI Automation system can check for registered listeners at run-time and avoid raising events for particular text-edit changes when there are no listeners.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.




## -see-also




<a href="winauto.iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>
 

 

