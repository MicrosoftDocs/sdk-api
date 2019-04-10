---
UID: NN:uiautomationclient.IUIAutomationTreeWalker
title: IUIAutomationTreeWalker (uiautomationclient.h)
author: windows-sdk-content
description: Exposes properties and methods that UI Automation client applications use to view and navigate the UI Automation elements on the desktop.
old-location: winauto\uiauto_IUIAutomationTreeWalker.htm
tech.root: WinAuto
ms.assetid: adb4afed-63b9-42b4-8a8d-673d4813bb52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationTreeWalker, IUIAutomationTreeWalker interface [Windows Accessibility], IUIAutomationTreeWalker interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTreeWalker, uiauto_IUIAutomationTreeWalker, uiautomationclient/IUIAutomationTreeWalker, winauto.uiauto_IUIAutomationTreeWalker
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
 - IUIAutomationTreeWalker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTreeWalker interface


## -description


Exposes properties and methods that UI Automation client applications use to view and navigate the UI Automation elements on the desktop. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTreeWalker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTreeWalker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTreeWalker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f1df27c-664b-451a-8a1f-e4dbc70b1845">GetFirstChildElement</a>
</td>
<td align="left" width="63%">
Retrieves the first child element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42bdc6c4-8ee5-4338-aba1-9740221786c8">GetFirstChildElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the first child element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e59d8f6-1540-4077-9e0e-f75bf8846da9">GetLastChildElement</a>
</td>
<td align="left" width="63%">
Retrieves the last child element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a52172c-76d9-4ab7-98db-c880b2d11f68">GetLastChildElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the last child element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1e42cb4-0b87-42c2-9ea5-67630c0b895a">GetNextSiblingElement</a>
</td>
<td align="left" width="63%">
Retrieves the next sibling element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71c29a02-11fa-41ee-816e-cb3a0bea3025">GetNextSiblingElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the next sibling element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaff4d83-a614-4559-a357-dc2d241ecf67">GetParentElement</a>
</td>
<td align="left" width="63%">
Retrieves the parent element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a1d9805-bcd7-4c5d-ac61-138ac75a523e">GetParentElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the parent element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e05f421-d037-4d3b-908e-44ddd818a3f1">GetPreviousSiblingElement</a>
</td>
<td align="left" width="63%">
Retrieves the previous sibling element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09350915-0620-4c51-a4b5-25aa247d8241">GetPreviousSiblingElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the previous sibling element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62616711-a841-4273-8e38-0d2344659d03">NormalizeElement</a>
</td>
<td align="left" width="63%">
Retrieves the ancestor element nearest to the specified UI Automation element in the tree view. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62306545-1c5f-48ab-87c3-35bb6c3d94fa">NormalizeElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the ancestor element nearest to the specified UI Automation element in the tree view, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTreeWalker</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e62989ac-6fcf-4648-9b81-40b508ceae71">Condition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the condition that defines the view of the UI Automation tree.

</td>
</tr>
</table> 


## -remarks



UI Automation clients view the elements on the desktop as a set of <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> objects arranged in a tree structure. Using the <b>IUIAutomationTreeWalker</b> interface, a client application can navigate by selecting a view of the tree and stepping from one element to another in a specified direction using methods such as <a href="https://msdn.microsoft.com/2f1df27c-664b-451a-8a1f-e4dbc70b1845">GetFirstChildElement</a> and <a href="https://msdn.microsoft.com/a1e42cb4-0b87-42c2-9ea5-67630c0b895a">GetNextSiblingElement</a>.

Navigating the tree using <b>IUIAutomationTreeWalker</b> can result in cross-process calls and is not as efficient as locating an element using the <a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">IUIAutomationElement::FindAll</a> or <a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">IUIAutomationElement::FindFirst</a> methods.

If your client application might try to find elements in its own user interface, you must make all UI Automation calls on a separate thread.




## -see-also




<a href="https://msdn.microsoft.com/c976bf97-656b-4992-b0c5-f442b501ad75">CreateTreeWalker</a>



<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

