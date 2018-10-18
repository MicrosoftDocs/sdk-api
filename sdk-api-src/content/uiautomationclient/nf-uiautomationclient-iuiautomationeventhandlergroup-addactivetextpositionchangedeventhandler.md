---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler
title: IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles when the active text position changes.
old-location: winauto\uiauto_IUIAutomationEventHandlerGroup_AddActiveTextPositionChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: D3A09F61-5536-409E-BFA2-63D6E4A774A2
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: AddActiveTextPositionChangedEventHandler, AddActiveTextPositionChangedEventHandler method [Windows Accessibility], AddActiveTextPositionChangedEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddActiveTextPositionChangedEventHandler method, IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler, IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler, winauto.uiauto_IUIAutomationEventHandlerGroup_AddActiveTextPositionChangedEventHandler
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
 - IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler


## -description


Registers a method that handles when the active text position changes.<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> namespaces.</div>
<div> </div>



## -parameters




### -param arg1

TBD


### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

A pointer to the object that handles the active text position changed event.



#### - scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.




## -see-also




<a href="winauto.iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>
 

 

