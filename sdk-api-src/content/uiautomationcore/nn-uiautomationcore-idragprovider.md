---
UID: NN:uiautomationcore.IDragProvider
title: IDragProvider
author: windows-sdk-content
description: Enables a Microsoft UI Automation element to describe itself as an element that can be dragged as part of a drag-and-drop operation.
old-location: winauto\uiauto_idragprovider.htm
tech.root: WinAuto
ms.assetid: FAC4A56D-17BC-42E6-A03E-EE45D717DE37
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IDragProvider, IDragProvider interface [Windows Accessibility], IDragProvider interface [Windows Accessibility],described, uiautomationcore/IDragProvider, winauto.uiauto_idragprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IDragProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDragProvider interface


## -description


Enables a Microsoft UI Automation element to describe itself as an element that can be dragged as part of a drag-and-drop operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDragProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDragProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDragProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B56F5975-279C-48C7-84C9-35BBBE222F6A">GetGrabbedItems</a>
</td>
<td align="left" width="63%">
Retrieves the collection of elements that are being dragged as part of a drag operation.  

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDragProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90850574-83EA-4291-99D0-391D8CACFE9F">DropEffect</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/66DEC1A0-5AB4-41C7-AA7A-F512AE388999">DropEffects</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an array of localized strings that enumerate the  full set of effects that can happen when this element is dropped as part of a drag-and-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/E2A472A0-F9CE-4778-96DD-60B00D53EEA6">IsGrabbed</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element has been grabbed as part of a drag-and-drop operation.

</td>
</tr>
</table> 


## -remarks



A provider can implement <b>IDragProvider</b> only on the element being dragged, or it can use an intermediary drag object that implements <b>IDragProvider</b>, in addition to the <b>IDragProvider</b> implementation on the individual element.  The intermediary is responsible for firing all events, which enables the provider to support dragging multiple elements at once, and to describe the multi-element drag operation with a single set of drag properties and events.




## -see-also




<a href="https://msdn.microsoft.com/ECCDC429-4829-46E0-AE77-270024E2DA48">IDropTargetProvider</a>



<a href="https://msdn.microsoft.com/FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE">UI Automation Support for Drag-and-Drop</a>
 

 

