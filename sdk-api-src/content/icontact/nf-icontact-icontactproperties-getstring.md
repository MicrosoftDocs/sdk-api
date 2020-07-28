---
UID: NF:icontact.IContactProperties.GetString
title: IContactProperties::GetString (icontact.h)
description: Retrieves the string value at a specified property into a caller-allocated buffer.
helpviewer_keywords: ["GetString","GetString method [Windows Contacts]","GetString method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","GetString method","IContactProperties.GetString","IContactProperties::GetString","_wincontacts_IContactProperties_GetString","icontact/IContactProperties::GetString","wincontacts._wincontacts_IContactProperties_GetString"]
old-location: wincontacts\_wincontacts_IContactProperties_GetString.htm
tech.root: wincontacts
ms.assetid: ecab7290-9a35-4da3-a161-b8d52a031172
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Windows Contacts], GetString method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],GetString method, IContactProperties.GetString, IContactProperties::GetString, _wincontacts_IContactProperties_GetString, icontact/IContactProperties::GetString, wincontacts._wincontacts_IContactProperties_GetString
f1_keywords:
- icontact/IContactProperties.GetString
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wab32.dll
api_name:
- IContactProperties.GetString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContactProperties::GetString


## -description


Retrieves the string value at a specified property into a caller-allocated buffer. 


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to retrieve.


### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT. 


### -param pszValue [in, out]

Type: <b>LPWSTR</b>

Specifies user-allocated buffer to store the property. 


### -param cchValue [in]

Type: <b>DWORD*</b>

Specifies allocated buffer size in characters. 


### -param pdwcchPropertyValueRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszValue</i>. 


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
<i>pszValue</i> contains the null-terminated value. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No data for this value. Either the property has been present in the past but its value has been removed 
					or the property is a container of other properties (toplevel/secondlevel[3]). The buffer at <i>pszValue</i> has been zero'ed. 

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszValue</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchPropertyValueRequired</i>. 

</td>
</tr>
</table>
 




## -remarks



To retrieve a single level property, set <i>pszPropertyName</i> to the property name.

To retrieve a value from a multi-value (hierarchical) property, include the desired index as part of <i>pszPropertyName</i> in the form: toplevel/secondlevel[1]/thirdlevel. NOTE: the first element of a set is index 1, so index [0] is invalid. The following example retrieves the Title of the fourth Name property of a contact.
		

<code>L"NameCollection/Name[4]/Title"</code>



