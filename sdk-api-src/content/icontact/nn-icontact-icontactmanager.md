---
UID: NN:icontact.IContactManager
title: IContactManager
author: windows-sdk-content
description: Do not use. Used for retrieving a contact, based on a contact ID string.
old-location: wincontacts\_wincontacts_IContactManager.htm
old-project: wincontacts
ms.assetid: d0102659-488c-45db-931b-345013e21eed
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IContactManager, IContactManager interface [Windows Contacts], IContactManager interface [Windows Contacts],described, _wincontacts_IContactManager, icontact/IContactManager, wincontacts._wincontacts_IContactManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: icontact.h
req.include-header: Contact.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Icontact.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactManager
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactManager interface


## -description


Do not use. Used for retrieving a contact, based on a contact ID string. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContactManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContactManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b9d7ba5-e2cd-452f-8479-fdaad183b1ac">GetContactCollection</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897">IContactCollection</a> object that contains all known contacts. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fcf5700-399f-4388-9741-6be3b7aef6a9">GetMeContact</a>
</td>
<td align="left" width="63%">
Retrieves the local user account concept of 'me'.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the contact manager with the unique application name and application version 
		being used to manipulate contacts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9addc49-72fd-4b87-bf48-a2a09b1161e9">Load</a>
</td>
<td align="left" width="63%">
Loads an <a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a> object with the data from the contact 
		referenced by the computer-local contact ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a3aea59-ef92-4775-b942-7383a5e8a63c">MergeContactIDs</a>
</td>
<td align="left" width="63%">
Makes an old Contact ID resolve to the same value as a new Contact ID. 
		Subsequent calls to <a href="https://msdn.microsoft.com/d9addc49-72fd-4b87-bf48-a2a09b1161e9">Load</a> with the old contact ID 
		now loads the new contact ID contact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3922ea46-da14-44ad-a9bf-8a10480722da">SetMeContact</a>
</td>
<td align="left" width="63%">
Sets the local user account concept of 'me' to specified user.

</td>
</tr>
</table> 

