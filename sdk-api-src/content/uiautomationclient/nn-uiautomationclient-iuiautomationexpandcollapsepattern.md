---
UID: NN:uiautomationclient.IUIAutomationExpandCollapsePattern
title: IUIAutomationExpandCollapsePattern
author: windows-sdk-content
description: Provides access to a control that can visually expand to display content, and collapse to hide content.
old-location: winauto\uiauto_IUIAutomationExpandCollapsePattern.htm
tech.root: WinAuto
ms.assetid: 816c28a9-2486-403e-bfbd-94d040d0aac5
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IUIAutomationExpandCollapsePattern, IUIAutomationExpandCollapsePattern interface [Windows Accessibility], IUIAutomationExpandCollapsePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationExpandCollapsePattern, uiauto_IUIAutomationExpandCollapsePattern, uiautomationclient/IUIAutomationExpandCollapsePattern, winauto.uiauto_IUIAutomationExpandCollapsePattern
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
 - IUIAutomationExpandCollapsePattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationExpandCollapsePattern interface


## -description


Provides access to a control  that can visually expand to display content, and collapse to hide content.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationExpandCollapsePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationExpandCollapsePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationExpandCollapsePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9337d2dd-08db-4af7-ad65-e113811dd7ba">Collapse</a>
</td>
<td align="left" width="63%">
Hides all child nodes, controls, or content of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc21cffc-63fe-4c5d-9c4d-35e1bab67a7c">Expand</a>
</td>
<td align="left" width="63%">
Displays all child nodes, controls, or content of the element. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationExpandCollapsePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fa95dcb8-487b-49ef-b04d-8a84eb2334e0">CachedExpandCollapseState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates the state, expanded or collapsed, of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/abd21a19-c7a0-44db-ad5b-64c476efa400">CurrentExpandCollapseState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates the state, expanded or collapsed, of the element.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

