---
UID: NF:icontact.IContactManager.GetContactCollection
title: IContactManager::GetContactCollection (icontact.h)
description: Returns an IContactCollection object that contains all known contacts.
helpviewer_keywords: ["GetContactCollection","GetContactCollection method [Windows Contacts]","GetContactCollection method [Windows Contacts]","IContactManager interface","IContactManager interface [Windows Contacts]","GetContactCollection method","IContactManager.GetContactCollection","IContactManager::GetContactCollection","_wincontacts_IContactManager_GetContactCollection","icontact/IContactManager::GetContactCollection","wincontacts._wincontacts_IContactManager_GetContactCollection"]
old-location: wincontacts\_wincontacts_IContactManager_GetContactCollection.htm
tech.root: wincontacts
ms.assetid: 6b9d7ba5-e2cd-452f-8479-fdaad183b1ac
ms.date: 12/05/2018
ms.keywords: GetContactCollection, GetContactCollection method [Windows Contacts], GetContactCollection method [Windows Contacts],IContactManager interface, IContactManager interface [Windows Contacts],GetContactCollection method, IContactManager.GetContactCollection, IContactManager::GetContactCollection, _wincontacts_IContactManager_GetContactCollection, icontact/IContactManager::GetContactCollection, wincontacts._wincontacts_IContactManager_GetContactCollection
req.header: icontact.h
req.include-header: 
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
 - IContactManager::GetContactCollection
 - icontact/IContactManager::GetContactCollection
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
 - IContactManager.GetContactCollection
---

# IContactManager::GetContactCollection


## -description

Returns an <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactcollection">IContactCollection</a> object that contains all known contacts.

## -parameters

### -param ppContactCollection [out]

Type: <b><a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactcollection">IContactCollection</a>**</b>

On success, contains an enumeration of the contact collection.

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
Success. <i>ppContactCollection</i> contains the collection. 

</td>
</tr>
</table>

## -remarks

The enumerator of the new collection is set before the first contact. You must first call <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-next">Next</a> before querying the collection with <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-getcurrent">GetCurrent</a>.