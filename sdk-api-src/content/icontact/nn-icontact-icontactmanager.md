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

