---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler
title: IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles property-changed events.
old-location: winauto\uiauto_iuiautomationeventhandlergroup_addpropertychangedeventhandler.htm
tech.root: WinAuto
ms.assetid: 186958B6-6D13-41F2-B6E5-A4C36D1B8451
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: AddPropertyChangedEventHandler, AddPropertyChangedEventHandler method [Windows Accessibility], AddPropertyChangedEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddPropertyChangedEventHandler method, IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler, IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler, winauto.uiauto_iuiautomationeventhandlergroup_addpropertychangedeventhandler
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
 - IUIAutomationEventHandlerGroup.AddPropertyChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationEventHandlerGroup::AddPropertyChangedEventHandler


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Registers a method that handles property-changed events. 
<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters




### -param arg1

TBD


### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

A pointer to the object that handles the event.


### -param propertyArray [in]

A pointer to the UI Automation properties of interest. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param propertyCount

The number of properties being monitored.


#### - scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and children.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.




## -see-also




<a href="winauto.iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>
 

 

