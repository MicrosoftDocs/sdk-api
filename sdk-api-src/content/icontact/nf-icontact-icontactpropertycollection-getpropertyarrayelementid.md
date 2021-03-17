---
UID: NF:icontact.IContactPropertyCollection.GetPropertyArrayElementID
title: IContactPropertyCollection::GetPropertyArrayElementID (icontact.h)
description: Retrieves the unique ID for a given element in a property array.
helpviewer_keywords: ["GetPropertyArrayElementID","GetPropertyArrayElementID method [Windows Contacts]","GetPropertyArrayElementID method [Windows Contacts]","IContactPropertyCollection interface","IContactPropertyCollection interface [Windows Contacts]","GetPropertyArrayElementID method","IContactPropertyCollection.GetPropertyArrayElementID","IContactPropertyCollection::GetPropertyArrayElementID","_wincontacts_IContactPropertyCollection_GetPropertyArrayElementID","icontact/IContactPropertyCollection::GetPropertyArrayElementID","wincontacts._wincontacts_IContactPropertyCollection_GetPropertyArrayElementID"]
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyArrayElementID.htm
tech.root: wincontacts
ms.assetid: bfd860d6-cd67-4f97-afc4-1e2e7c8f57ca
ms.date: 12/05/2018
ms.keywords: GetPropertyArrayElementID, GetPropertyArrayElementID method [Windows Contacts], GetPropertyArrayElementID method [Windows Contacts],IContactPropertyCollection interface, IContactPropertyCollection interface [Windows Contacts],GetPropertyArrayElementID method, IContactPropertyCollection.GetPropertyArrayElementID, IContactPropertyCollection::GetPropertyArrayElementID, _wincontacts_IContactPropertyCollection_GetPropertyArrayElementID, icontact/IContactPropertyCollection::GetPropertyArrayElementID, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyArrayElementID
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
 - IContactPropertyCollection::GetPropertyArrayElementID
 - icontact/IContactPropertyCollection::GetPropertyArrayElementID
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
 - IContactPropertyCollection.GetPropertyArrayElementID
---

# IContactPropertyCollection::GetPropertyArrayElementID


## -description

Retrieves the unique ID for a given element in a property array.

## -parameters

### -param pszArrayElementID [in, out]

Type: <b>LPWSTR</b>

On success, contains the unique ID for the element.

### -param cchArrayElementID [in]

Type: <b>DWORD</b>

Specifies caller-allocated buffer size in characters.

### -param pdwcchArrayElementIDRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszArrayElementID</i>.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

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
Query is successful. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Array node does not have a unique array element ID. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszArrayElementID</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchArrayElementIDRequired</i>. 

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Valid only when <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactpropertycollection-getpropertytype">IContactPropertyCollection::GetPropertyType</a> 
		returns CGD_ARRAY_NODE for the current property.</div>
<div> </div>