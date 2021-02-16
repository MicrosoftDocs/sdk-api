---
UID: NF:icontact.IContactProperties.SetBinary
title: IContactProperties::SetBinary (icontact.h)
description: Sets the binary data at a specified property to the contents of a specified IStream interface [Structured Storage], which contains a null-terminated string (as MIME type) data.
helpviewer_keywords: ["IContactProperties interface [Windows Contacts]","SetBinary method","IContactProperties.SetBinary","IContactProperties::SetBinary","SetBinary","SetBinary method [Windows Contacts]","SetBinary method [Windows Contacts]","IContactProperties interface","_wincontacts_IContactProperties_SetBinary","icontact/IContactProperties::SetBinary","wincontacts._wincontacts_IContactProperties_SetBinary"]
old-location: wincontacts\_wincontacts_IContactProperties_SetBinary.htm
tech.root: wincontacts
ms.assetid: 432c2417-e762-47ff-b2ce-a244120f0545
ms.date: 12/05/2018
ms.keywords: IContactProperties interface [Windows Contacts],SetBinary method, IContactProperties.SetBinary, IContactProperties::SetBinary, SetBinary, SetBinary method [Windows Contacts], SetBinary method [Windows Contacts],IContactProperties interface, _wincontacts_IContactProperties_SetBinary, icontact/IContactProperties::SetBinary, wincontacts._wincontacts_IContactProperties_SetBinary
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
 - IContactProperties::SetBinary
 - icontact/IContactProperties::SetBinary
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
 - IContactProperties.SetBinary
---

# IContactProperties::SetBinary


## -description

Sets the binary data at a specified property to the contents of a specified <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a>, 
		which contains a null-terminated string (as MIME type) data.

## -parameters

### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to set.

### -param dwFlags [in]

Type: <b>DWORD</b>

CGD_DEFAULT can be used to create or overwrite the value at <i>pszPropertyName</i>.

### -param pszContentType [in]

Type: <b>LPWSTR</b>

Specifies null-terminated string representing MIME type to store when CGD_DEFAULT.

### -param pStream [in]

Type: <b>IStream*</b>

Pointer to <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a> object containing data to place at this node. 
				NOTE: IStream::Read is called for the data until it succeeds with a zero-length read. 
				Any other return value results in a failure and no change.

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
Value is set successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Property name is invalid for set, or property name doesn't exist for delete. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Unable to set the value for this property due to schema. 

</td>
</tr>
</table>

## -remarks

To set a single-level property, set <i>pszPropertyName</i> to the property name. 

To set a property from a multi-value property, set <i>pszPropertyName</i> 
		to the form: toplevel/secondlevel[4]/thirdlevel.