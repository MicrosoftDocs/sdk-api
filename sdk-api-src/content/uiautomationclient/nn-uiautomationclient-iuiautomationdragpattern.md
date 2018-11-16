---
UID: NN:uiautomationclient.IUIAutomationDragPattern
title: IUIAutomationDragPattern
author: windows-sdk-content
description: Provides access to information exposed by a UI Automation provider for an element that can be dragged as part of a drag-and-drop operation.
old-location: winauto\uiauto_iuiautomationdragpattern.htm
tech.root: WinAuto
ms.assetid: F7768A87-3981-48E0-A72D-BEA14C189E6E
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAutomationDragPattern, IUIAutomationDragPattern interface [Windows Accessibility], IUIAutomationDragPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationDragPattern, winauto.uiauto_iuiautomationdragpattern
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationDragPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationDragPattern interface


## -description


Provides access to information exposed by a UI Automation provider for an element that can be dragged as part of a drag-and-drop operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationDragPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationDragPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationDragPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A3CB19E9-634D-4023-926E-BAA717DE4528">GetCachedGrabbedItems</a>
</td>
<td align="left" width="63%">
Retrieves a cached collection of elements that represent the full set of items that the user is dragging as part of a drag operation.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9311E1E3-FE4E-428F-9DAD-32AE347477EF">GetCurrentGrabbedItems</a>
</td>
<td align="left" width="63%">
Retrieves a collection of elements that represent the full set of items that the user is dragging as part of a drag operation.  

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationDragPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/A99F5E0F-FC61-4AD7-9DC8-B4B7B1AB2F6C">CachedDropEffect</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached localized string that indicates what happens when the user drops this element as part of a drag-and-drop operation.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/FDE2A5CA-1353-466E-A28C-E317059AEA54">CachedDropEffects</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached array of localized strings that enumerate the  full set of effects that can happen when the user drops this element as part of a drag-and-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/DA63B155-56FC-49EE-99EA-56288CC7F8E9">CachedIsGrabbed</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether this element has been grabbed as part of a drag-and-drop operation.



</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8F5459DE-4BAA-412D-88E9-A81125150CAA">CurrentDropEffect</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a localized string that indicates what happens when the user drops this element as part of a drag-drop operation.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/393692C9-AA4E-4C50-8006-39457EB57153">CurrentDropEffects</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an array of localized strings that enumerate the  full set of effects that can happen when this element  as part of a drag-and-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4A528EA2-4E0D-458B-9EC1-ACF5964F0874">CurrentIsGrabbed</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the user has grabbed this element as part of a drag-and-drop operation.

</td>
</tr>
</table> 


## -remarks



Microsoft UI Automation clients use this interface to access the dragging properties and functionality of a control or UI element that the user can drag-and-drop on a drop target.




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>



<a href="https://msdn.microsoft.com/FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE">UI Automation Support for Drag-and-Drop</a>
 

 

