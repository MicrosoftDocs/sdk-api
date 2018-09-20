---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddChangesEventHandler
title: IUIAutomationEventHandlerGroup::AddChangesEventHandler
author: windows-sdk-content
description: Registers a method that handles change events.
old-location: winauto\uiauto_iuiautomationeventhandlergroup_addchangeseventhandler.htm
tech.root: WinAuto
ms.assetid: AB46E0D3-FFE0-4565-A971-191C0D266506
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: AddChangesEventHandler, AddChangesEventHandler method [Windows Accessibility], AddChangesEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddChangesEventHandler method, IUIAutomationEventHandlerGroup.AddChangesEventHandler, IUIAutomationEventHandlerGroup::AddChangesEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddChangesEventHandler, winauto.uiauto_iuiautomationeventhandlergroup_addchangeseventhandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, next major update [desktop apps only]
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
 - IUIAutomationEventHandlerGroup.AddChangesEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationEventHandlerGroup::AddChangesEventHandler


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Registers a method that handles change events.
<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters




### -param arg1

TBD


### -param changeTypes [in]

A pointer to a list of integers that indicate the change types the event represents.


### -param changesCount [in]

The number of changes that occurred in this event.


### -param cacheRequest

TBD


### -param handler [in]

A pointer to the object that handles the changes event.


#### - pCacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


#### - scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.




## -see-also




<a href="winauto.iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>
 

 

