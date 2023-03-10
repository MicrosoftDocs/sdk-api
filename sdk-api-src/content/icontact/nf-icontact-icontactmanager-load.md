---
UID: NF:icontact.IContactManager.Load
title: IContactManager::Load (icontact.h)
description: Loads an IContact object with the data from the contact referenced by the computer-local contact ID.
helpviewer_keywords: ["IContactManager interface [Windows Contacts]","Load method","IContactManager.Load","IContactManager::Load","Load","Load method [Windows Contacts]","Load method [Windows Contacts]","IContactManager interface","_wincontacts_IContactManager_Load","icontact/IContactManager::Load","wincontacts._wincontacts_IContactManager_Load"]
old-location: wincontacts\_wincontacts_IContactManager_Load.htm
tech.root: wincontacts
ms.assetid: d9addc49-72fd-4b87-bf48-a2a09b1161e9
ms.date: 12/05/2018
ms.keywords: IContactManager interface [Windows Contacts],Load method, IContactManager.Load, IContactManager::Load, Load, Load method [Windows Contacts], Load method [Windows Contacts],IContactManager interface, _wincontacts_IContactManager_Load, icontact/IContactManager::Load, wincontacts._wincontacts_IContactManager_Load
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
 - IContactManager::Load
 - icontact/IContactManager::Load
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
 - IContactManager.Load
---

# IContactManager::Load


## -description

Loads an <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a> object with the data from the contact 
		referenced by the computer-local contact ID.

## -parameters

### -param pszContactID [in]

Type: <b>LPCWSTR</b>

Specifies the contact ID to load.

### -param ppContact [out]

Type: <b><a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a>**</b>

Specifies the destination <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a> object.

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
Contact was found and loaded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Could not find this contact ID. 

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontact-getcontactid">GetContactID</a>



<a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactmanager">IContactManager</a>