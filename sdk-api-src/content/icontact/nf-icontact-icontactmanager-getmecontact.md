---
UID: NF:icontact.IContactManager.GetMeContact
title: IContactManager::GetMeContact (icontact.h)
author: windows-sdk-content
description: Retrieves the local user account concept of 'me'.
old-location: wincontacts\_wincontacts_IContactManager_GetMeContact.htm
tech.root: wincontacts
ms.assetid: 0fcf5700-399f-4388-9741-6be3b7aef6a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMeContact, GetMeContact method [Windows Contacts], GetMeContact method [Windows Contacts],IContactManager interface, IContactManager interface [Windows Contacts],GetMeContact method, IContactManager.GetMeContact, IContactManager::GetMeContact, _wincontacts_IContactManager_GetMeContact, icontact/IContactManager::GetMeContact, wincontacts._wincontacts_IContactManager_GetMeContact
ms.topic: method
f1_keywords: ["icontact/IContactManager.GetMeContact"]
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
 - IContactManager.GetMeContact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContactManager::GetMeContact


## -description


Retrieves the local user account concept of 'me'.


## -parameters




### -param ppMeContact [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a>**</b>

Specifies where to store a pointer to the 'me' contact.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Retrieval was successful. 

</td>
</tr>
</table>
 



