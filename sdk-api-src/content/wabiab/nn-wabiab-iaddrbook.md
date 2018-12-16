---
UID: NN:wabiab.IAddrBook
title: IAddrBook
author: windows-sdk-content
description: Do not use.
old-location: wab\_wab_IAddrBook.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iaddrbook\iaddrbook.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAddrBook, IAddrBook interface [Windows Address Book], IAddrBook interface [Windows Address Book],described, _wab_IAddrBook, wab._wab_IAddrBook, wabiab/IAddrBook
ms.topic: interface
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
---

# IAddrBook interface


## -description


Do not use. This interface supports access to the Windows Address Book (WAB) and includes operations such as displaying common dialog boxes, opening containers, messaging users (contacts) and distribution lists (groups) in the address book, and performing name resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAddrBook</b> interface inherits from <a href="https://msdn.microsoft.com/library/Cc815525(v=office.12).aspx">IMAPIProp</a>. <b>IAddrBook</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms629532(v=VS.85).aspx">Address</a>
</td>
<td align="left" width="63%">
Displays the common address book dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629533(v=VS.85).aspx">Advise</a>
</td>
<td align="left" width="63%">
Registers the caller with the WAB to receive notifications.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629534(v=VS.85).aspx">CompareEntryIDs</a>
</td>
<td align="left" width="63%">
Compares two entry identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629535(v=VS.85).aspx">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629637(v=VS.85).aspx">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629638(v=VS.85).aspx">CreateOneOff</a>
</td>
<td align="left" width="63%">
Creates an entry identifier for a <a href="https://docs.microsoft.com/">one-off</a> address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629639(v=VS.85).aspx">DeleteProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629640(v=VS.85).aspx">Details</a>
</td>
<td align="left" width="63%">
Displays a dialog box that shows details, and allows editing, 
		of a particular entry in the WAB.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629641(v=VS.85).aspx">GetDefaultDir</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629642(v=VS.85).aspx">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629643(v=VS.85).aspx">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629644(v=VS.85).aspx">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629645(v=VS.85).aspx">GetPAB</a>
</td>
<td align="left" width="63%">
Returns the entry identifier of the default WAB container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629646(v=VS.85).aspx">GetPropList</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629647(v=VS.85).aspx">GetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629648(v=VS.85).aspx">GetSearchPath</a>
</td>
<td align="left" width="63%">
Returns an ordered list of the entry identifiers of containers 
		to be included in the name resolution process initiated by the 
		<a href="https://msdn.microsoft.com/en-us/library/ms629656(v=VS.85).aspx">ResolveName</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629650(v=VS.85).aspx">NewEntry</a>
</td>
<td align="left" width="63%">
Displays a blank dialog box that enables the user to create a new entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629651(v=VS.85).aspx">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens a container or mail user object and returns a pointer 
		to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629652(v=VS.85).aspx">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629653(v=VS.85).aspx">PrepareRecips</a>
</td>
<td align="left" width="63%">
Prepares a recipient list for later use by the messaging system.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629654(v=VS.85).aspx">QueryDefaultRecipOpt</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629655(v=VS.85).aspx">RecipOptions</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629656(v=VS.85).aspx">ResolveName</a>
</td>
<td align="left" width="63%">
Resolves a partial recipient list to full addresses.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629657(v=VS.85).aspx">SaveChanges</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629658(v=VS.85).aspx">SetDefaultDir</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629660(v=VS.85).aspx">SetPAB</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629662(v=VS.85).aspx">SetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629665(v=VS.85).aspx">SetSearchPath</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629668(v=VS.85).aspx">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters the caller from the WAB 
		for notifications.

</td>
</tr>
</table> 

