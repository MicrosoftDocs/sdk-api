---
UID: NF:icontact.IContactProperties.GetDate
title: IContactProperties::GetDate (icontact.h)
description: Retrieves the date and time value at a specified property into a caller's FILETIME structure. All times are stored and returned as Coordinated Universal Time (UTC).
helpviewer_keywords: ["GetDate","GetDate method [Windows Contacts]","GetDate method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","GetDate method","IContactProperties.GetDate","IContactProperties::GetDate","_wincontacts_IContactProperties_GetDate","icontact/IContactProperties::GetDate","wincontacts._wincontacts_IContactProperties_GetDate"]
old-location: wincontacts\_wincontacts_IContactProperties_GetDate.htm
tech.root: wincontacts
ms.assetid: 0ee9a870-ad51-4528-b830-bee72586b936
ms.date: 12/05/2018
ms.keywords: GetDate, GetDate method [Windows Contacts], GetDate method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],GetDate method, IContactProperties.GetDate, IContactProperties::GetDate, _wincontacts_IContactProperties_GetDate, icontact/IContactProperties::GetDate, wincontacts._wincontacts_IContactProperties_GetDate
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
 - IContactProperties::GetDate
 - icontact/IContactProperties::GetDate
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
 - IContactProperties.GetDate
---

# IContactProperties::GetDate


## -description

Retrieves the date and time value at a specified property into a caller's 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. All times are stored 
    and returned as Coordinated Universal Time (UTC).

## -parameters

### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to retrieve.

### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT.

### -param pftDateTime [in, out]

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>*</b>

Specifies caller-allocated <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

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
<i>pftDateTime</i> contains a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The property has been present in the past but its value has been removed. 
					The <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> has been zeroed. 

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
</table>

## -remarks

To retrieve a single level property, set <i>pszPropertyName</i> to the property name. 

To retrieve a value from a multi-value (hierarchical) property, include the desired index as part of <i>pszPropertyName</i> using the form: toplevel/secondlevel[1]/thirdlevel. NOTE: the first element of a set is index 1, so index [0] is invalid.