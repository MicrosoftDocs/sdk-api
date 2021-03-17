---
UID: NF:icontact.IContactPropertyCollection.GetPropertyModificationDate
title: IContactPropertyCollection::GetPropertyModificationDate (icontact.h)
description: Retrieves the last modification date for the current property in the enumeration. If not modified, contact creation date is returned.
helpviewer_keywords: ["GetPropertyModificationDate","GetPropertyModificationDate method [Windows Contacts]","GetPropertyModificationDate method [Windows Contacts]","IContactPropertyCollection interface","IContactPropertyCollection interface [Windows Contacts]","GetPropertyModificationDate method","IContactPropertyCollection.GetPropertyModificationDate","IContactPropertyCollection::GetPropertyModificationDate","_wincontacts_IContactPropertyCollection_GetPropertyModificationDate","icontact/IContactPropertyCollection::GetPropertyModificationDate","wincontacts._wincontacts_IContactPropertyCollection_GetPropertyModificationDate"]
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyModificationDate.htm
tech.root: wincontacts
ms.assetid: 7ad95916-4e21-4607-b27d-584a931f9201
ms.date: 12/05/2018
ms.keywords: GetPropertyModificationDate, GetPropertyModificationDate method [Windows Contacts], GetPropertyModificationDate method [Windows Contacts],IContactPropertyCollection interface, IContactPropertyCollection interface [Windows Contacts],GetPropertyModificationDate method, IContactPropertyCollection.GetPropertyModificationDate, IContactPropertyCollection::GetPropertyModificationDate, _wincontacts_IContactPropertyCollection_GetPropertyModificationDate, icontact/IContactPropertyCollection::GetPropertyModificationDate, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyModificationDate
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
 - IContactPropertyCollection::GetPropertyModificationDate
 - icontact/IContactPropertyCollection::GetPropertyModificationDate
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
 - IContactPropertyCollection.GetPropertyModificationDate
---

# IContactPropertyCollection::GetPropertyModificationDate


## -description

Retrieves the last modification date for the current property in the enumeration. 
		If not modified, contact creation date is returned.

## -parameters

### -param pftModificationDate [in, out]

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>*</b>

Specifies the last modified date as a UTC FILETIME.

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
</table>