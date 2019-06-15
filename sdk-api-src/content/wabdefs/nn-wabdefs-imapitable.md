---
UID: NN:wabdefs.IMAPITable
title: IMAPITable (wabdefs.h)
author: windows-sdk-content
description: Do not use. This interface is used for content tables of Windows Address Book (WAB) containers and distribution lists.
old-location: wab\_wab_IMAPITable.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\imapitable\imapitable.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# IMAPITable interface


## -description


Do not use. This interface is used for content tables of Windows Address Book (WAB) containers and distribution lists.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMAPITable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMAPITable</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions//ms629475(v=vs.85)">Abort</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629476(v=vs.85)">Advise</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629477(v=vs.85)">CollapseRow</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629478(v=vs.85)">CreateBookmark</a>
</td>
<td align="left" width="63%">
Marks the current position of the table cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629479(v=vs.85)">ExpandRow</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629480(v=vs.85)">FindRow</a>
</td>
<td align="left" width="63%">
Finds the next row in a table that contains a property matching 
		the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629481(v=vs.85)">FreeBookmark</a>
</td>
<td align="left" width="63%">
Frees a bookmark created by 
		<a href="https://docs.microsoft.com/previous-versions//ms629478(v=vs.85)">CreateBookmark</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629482(v=vs.85)">GetCollapseState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629483(v=vs.85)">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629484(v=vs.85)">GetRowCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of rows in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629485(v=vs.85)">GetStatus</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629487(v=vs.85)">QueryColumns</a>
</td>
<td align="left" width="63%">
Retrieves either the current list of columns for a table view or 
		the full list of columns available for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629488(v=vs.85)">QueryPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current table row position of the cursor, 
		if possible, and its fractional position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629489(v=vs.85)">QueryRows</a>
</td>
<td align="left" width="63%">
Retrieves rows of data from a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629490(v=vs.85)">QuerySortOrder</a>
</td>
<td align="left" width="63%">
Retrieves the current sort order for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629491(v=vs.85)">Restrict</a>
</td>
<td align="left" width="63%">
Applies a restriction to a table, reducing the visible rows 
		to those matching the restriction criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629492(v=vs.85)">SeekRow</a>
</td>
<td align="left" width="63%">
Moves the table cursor to a specific position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629493(v=vs.85)">SeekRowApprox</a>
</td>
<td align="left" width="63%">
Moves the cursor to an approximate position 
		in the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629494(v=vs.85)">SetCollapseState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629495(v=vs.85)">SetColumns</a>
</td>
<td align="left" width="63%">
Sets the order of property values returned by query operations.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629496(v=vs.85)">SortTable</a>
</td>
<td align="left" width="63%">
Sorts the table rows according to the criteria provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629497(v=vs.85)">Unadvise</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms629498(v=vs.85)">WaitForCompletion</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

