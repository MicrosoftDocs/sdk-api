---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAutomationTableItemPattern interface


## -description


Provides access to a  child element in a container that supports <a href="https://msdn.microsoft.com/a393b323-31f9-4f31-abdb-7a0fb7c8ab96">IUIAutomationTablePattern</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTableItemPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTableItemPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTableItemPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40d4c31b-643f-479b-859c-3458d2d17f19">GetCachedColumnHeaderItems</a>
</td>
<td align="left" width="63%">
Retrieves the cached column headers associated with a table item or cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69d4a632-8e35-4569-8c14-f56e9fd84c34">GetCachedRowHeaderItems</a>
</td>
<td align="left" width="63%">
Retrieves the cached row headers associated with a table item or cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccacd62c-c3f5-46a2-9449-5eb881f213b0">GetCurrentColumnHeaderItems</a>
</td>
<td align="left" width="63%">
Retrieves the column headers associated with a table item or cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ae074c6-1855-4aea-845c-284a7bbc3f3f">GetCurrentRowHeaderItems</a>
</td>
<td align="left" width="63%">
Retrieves the row headers associated with a table item or cell.

</td>
</tr>
</table> 


## -remarks



Elements that support this interface must also support <a href="https://msdn.microsoft.com/03b284de-3079-4543-ac5a-a8504da0d755">IUIAutomationGridItemPattern</a>, to provide properties that are not specific to tables.
	




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

