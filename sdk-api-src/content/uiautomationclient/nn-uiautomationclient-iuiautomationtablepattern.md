---
UID: NN:uiautomationclient.IUIAutomationTablePattern
title: IUIAutomationTablePattern
author: windows-sdk-content
description: Provides access to a control that acts as a container for a collection of child elements.
old-location: winauto\uiauto_IUIAutomationTablePattern.htm
old-project: WinAuto
ms.assetid: a393b323-31f9-4f31-abdb-7a0fb7c8ab96
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IUIAutomationTablePattern, IUIAutomationTablePattern interface [Windows Accessibility], IUIAutomationTablePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTablePattern, uiauto_IUIAutomationTablePattern, uiautomationclient/IUIAutomationTablePattern, winauto.uiauto_IUIAutomationTablePattern
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
 - IUIAutomationTablePattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTablePattern interface


## -description


Provides access to a control that acts as a container for a collection of child elements. The children of this element support <a href="https://msdn.microsoft.com/8e9948ec-7c31-45dd-ac9f-e9eafed9d2db">IUIAutomationTableItemPattern</a> and are organized in a two-dimensional logical coordinate system that can be traversed by row and column.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTablePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTablePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTablePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/817a13b3-6de5-4473-8286-e3d728d06819">GetCachedColumnHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a cached collection of UI Automation elements representing all the column headers in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2487f6cd-5871-457d-b634-83bb6191dce2">GetCachedRowHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a cached collection of UI Automation elements representing all the row headers in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f31bfa6-0a4a-4cd6-9f5d-2964696d4acd">GetCurrentColumnHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a collection of UI Automation elements representing all the column headers in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5669bdc7-a240-4c05-acf1-b1ff5e5b09fc">GetCurrentRowHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a collection of UI Automation elements representing all the row headers in a table.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTablePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/510917f9-43bf-4891-bae7-7e5ae7607092">CachedRowOrColumnMajor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached primary direction of traversal for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/abf2bbfd-2052-4ece-bf28-be836af407ff">CurrentRowOrColumnMajor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the primary direction of traversal for the table.

</td>
</tr>
</table> 


## -remarks



This control pattern is analogous to <a href="https://msdn.microsoft.com/36a4893e-5f49-413c-a29a-e58291c7d057">IUIAutomationGridPattern</a> with the distinction that any control that supports <b>IUIAutomationTablePattern</b> also exposes a column or row header relationship, or both, for each child element. Controls that support the <a href="https://msdn.microsoft.com/e00c7a58-410c-4818-8f61-57ee98527d6e">Table</a> control pattern also support the <a href="https://msdn.microsoft.com/c50fb6f7-884a-4147-a6b2-c59d787fc04b">Grid</a> control pattern in order to provide access to the inherent grid functionality of a table.




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

