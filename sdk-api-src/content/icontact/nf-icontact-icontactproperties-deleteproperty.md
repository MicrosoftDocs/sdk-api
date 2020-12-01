---
UID: NF:icontact.IContactProperties.DeleteProperty
title: IContactProperties::DeleteProperty (icontact.h)
description: Deletes the value at a specified property. Property modification and version data can still be enumerated with IContactPropertyCollection.
helpviewer_keywords: ["DeleteProperty","DeleteProperty method [Windows Contacts]","DeleteProperty method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","DeleteProperty method","IContactProperties.DeleteProperty","IContactProperties::DeleteProperty","_wincontacts_IContactProperties_DeleteProperty","icontact/IContactProperties::DeleteProperty","wincontacts._wincontacts_IContactProperties_DeleteProperty"]
old-location: wincontacts\_wincontacts_IContactProperties_DeleteProperty.htm
tech.root: wincontacts
ms.assetid: 74ed72da-e82c-4257-9d16-c5204a88c9bf
ms.date: 12/05/2018
ms.keywords: DeleteProperty, DeleteProperty method [Windows Contacts], DeleteProperty method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],DeleteProperty method, IContactProperties.DeleteProperty, IContactProperties::DeleteProperty, _wincontacts_IContactProperties_DeleteProperty, icontact/IContactProperties::DeleteProperty, wincontacts._wincontacts_IContactProperties_DeleteProperty
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
 - IContactProperties::DeleteProperty
 - icontact/IContactProperties::DeleteProperty
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
 - IContactProperties.DeleteProperty
---

# IContactProperties::DeleteProperty


## -description

Deletes the value at a specified property. Property modification 
		and version data can still be enumerated with <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a>.

## -parameters

### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to delete the value for.

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
Property deleted successfully. 

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