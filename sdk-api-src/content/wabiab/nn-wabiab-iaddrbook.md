---
UID: NN:wabiab.IAddrBook
title: IAddrBook (wabiab.h)
author: windows-sdk-content
description: Do not use.
old-location: wab\_wab_IAddrBook.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iaddrbook\iaddrbook.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAddrBook, IAddrBook interface [Windows Address Book], IAddrBook interface [Windows Address Book],described, _wab_IAddrBook, wab._wab_IAddrBook, wabiab/IAddrBook
ms.topic: interface
f1_keywords: ["wabiab/IAddrBook"]
req.header: wabiab.h
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
 - IAddrBook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IAddrBook interface


## -description


Do not use. This interface supports access to the Windows Address Book (WAB) and includes operations such as displaying common dialog boxes, opening containers, messaging users (contacts) and distribution lists (groups) in the address book, and performing name resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAddrBook</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/office/developer/office-2007/cc815525(v=office.12)">IMAPIProp</a>. <b>IAddrBook</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAddrBook</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629532(v=vs.85)">Address</a>
</td>
<td align="left" width="63%">
Displays the common address book dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629533(v=vs.85)">Advise</a>
</td>
<td align="left" width="63%">
Registers the caller with the WAB to receive notifications.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629534(v=vs.85)">CompareEntryIDs</a>
</td>
<td align="left" width="63%">
Compares two entry identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-copyprops">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629638(v=vs.85)">CreateOneOff</a>
</td>
<td align="left" width="63%">
Creates an entry identifier for a <a href="https://docs.microsoft.com/">one-off</a> address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-deleteprops">DeleteProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629640(v=vs.85)">Details</a>
</td>
<td align="left" width="63%">
Displays a dialog box that shows details, and allows editing, 
		of a particular entry in the WAB.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629641(v=vs.85)">GetDefaultDir</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-getidsfromnames">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-getlasterror">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-getnamesfromids">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629645(v=vs.85)">GetPAB</a>
</td>
<td align="left" width="63%">
Returns the entry identifier of the default WAB container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-getproplist">GetPropList</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-getprops">GetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629648(v=vs.85)">GetSearchPath</a>
</td>
<td align="left" width="63%">
Returns an ordered list of the entry identifiers of containers 
		to be included in the name resolution process initiated by the 
		<a href="https://docs.microsoft.com/previous-versions/ms629656(v=vs.85)">ResolveName</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629650(v=vs.85)">NewEntry</a>
</td>
<td align="left" width="63%">
Displays a blank dialog box that enables the user to create a new entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629651(v=vs.85)">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens a container or mail user object and returns a pointer 
		to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-openproperty">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629653(v=vs.85)">PrepareRecips</a>
</td>
<td align="left" width="63%">
Prepares a recipient list for later use by the messaging system.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629654(v=vs.85)">QueryDefaultRecipOpt</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629655(v=vs.85)">RecipOptions</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629656(v=vs.85)">ResolveName</a>
</td>
<td align="left" width="63%">
Resolves a partial recipient list to full addresses.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-savechanges">SaveChanges</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629658(v=vs.85)">SetDefaultDir</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629660(v=vs.85)">SetPAB</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-iaddrbook-setprops">SetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629665(v=vs.85)">SetSearchPath</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms629668(v=vs.85)">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters the caller from the WAB 
		for notifications.

</td>
</tr>
</table> 

