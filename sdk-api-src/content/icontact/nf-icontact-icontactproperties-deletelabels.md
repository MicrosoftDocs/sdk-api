---
UID: NF:icontact.IContactProperties.DeleteLabels
title: IContactProperties::DeleteLabels (icontact.h)
description: Deletes the labels at a specified array entry.
helpviewer_keywords: ["DeleteLabels","DeleteLabels method [Windows Contacts]","DeleteLabels method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","DeleteLabels method","IContactProperties.DeleteLabels","IContactProperties::DeleteLabels","_wincontacts_IContactProperties_DeleteLabels","icontact/IContactProperties::DeleteLabels","wincontacts._wincontacts_IContactProperties_DeleteLabels"]
old-location: wincontacts\_wincontacts_IContactProperties_DeleteLabels.htm
tech.root: wincontacts
ms.assetid: 0925bed9-26ef-46e6-9087-0e1a1e57349d
ms.date: 12/05/2018
ms.keywords: DeleteLabels, DeleteLabels method [Windows Contacts], DeleteLabels method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],DeleteLabels method, IContactProperties.DeleteLabels, IContactProperties::DeleteLabels, _wincontacts_IContactProperties_DeleteLabels, icontact/IContactProperties::DeleteLabels, wincontacts._wincontacts_IContactProperties_DeleteLabels
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
 - IContactProperties::DeleteLabels
 - icontact/IContactProperties::DeleteLabels
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
 - IContactProperties.DeleteLabels
---

# IContactProperties::DeleteLabels


## -description

Deletes the labels at a specified array entry.

## -parameters

### -param pszArrayElementName [in]

Type: <b>LPCWSTR</b>

Specifies the property to delete labels on.

### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT.

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
Labels deleted successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Property name doesn't exist for delete. 

</td>
</tr>
</table>

