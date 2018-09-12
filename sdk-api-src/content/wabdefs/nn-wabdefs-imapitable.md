---
UID: NN:wabdefs.IMAPITable
title: IMAPITable
author: windows-sdk-content
description: Do not use. This interface is used for content tables of Windows Address Book (WAB) containers and distribution lists.
old-location: wab\_wab_IMAPITable.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\imapitable\imapitable.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMAPITable, IMAPITable interface [Windows Address Book], IMAPITable interface [Windows Address Book],described, _wab_IMAPITable, wab._wab_IMAPITable, wabdefs/IMAPITable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IMAPITable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IMAPITable interface


## -description


Do not use. This interface is used for content tables of Windows Address Book (WAB) containers and distribution lists.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMAPITable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMAPITable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMAPITable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff7c7a2f-0ccb-47e6-bd51-4f5635ca11fe">Abort</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1738e4f3-3767-42c2-97d8-0e276c0c2e4c">Advise</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b970416-fcdb-40f9-b977-cd5b36e10408">CollapseRow</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed6f9cb1-a4f2-4288-983a-888317175cdf">CreateBookmark</a>
</td>
<td align="left" width="63%">
Marks the current position of the table cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4f0c9ba-d61c-4ea8-bcb2-e47dd8c4d387">ExpandRow</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df614edc-b4db-40b3-9f73-1ec95d381d8b">FindRow</a>
</td>
<td align="left" width="63%">
Finds the next row in a table that contains a property matching 
		the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/489bca9a-1a93-4764-a25c-2237020730c8">FreeBookmark</a>
</td>
<td align="left" width="63%">
Frees a bookmark created by 
		<a href="https://msdn.microsoft.com/ed6f9cb1-a4f2-4288-983a-888317175cdf">CreateBookmark</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d576b6e-9286-42d9-abb4-be514ee20374">GetCollapseState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c29a50a8-eaed-48fe-8351-fac0bb15b762">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f40ad94-4cff-41a0-88ac-af367b5df01c">GetRowCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of rows in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77bcb1b7-4cee-4c4d-b2fe-6ced3d80c49a">GetStatus</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd08a2e8-6687-4066-9181-84e9a655bd3d">QueryColumns</a>
</td>
<td align="left" width="63%">
Retrieves either the current list of columns for a table view or 
		the full list of columns available for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/641c5523-7663-4ee9-b705-f7341b3dee9e">QueryPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current table row position of the cursor, 
		if possible, and its fractional position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b6d2fff-9df7-4d89-b59e-cf507eafb7b7">QueryRows</a>
</td>
<td align="left" width="63%">
Retrieves rows of data from a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da530852-596c-4b0e-9058-1c79cb7fb6b6">QuerySortOrder</a>
</td>
<td align="left" width="63%">
Retrieves the current sort order for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcefd7e9-ec02-445d-9991-2cce54e21efa">Restrict</a>
</td>
<td align="left" width="63%">
Applies a restriction to a table, reducing the visible rows 
		to those matching the restriction criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ae97111-99db-45c3-8098-be027aab492e">SeekRow</a>
</td>
<td align="left" width="63%">
Moves the table cursor to a specific position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a14e4c10-93fd-4654-a530-4d7959744af7">SeekRowApprox</a>
</td>
<td align="left" width="63%">
Moves the cursor to an approximate position 
		in the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50d20e00-a201-4940-babb-588b223a9d32">SetCollapseState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce04f951-1ad8-4d6a-87fa-a37f49c93e1a">SetColumns</a>
</td>
<td align="left" width="63%">
Sets the order of property values returned by query operations.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c316e4f-bbea-4da2-9d16-f89d6e6da767">SortTable</a>
</td>
<td align="left" width="63%">
Sorts the table rows according to the criteria provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3ab9b7f-e63c-44cb-9e24-61a6f33e8a35">Unadvise</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4000100e-2d5f-49fa-bb05-cbd0a8434595">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

