---
UID: NN:icontact.IContactManager
title: IContactManager (icontact.h)
author: windows-sdk-content
description: Do not use. Used for retrieving a contact, based on a contact ID string.
old-location: wincontacts\_wincontacts_IContactManager.htm
tech.root: wincontacts
ms.assetid: d0102659-488c-45db-931b-345013e21eed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IContactManager, IContactManager interface [Windows Contacts], IContactManager interface [Windows Contacts],described, _wincontacts_IContactManager, icontact/IContactManager, wincontacts._wincontacts_IContactManager
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
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContactManager interface


## -description


Do not use. Used for retrieving a contact, based on a contact ID string. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContactManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-getcontactcollection">GetContactCollection</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactcollection">IContactCollection</a> object that contains all known contacts. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-getmecontact">GetMeContact</a>
</td>
<td align="left" width="63%">
Retrieves the local user account concept of 'me'.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the contact manager with the unique application name and application version 
		being used to manipulate contacts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-load">Load</a>
</td>
<td align="left" width="63%">
Loads an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a> object with the data from the contact 
		referenced by the computer-local contact ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-mergecontactids">MergeContactIDs</a>
</td>
<td align="left" width="63%">
Makes an old Contact ID resolve to the same value as a new Contact ID. 
		Subsequent calls to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-load">Load</a> with the old contact ID 
		now loads the new contact ID contact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-setmecontact">SetMeContact</a>
</td>
<td align="left" width="63%">
Sets the local user account concept of 'me' to specified user.

</td>
</tr>
</table> 

