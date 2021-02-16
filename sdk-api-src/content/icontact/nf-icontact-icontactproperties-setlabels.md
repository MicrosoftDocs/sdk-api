---
UID: NF:icontact.IContactProperties.SetLabels
title: IContactProperties::SetLabels (icontact.h)
description: Appends the set of labels passed in to the specified property's label set. Note:\_This method does not check for duplicate labels.
helpviewer_keywords: ["IContactProperties interface [Windows Contacts]","SetLabels method","IContactProperties.SetLabels","IContactProperties::SetLabels","SetLabels","SetLabels method [Windows Contacts]","SetLabels method [Windows Contacts]","IContactProperties interface","_wincontacts_IContactProperties_SetLabels","icontact/IContactProperties::SetLabels","wincontacts._wincontacts_IContactProperties_SetLabels"]
old-location: wincontacts\_wincontacts_IContactProperties_SetLabels.htm
tech.root: wincontacts
ms.assetid: 884d4edf-e001-4a1d-9ee4-7f8733aba343
ms.date: 12/05/2018
ms.keywords: IContactProperties interface [Windows Contacts],SetLabels method, IContactProperties.SetLabels, IContactProperties::SetLabels, SetLabels, SetLabels method [Windows Contacts], SetLabels method [Windows Contacts],IContactProperties interface, _wincontacts_IContactProperties_SetLabels, icontact/IContactProperties::SetLabels, wincontacts._wincontacts_IContactProperties_SetLabels
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
 - IContactProperties::SetLabels
 - icontact/IContactProperties::SetLabels
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
 - IContactProperties.SetLabels
---

# IContactProperties::SetLabels


## -description

Appends the set of labels passed in to the specified property's label set. 
		Note: This method does not check for duplicate labels.

## -parameters

### -param pszArrayElementName [in]

Type: <b>LPCWSTR</b>

Specifies the property to label.

### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT.

### -param dwLabelCount [in]

Type: <b>DWORD</b>

Specifies the count of labels in array.

### -param ppszLabels [in]

Type: <b>LPCWSTR</b>

 Specifies an array of LPCWSTR labels.

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
Labels set successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No data found for this property name. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Unable to set value for this property due to schema. 

</td>
</tr>
</table>

