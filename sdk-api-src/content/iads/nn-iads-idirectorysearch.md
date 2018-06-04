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

# IDirectorySearch interface


## -description


The <b>IDirectorySearch</b> interface is a pure COM interface that provides a low overhead method that non-Automation clients can use to perform queries in the underlying directory.

Of the ADSI system-supplied providers, only the LDAP provider supports this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectorySearch</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectorySearch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectorySearch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf220625-0aac-42ce-a15f-c44766693cf8">AbandonSearch</a>
</td>
<td align="left" width="63%">
Abandons a search already in process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a233c67b-4747-4417-bec8-86b27147863c">CloseSearchHandle</a>
</td>
<td align="left" width="63%">
Releases the search result from memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">ExecuteSearch</a>
</td>
<td align="left" width="63%">
Executes an individual search.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e75429-d22c-490f-a1f7-d771628067c9">FreeColumn</a>
</td>
<td align="left" width="63%">
Frees the  <a href="https://msdn.microsoft.com/9fdb370d-9409-4717-ae10-bb3b5b8a0e02">ADS_SEARCH_COLUMN</a> structure created by the  <a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">GetColumn</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">GetColumn</a>
</td>
<td align="left" width="63%">
Gets the item in a specified column from the current row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99ece6d1-3963-40bc-993e-f03aa9039c2d">GetFirstRow</a>
</td>
<td align="left" width="63%">
Gets the first row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3d95cc6-02f0-4a51-8dc5-4007cc8c63c8">GetNextColumnName</a>
</td>
<td align="left" width="63%">
Gets the name of the next column of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fb0b765-0162-418d-b0cd-7e9b1b53e1b9">GetNextRow</a>
</td>
<td align="left" width="63%">
Gets the next row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fccc9763-c64d-474b-a0c0-9bc9d4e34d65">GetPreviousRow</a>
</td>
<td align="left" width="63%">
Gets the previous row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">SetSearchPreference</a>
</td>
<td align="left" width="63%">
Sets options for conducting a search.

</td>
</tr>
</table> 

