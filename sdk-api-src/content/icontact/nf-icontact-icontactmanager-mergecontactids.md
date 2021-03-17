---
UID: NF:icontact.IContactManager.MergeContactIDs
title: IContactManager::MergeContactIDs (icontact.h)
description: Makes an old Contact ID resolve to the same value as a new Contact ID. Subsequent calls to IContactManager::Load with the old contact ID now loads the new contact ID contact.
helpviewer_keywords: ["IContactManager interface [Windows Contacts]","MergeContactIDs method","IContactManager.MergeContactIDs","IContactManager::MergeContactIDs","MergeContactIDs","MergeContactIDs method [Windows Contacts]","MergeContactIDs method [Windows Contacts]","IContactManager interface","_wincontacts_IContactManager_MergeContactIDs","icontact/IContactManager::MergeContactIDs","wincontacts._wincontacts_IContactManager_MergeContactIDs"]
old-location: wincontacts\_wincontacts_IContactManager_MergeContactIDs.htm
tech.root: wincontacts
ms.assetid: 1a3aea59-ef92-4775-b942-7383a5e8a63c
ms.date: 12/05/2018
ms.keywords: IContactManager interface [Windows Contacts],MergeContactIDs method, IContactManager.MergeContactIDs, IContactManager::MergeContactIDs, MergeContactIDs, MergeContactIDs method [Windows Contacts], MergeContactIDs method [Windows Contacts],IContactManager interface, _wincontacts_IContactManager_MergeContactIDs, icontact/IContactManager::MergeContactIDs, wincontacts._wincontacts_IContactManager_MergeContactIDs
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
 - IContactManager::MergeContactIDs
 - icontact/IContactManager::MergeContactIDs
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
 - IContactManager.MergeContactIDs
---

# IContactManager::MergeContactIDs


## -description

Makes an old Contact ID resolve to the same value as a new Contact ID. 
		Subsequent calls to <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactmanager-load">IContactManager::Load</a> with the old contact ID 
		now loads the new contact ID contact.

## -parameters

### -param pszNewContactID [in]

Type: <b>LPWSTR</b>

Specifies the ID of the new contact, representing both the old and new contacts.

### -param pszOldContactID [in]

Type: <b>LPCWSTR</b>

Specifies the ID representing the old contact.

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
Address change was successful. 

</td>
</tr>
</table>