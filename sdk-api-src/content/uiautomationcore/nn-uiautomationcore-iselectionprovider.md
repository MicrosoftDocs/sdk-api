---
UID: NN:uiautomationcore.ISelectionProvider
title: ISelectionProvider
author: windows-sdk-content
description: Provides access to controls that act as containers for a collection of individual, selectable child items.
old-location: winauto\uiauto_ISelectionProvider.htm
tech.root: WinAuto
ms.assetid: e02731f8-e58d-4c66-95bf-005cf954471c
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ISelectionProvider, ISelectionProvider interface [Windows Accessibility], ISelectionProvider interface [Windows Accessibility],described, uiauto.uiauto_ISelectionProvider, uiauto_ISelectionProvider, uiautomationcore/ISelectionProvider, winauto.uiauto_ISelectionProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ISelectionProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISelectionProvider interface


## -description


Provides access 
        to controls that act as containers for a collection of individual, selectable child items. 
        The children of this control must implement <a href="https://msdn.microsoft.com/464b05e3-06da-44b9-b4a6-c64452fcdb6d">ISelectionItemProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISelectionProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISelectionProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f97481b9-f227-47fb-9163-a65a259c9d78">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation provider for each child element that is selected.
        

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectionProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/00098f73-4cbe-4cc5-a91a-479721f9b7c1">CanSelectMultiple</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the UI Automation provider 
        allows more than one child element to be selected concurrently.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1b1ee10d-39de-480f-901f-198d9a9c48f8">IsSelectionRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the UI Automation provider requires at least one child element to be selected.
        

</td>
</tr>
</table> 


## -remarks



This interface is implemented by a UI Automation provider.

Providers should raise an event of type <a href="uiauto_event_ids.htm">UIA_Selection_InvalidatedEventId</a> when a selection in a container has changed significantly.





## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

