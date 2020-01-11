---
UID: NN:wabdefs.IABContainer
title: IABContainer (wabdefs.h)
description: Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients.
old-location: wab\_wab_IABContainer.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iabcontainer\iabcontainer.htm
ms.date: 12/05/2018
ms.keywords: IABContainer, IABContainer interface [Windows Address Book], IABContainer interface [Windows Address Book],described, _wab_IABContainer, wab._wab_IABContainer, wabdefs/IABContainer
f1_keywords:
- wabdefs/IABContainer
dev_langs:
- c++
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
- IABContainer
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IABContainer interface


## -description


Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IABContainer</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/office/developer/office-2007/cc839817(v=office.12)">IMAPIContainer</a>. <b>IABContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IABContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629670(v=vs.85)">CopyEntries</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-copyprops">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629676(v=vs.85)">CreateEntry</a>
</td>
<td align="left" width="63%">
Creates a new entry in the address book container.  The WAB supports creation of mail users and distribution lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-deleteentries">DeleteEntries</a>
</td>
<td align="left" width="63%">
Removes one or more entries from the address book container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-deleteprops">DeleteProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getcontentstable">GetContentsTable</a>
</td>
<td align="left" width="63%">
Retrieves the address of the contents table of the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-gethierarchytable">GetHierarchyTable</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getidsfromnames">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getlasterror">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getnamesfromids">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getproplist">GetPropList</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getprops">GetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-getsearchcriteria">GetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-openentry">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens a child container object in the open container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-openproperty">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-resolvenames">ResolveNames</a>
</td>
<td align="left" width="63%">
Resolves entries against the address book container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-savechanges">SaveChanges</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-setprops">SetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iabcontainer-setsearchcriteria">SetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

