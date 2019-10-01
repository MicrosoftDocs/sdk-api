---
UID: NN:wabdefs.IDistList
title: IDistList (wabdefs.h)
author: windows-sdk-content
description: Do not use. This interface is used to provide access to distribution lists in modifiable address book containers. The interface provides methods to create, copy, and delete distribution lists, in addition to performing name resolution.
old-location: wab\_wab_IDistList.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\idistlist\idistlist.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDistList, IDistList interface [Windows Address Book], IDistList interface [Windows Address Book],described, _wab_IDistList, wab._wab_IDistList, wabdefs/IDistList
ms.topic: interface
f1_keywords: 
 - "wabdefs/IDistList"
req.header: wabdefs.h
req.include-header: Wabtmp.h
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
 - IDistList
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IDistList interface


## -description


Do not use. This interface is used to provide access to distribution lists in modifiable address book containers. The interface provides methods to create, copy, and delete distribution lists, in addition to performing name resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDistList</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/office/developer/office-2007/cc839817(v=office.12)">IMAPIContainer</a>. <b>IDistList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDistList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-copyentries">CopyEntries</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-copyprops">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-createentry">CreateEntry</a>
</td>
<td align="left" width="63%">
Creates a new entry in the distribution list container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-deleteentries">DeleteEntries</a>
</td>
<td align="left" width="63%">
Removes one or more entries from the distribution list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-deleteprops">DeleteProps</a>
</td>
<td align="left" width="63%">
Deletes property values from a distribution list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getcontentstable">GetContentsTable</a>
</td>
<td align="left" width="63%">
Retrieves the address of the contents table of the distribution list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-gethierarchytable">GetHierarchyTable</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getidsfromnames">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Retrieves the property identifiers that correspond to one or more property names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getlasterror">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getnamesfromids">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getproplist">GetPropList</a>
</td>
<td align="left" width="63%">
Retrieves a list of the object property tags.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getprops">GetProps</a>
</td>
<td align="left" width="63%">
Retrieves the property tag information for the distribution list items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-getsearchcriteria">GetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-openentry">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens an entry from the distribution list and returns a pointer to the object to provide further access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-openproperty">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-resolvenames">ResolveNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-savechanges">SaveChanges</a>
</td>
<td align="left" width="63%">
Provides the ability to save changes to the open distribution list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-setprops">SetProps</a>
</td>
<td align="left" width="63%">
Sets property values for a distribution list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-idistlist-setsearchcriteria">SetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

