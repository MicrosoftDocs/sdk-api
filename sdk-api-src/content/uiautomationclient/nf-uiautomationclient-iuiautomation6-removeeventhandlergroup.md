---
UID: NF:uiautomationclient.IUIAutomation6.RemoveEventHandlerGroup
title: IUIAutomation6::RemoveEventHandlerGroup
author: windows-sdk-content
description: Asynchronously removes the specified UI Automation event handler group.
old-location: winauto\uiauto_IUIAutomation6_RemoveEventHandlerGroup.htm
tech.root: WinAuto
ms.assetid: 43BDE7F5-67DF-4DE5-AEDE-068421375E07
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IUIAutomation6 interface [Windows Accessibility],RemoveEventHandlerGroup method, IUIAutomation6.RemoveEventHandlerGroup, IUIAutomation6::RemoveEventHandlerGroup, RemoveEventHandlerGroup, RemoveEventHandlerGroup method [Windows Accessibility], RemoveEventHandlerGroup method [Windows Accessibility],IUIAutomation6 interface, uiautomationclient/IUIAutomation6::RemoveEventHandlerGroup, winauto.uiauto_IUIAutomation6_RemoveEventHandlerGroup
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
 - IUIAutomation6.RemoveEventHandlerGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation6::RemoveEventHandlerGroup


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Asynchronously removes the specified UI Automation event handler group.


## -parameters




### -param element [in]

A pointer to the UI Automation element associated with the event handler group.


### -param handlerGroup

The collection of event handlers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, if the event is received simultaneously with the request to unsubscribe the event. The best practice is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an access violation if an event is delivered late.




## -see-also




<a href="winauto.uiauto_iuiautomation6_addeventhandlergroup">AddEventHandlerGroup</a>



<a href="winauto.iuiautomation6">IUIAutomation6</a>
 

 

