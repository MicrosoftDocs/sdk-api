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
f1_keywords: 
 - "uiautomationclient/IUIAutomationTreeWalker"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTreeWalker interface


## -description


Exposes properties and methods that UI Automation client applications use to view and navigate the UI Automation elements on the desktop. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTreeWalker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTreeWalker</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelement">GetFirstChildElement</a>
</td>
<td align="left" width="63%">
Retrieves the first child element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache">GetFirstChildElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the first child element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getlastchildelement">GetLastChildElement</a>
</td>
<td align="left" width="63%">
Retrieves the last child element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getlastchildelementbuildcache">GetLastChildElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the last child element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getnextsiblingelement">GetNextSiblingElement</a>
</td>
<td align="left" width="63%">
Retrieves the next sibling element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getnextsiblingelementbuildcache">GetNextSiblingElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the next sibling element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getparentelement">GetParentElement</a>
</td>
<td align="left" width="63%">
Retrieves the parent element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getparentelementbuildcache">GetParentElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the parent element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getprevioussiblingelement">GetPreviousSiblingElement</a>
</td>
<td align="left" width="63%">
Retrieves the previous sibling element of the specified UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getprevioussiblingelementbuildcache">GetPreviousSiblingElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the previous sibling element of the specified UI Automation element, and caches properties and control patterns.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement">NormalizeElement</a>
</td>
<td align="left" width="63%">
Retrieves the ancestor element nearest to the specified UI Automation element in the tree view. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelementbuildcache">NormalizeElementBuildCache</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-get_condition">Condition</a>


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



UI Automation clients view the elements on the desktop as a set of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a> objects arranged in a tree structure. Using the <b>IUIAutomationTreeWalker</b> interface, a client application can navigate by selecting a view of the tree and stepping from one element to another in a specified direction using methods such as <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelement">GetFirstChildElement</a> and <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getnextsiblingelement">GetNextSiblingElement</a>.

Navigating the tree using <b>IUIAutomationTreeWalker</b> can result in cross-process calls and is not as efficient as locating an element using the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">IUIAutomationElement::FindAll</a> or <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">IUIAutomationElement::FindFirst</a> methods.

If your client application might try to find elements in its own user interface, you must make all UI Automation calls on a separate thread.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createtreewalker">CreateTreeWalker</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
 

 

