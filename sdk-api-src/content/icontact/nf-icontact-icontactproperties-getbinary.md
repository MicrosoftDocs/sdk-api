---
UID: NF:icontact.IContactProperties.GetBinary
title: IContactProperties::GetBinary (icontact.h)
description: Retrieves the binary data of a property using an IStream interface [Structured Storage].
helpviewer_keywords: ["GetBinary","GetBinary method [Windows Contacts]","GetBinary method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","GetBinary method","IContactProperties.GetBinary","IContactProperties::GetBinary","_wincontacts_IContactProperties_GetBinary","icontact/IContactProperties::GetBinary","wincontacts._wincontacts_IContactProperties_GetBinary"]
old-location: wincontacts\_wincontacts_IContactProperties_GetBinary.htm
tech.root: wincontacts
ms.assetid: 1a62c5d3-7052-4c10-90e7-25f616ac36b8
ms.date: 12/05/2018
ms.keywords: GetBinary, GetBinary method [Windows Contacts], GetBinary method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],GetBinary method, IContactProperties.GetBinary, IContactProperties::GetBinary, _wincontacts_IContactProperties_GetBinary, icontact/IContactProperties::GetBinary, wincontacts._wincontacts_IContactProperties_GetBinary
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
 - IContactProperties::GetBinary
 - icontact/IContactProperties::GetBinary
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
 - IContactProperties.GetBinary
---

# IContactProperties::GetBinary


## -description

Retrieves the binary data of a property using an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a>.

## -parameters

### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to retrieve.

### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT.

### -param pszContentType [in, out]

Type: <b>LPWSTR</b>

Specifies user-allocated buffer to store the MIME content type.

### -param cchContentType [in]

Type: <b>DWORD</b>

Specifies the allocated buffer size in characters.

### -param pdwcchContentTypeRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszContentType</i>.

### -param ppStream [out]

Type: <b>IStream**</b>

On success, contains a new <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a>. Use this to retrieve the binary data.

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
<i>ppStream</i> contains an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a>.  
					Caller must release the reference. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No data for this value. Either the property has been present in the past 
					but its value has been removed or the property is a container of other properties 
					(toplevel/secondlevel[3]). The buffer at <i>pszContentType</i> has been zeroed. 

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
Unable to get value for this property due to schema. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszContentType</i> was not large enough to store the value. 
					The required buffer size is stored in <i>pdwcchContentTypeRequired</i>. 

</td>
</tr>
</table>

## -remarks

To retrieve a single level property, set <i>pszPropertyName</i> to the property name. 

To retrieve a value from a multi-value (hierarchical) property, include the desired index as part of <i>pszPropertyName</i> using the form: toplevel/secondlevel[1]/thirdlevel. NOTE: the first element of a set is index 1, so index [0] is invalid.

For deleted properties, this method returns S_OK and an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a> of zero length. NOTE: For properties not of binary type, this method may return incorrect data in the IStream.