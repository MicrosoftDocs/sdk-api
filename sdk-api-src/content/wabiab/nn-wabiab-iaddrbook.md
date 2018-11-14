---
UID: NN:wabiab.IAddrBook
title: IAddrBook
author: windows-sdk-content
description: Do not use.
old-location: wab\_wab_IAddrBook.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iaddrbook\iaddrbook.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAddrBook, IAddrBook interface [Windows Address Book], IAddrBook interface [Windows Address Book],described, _wab_IAddrBook, wab._wab_IAddrBook, wabiab/IAddrBook
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAddrBook</b> interface inherits from <a href="3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5">IMAPIProp</a>. <b>IAddrBook</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b2d899bd-64d4-4ec1-8866-8c757f3f5e04">Address</a>
</td>
<td align="left" width="63%">
Displays the common address book dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8992858e-604e-44dd-8983-1e8bae2ea1fe">Advise</a>
</td>
<td align="left" width="63%">
Registers the caller with the WAB to receive notifications.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e5a657f-dcf5-4286-b626-782df8aa9526">CompareEntryIDs</a>
</td>
<td align="left" width="63%">
Compares two entry identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f292fb4-deb4-4bb9-8ebd-c4da1574cea2">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f65bf1c-2bb4-434b-b68f-2bec6fb2ce79">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4409e758-4337-423c-b1d5-5feb22073a74">CreateOneOff</a>
</td>
<td align="left" width="63%">
Creates an entry identifier for a <a href="https://docs.microsoft.com/">one-off</a> address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73142d49-4f70-4e1d-bd71-41aac4d342f7">DeleteProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/818af9a4-d2d4-4238-9665-68296d4a335f">Details</a>
</td>
<td align="left" width="63%">
Displays a dialog box that shows details, and allows editing, 
		of a particular entry in the WAB.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb431c6d-d3c4-46f2-805e-5672934511a4">GetDefaultDir</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17525838-5921-478f-b5f9-1e3d0679a458">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c7ed99-c6ce-4940-b6ec-a1a7b7f3dd8d">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13afdb2b-3f1e-43f0-9d41-4a040c38868f">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b006d63-6a45-4dc5-8c41-b1b1f1089644">GetPAB</a>
</td>
<td align="left" width="63%">
Returns the entry identifier of the default WAB container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12b9a6bc-8ed6-4ca2-94f8-1fb38e467152">GetPropList</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4f635fd-bebb-4cbf-a4b5-98125d88ecad">GetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dfcdb62-c02a-4ad6-b573-b87b0755fcdd">GetSearchPath</a>
</td>
<td align="left" width="63%">
Returns an ordered list of the entry identifiers of containers 
		to be included in the name resolution process initiated by the 
		<a href="https://msdn.microsoft.com/597516a6-96ce-4362-ba1c-2ab9ba94eb30">ResolveName</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d531f730-1f48-40d2-9e1a-093ce3add2f4">NewEntry</a>
</td>
<td align="left" width="63%">
Displays a blank dialog box that enables the user to create a new entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58c1d80f-2b5d-4762-af5f-e95fa99ac69d">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens a container or mail user object and returns a pointer 
		to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e98bf9a4-9bbf-4299-8eca-3ae300018ff5">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/019ab137-4611-459e-ac0d-37c208927a98">PrepareRecips</a>
</td>
<td align="left" width="63%">
Prepares a recipient list for later use by the messaging system.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a025255-7379-4181-a00c-3bdb78af1e1d">QueryDefaultRecipOpt</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1343e49-d8ae-44d6-943a-4430da1b68f8">RecipOptions</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/597516a6-96ce-4362-ba1c-2ab9ba94eb30">ResolveName</a>
</td>
<td align="left" width="63%">
Resolves a partial recipient list to full addresses.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d0711df-608e-4985-a6d1-a766d230c461">SaveChanges</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2247e3f-2905-4070-86d7-225d5402f423">SetDefaultDir</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59040f77-727c-42d4-b8ac-9b868eb9ba68">SetPAB</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c26b5d2-4f1a-4e67-b41e-98d7d3f5953b">SetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cd50a0b-a5ef-48b6-93b1-bea56f1e6dec">SetSearchPath</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/856622b1-7839-4559-966e-5004974ae4c6">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters the caller from the WAB 
		for notifications.

</td>
</tr>
</table> 

