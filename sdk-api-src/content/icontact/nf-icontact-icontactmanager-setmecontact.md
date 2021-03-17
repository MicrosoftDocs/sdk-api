---
UID: NF:icontact.IContactManager.SetMeContact
title: IContactManager::SetMeContact (icontact.h)
description: Sets the local user account concept of 'me' to specified user.
helpviewer_keywords: ["IContactManager interface [Windows Contacts]","SetMeContact method","IContactManager.SetMeContact","IContactManager::SetMeContact","SetMeContact","SetMeContact method [Windows Contacts]","SetMeContact method [Windows Contacts]","IContactManager interface","_wincontacts_IContactManager_SetMeContact","icontact/IContactManager::SetMeContact","wincontacts._wincontacts_IContactManager_SetMeContact"]
old-location: wincontacts\_wincontacts_IContactManager_SetMeContact.htm
tech.root: wincontacts
ms.assetid: 3922ea46-da14-44ad-a9bf-8a10480722da
ms.date: 12/05/2018
ms.keywords: IContactManager interface [Windows Contacts],SetMeContact method, IContactManager.SetMeContact, IContactManager::SetMeContact, SetMeContact, SetMeContact method [Windows Contacts], SetMeContact method [Windows Contacts],IContactManager interface, _wincontacts_IContactManager_SetMeContact, icontact/IContactManager::SetMeContact, wincontacts._wincontacts_IContactManager_SetMeContact
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContactManager::SetMeContact
 - icontact/IContactManager::SetMeContact
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactManager.SetMeContact
---

# IContactManager::SetMeContact


## -description

Sets the local user account concept of 'me' to specified user.

## -parameters

### -param pMeContact [in]

Type: <b><a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a>*</b>

Specifies the contact to treat as 'me' for the current user.

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
Specification was successful. 

</td>
</tr>
</table>