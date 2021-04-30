---
UID: NF:icontact.IContactPropertyCollection.GetPropertyVersion
title: IContactPropertyCollection::GetPropertyVersion (icontact.h)
description: Retrieves the version number for the current property in the enumeration.
helpviewer_keywords: ["GetPropertyVersion","GetPropertyVersion method [Windows Contacts]","GetPropertyVersion method [Windows Contacts]","IContactPropertyCollection interface","IContactPropertyCollection interface [Windows Contacts]","GetPropertyVersion method","IContactPropertyCollection.GetPropertyVersion","IContactPropertyCollection::GetPropertyVersion","_wincontacts_IContactPropertyCollection_GetPropertyVersion","icontact/IContactPropertyCollection::GetPropertyVersion","wincontacts._wincontacts_IContactPropertyCollection_GetPropertyVersion"]
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyVersion.htm
tech.root: wincontacts
ms.assetid: ff10129e-45cb-41a4-8800-22b33a238b65
ms.date: 12/05/2018
ms.keywords: GetPropertyVersion, GetPropertyVersion method [Windows Contacts], GetPropertyVersion method [Windows Contacts],IContactPropertyCollection interface, IContactPropertyCollection interface [Windows Contacts],GetPropertyVersion method, IContactPropertyCollection.GetPropertyVersion, IContactPropertyCollection::GetPropertyVersion, _wincontacts_IContactPropertyCollection_GetPropertyVersion, icontact/IContactPropertyCollection::GetPropertyVersion, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyVersion
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
 - IContactPropertyCollection::GetPropertyVersion
 - icontact/IContactPropertyCollection::GetPropertyVersion
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
 - IContactPropertyCollection.GetPropertyVersion
---

# IContactPropertyCollection::GetPropertyVersion


## -description

Retrieves the version number for the current property in the enumeration.

## -parameters

### -param pdwVersion [in, out]

Type: <b>DWORD*</b>

Specifies the version of the property.

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
</table>

