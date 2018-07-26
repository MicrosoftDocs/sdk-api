---
UID: NN:uiautomationclient.IUIAutomationSelectionItemPattern
title: IUIAutomationSelectionItemPattern
author: windows-sdk-content
description: Provides access to the selectable child items of a container control that supports IUIAutomationSelectionPattern.
old-location: winauto\uiauto_IUIAutomationSelectionItemPattern.htm
old-project: WinAuto
ms.assetid: b76d5003-b9af-4a48-91d3-8075f45cf131
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IUIAutomationSelectionItemPattern, IUIAutomationSelectionItemPattern interface [Windows Accessibility], IUIAutomationSelectionItemPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationSelectionItemPattern, uiauto_IUIAutomationSelectionItemPattern, uiautomationclient/IUIAutomationSelectionItemPattern, winauto.uiauto_IUIAutomationSelectionItemPattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationSelectionItemPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationSelectionItemPattern interface


## -description


Provides access to the selectable child items of a container control that supports <a href="https://msdn.microsoft.com/10e0c9c3-ed42-4ffa-b0a8-25a1c760a583">IUIAutomationSelectionPattern</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSelectionItemPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationSelectionItemPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationSelectionItemPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3d90861-1926-4294-b14b-f4c61a4f9176">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the current element to the collection of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25f9a8da-4bc9-496e-888c-a270a2bf8fb3">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes this element from the selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/676d3fef-77b8-4f02-9a89-a7471898598f">Select</a>
</td>
<td align="left" width="63%">
Clears any selected items and then selects the current element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSelectionItemPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dafa51b9-7dfd-46ad-89cc-8c3af3df8ea0">CachedIsSelected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A cached value that indicates whether this item is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/58664ca5-1188-44a5-99d8-741c08eaf3f3">CachedSelectionContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached element that supports <a href="https://msdn.microsoft.com/10e0c9c3-ed42-4ffa-b0a8-25a1c760a583">IUIAutomationSelectionPattern</a> and acts as the container for this item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5a81509b-b09b-482c-bf1f-5d85665c0d82">CurrentIsSelected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether this item is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e4e9ac5f-15d2-491f-9f23-3da7a5bf8fe2">CurrentSelectionContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the element that supports <a href="https://msdn.microsoft.com/10e0c9c3-ed42-4ffa-b0a8-25a1c760a583">IUIAutomationSelectionPattern</a> and acts as the container for this item.



</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

