---
UID: NN:wabdefs.IMAPITable
title: IMAPITable (wabdefs.h)
author: windows-sdk-content
description: Do not use. This interface is used for content tables of Windows Address Book (WAB) containers and distribution lists.
old-location: wab\_wab_IMAPITable.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\imapitable\imapitable.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMAPITable, IMAPITable interface [Windows Address Book], IMAPITable interface [Windows Address Book],described, _wab_IMAPITable, wab._wab_IMAPITable, wabdefs/IMAPITable
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
<a href="https://msdn.microsoft.com/en-us/library/ms629475(v=VS.85).aspx">Abort</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629476(v=VS.85).aspx">Advise</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629477(v=VS.85).aspx">CollapseRow</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629478(v=VS.85).aspx">CreateBookmark</a>
</td>
<td align="left" width="63%">
Marks the current position of the table cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629479(v=VS.85).aspx">ExpandRow</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629480(v=VS.85).aspx">FindRow</a>
</td>
<td align="left" width="63%">
Finds the next row in a table that contains a property matching 
		the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629481(v=VS.85).aspx">FreeBookmark</a>
</td>
<td align="left" width="63%">
Frees a bookmark created by 
		<a href="https://msdn.microsoft.com/en-us/library/ms629478(v=VS.85).aspx">CreateBookmark</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629482(v=VS.85).aspx">GetCollapseState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629483(v=VS.85).aspx">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629484(v=VS.85).aspx">GetRowCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of rows in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629485(v=VS.85).aspx">GetStatus</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629487(v=VS.85).aspx">QueryColumns</a>
</td>
<td align="left" width="63%">
Retrieves either the current list of columns for a table view or 
		the full list of columns available for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629488(v=VS.85).aspx">QueryPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current table row position of the cursor, 
		if possible, and its fractional position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629489(v=VS.85).aspx">QueryRows</a>
</td>
<td align="left" width="63%">
Retrieves rows of data from a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629490(v=VS.85).aspx">QuerySortOrder</a>
</td>
<td align="left" width="63%">
Retrieves the current sort order for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629491(v=VS.85).aspx">Restrict</a>
</td>
<td align="left" width="63%">
Applies a restriction to a table, reducing the visible rows 
		to those matching the restriction criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629492(v=VS.85).aspx">SeekRow</a>
</td>
<td align="left" width="63%">
Moves the table cursor to a specific position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629493(v=VS.85).aspx">SeekRowApprox</a>
</td>
<td align="left" width="63%">
Moves the cursor to an approximate position 
		in the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629494(v=VS.85).aspx">SetCollapseState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629495(v=VS.85).aspx">SetColumns</a>
</td>
<td align="left" width="63%">
Sets the order of property values returned by query operations.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629496(v=VS.85).aspx">SortTable</a>
</td>
<td align="left" width="63%">
Sorts the table rows according to the criteria provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629497(v=VS.85).aspx">Unadvise</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629498(v=VS.85).aspx">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

