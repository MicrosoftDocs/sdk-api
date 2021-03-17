---
UID: NF:icontact.IContactProperties.GetLabels
title: IContactProperties::GetLabels (icontact.h)
description: Retrieves the labels for a specified array element name.
helpviewer_keywords: ["GetLabels","GetLabels method [Windows Contacts]","GetLabels method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","GetLabels method","IContactProperties.GetLabels","IContactProperties::GetLabels","_wincontacts_IContactProperties_GetLabels","icontact/IContactProperties::GetLabels","wincontacts._wincontacts_IContactProperties_GetLabels"]
old-location: wincontacts\_wincontacts_IContactProperties_GetLabels.htm
tech.root: wincontacts
ms.assetid: c639a30b-3778-4ed9-b175-60b4a7ba9748
ms.date: 12/05/2018
ms.keywords: GetLabels, GetLabels method [Windows Contacts], GetLabels method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],GetLabels method, IContactProperties.GetLabels, IContactProperties::GetLabels, _wincontacts_IContactProperties_GetLabels, icontact/IContactProperties::GetLabels, wincontacts._wincontacts_IContactProperties_GetLabels
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
 - IContactProperties::GetLabels
 - icontact/IContactProperties::GetLabels
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
 - IContactProperties.GetLabels
---

# IContactProperties::GetLabels


## -description

Retrieves the labels for a specified array element name.

## -parameters

### -param pszArrayElementName [in]

Type: <b>LPCWSTR</b>

Specifies the array element name.

### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT.

### -param pszLabels [in, out]

Type: <b>LPWSTR</b>

Specifies user-allocated buffer to store the labels.

### -param cchLabels [in]

Type: <b>DWORD</b>

Specifies allocated buffer size in characters.

### -param pdwcchLabelsRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszLabels</i>.

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
Retrieval successful. 

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
Unable to get value 
					for this property due to schema. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszLabels</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchLabelsRequired</i>. 

</td>
</tr>
</table>

## -remarks

The user-allocated buffer in <i>pszLabels</i> receives a concatenated list of null-terminated strings, followed by an empty string. In other words, the last 4 bytes will be zero. For example,  L"str1\0str2\0\0". NOTE: Succeeds only for multi-value properties. Also, may return labels in a different order than they were set.

