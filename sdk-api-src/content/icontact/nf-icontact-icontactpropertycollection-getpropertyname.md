---
UID: NF:icontact.IContactPropertyCollection.GetPropertyName
title: IContactPropertyCollection::GetPropertyName (icontact.h)
description: Retrieves the name for the current property in the enumeration.
helpviewer_keywords: ["GetPropertyName","GetPropertyName method [Windows Contacts]","GetPropertyName method [Windows Contacts]","IContactPropertyCollection interface","IContactPropertyCollection interface [Windows Contacts]","GetPropertyName method","IContactPropertyCollection.GetPropertyName","IContactPropertyCollection::GetPropertyName","_wincontacts_IContactPropertyCollection_GetPropertyName","icontact/IContactPropertyCollection::GetPropertyName","wincontacts._wincontacts_IContactPropertyCollection_GetPropertyName"]
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyName.htm
tech.root: wincontacts
ms.assetid: 8fa7fb24-2648-4f7b-b37c-d42b2966a959
ms.date: 12/05/2018
ms.keywords: GetPropertyName, GetPropertyName method [Windows Contacts], GetPropertyName method [Windows Contacts],IContactPropertyCollection interface, IContactPropertyCollection interface [Windows Contacts],GetPropertyName method, IContactPropertyCollection.GetPropertyName, IContactPropertyCollection::GetPropertyName, _wincontacts_IContactPropertyCollection_GetPropertyName, icontact/IContactPropertyCollection::GetPropertyName, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyName
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
 - IContactPropertyCollection::GetPropertyName
 - icontact/IContactPropertyCollection::GetPropertyName
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
 - IContactPropertyCollection.GetPropertyName
---

# IContactPropertyCollection::GetPropertyName


## -description

Retrieves the name for the current property in the enumeration.

## -parameters

### -param pszPropertyName [in, out]

Type: <b>LPWSTR</b>

On success, contains the name to use for querying on <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactproperties">IContactProperties</a>. 
				EX: toplevel -or- toplevel/secondlevel[4]/thirdlevel.

### -param cchPropertyName [in]

Type: <b>DWORD</b>

Specifies caller-allocated buffer size in characters.

### -param pdwcchPropertyNameRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszPropertyName</i>.

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
Query is successful. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszPropertyName</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchPropertyNameRequired</i>. 

</td>
</tr>
</table>