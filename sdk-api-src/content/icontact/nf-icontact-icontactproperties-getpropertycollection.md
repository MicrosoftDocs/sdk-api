---
UID: NF:icontact.IContactProperties.GetPropertyCollection
title: IContactProperties::GetPropertyCollection (icontact.h)
description: Returns an IContactPropertyCollection for the current contact. Optionally, filters the IContactPropertyCollection to enumerate only some values.
helpviewer_keywords: ["GetPropertyCollection","GetPropertyCollection method [Windows Contacts]","GetPropertyCollection method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","GetPropertyCollection method","IContactProperties.GetPropertyCollection","IContactProperties::GetPropertyCollection","_wincontacts_IContactProperties_GetPropertyCollection","icontact/IContactProperties::GetPropertyCollection","wincontacts._wincontacts_IContactProperties_GetPropertyCollection"]
old-location: wincontacts\_wincontacts_IContactProperties_GetPropertyCollection.htm
tech.root: wincontacts
ms.assetid: 12ef5ff0-ac87-4475-86b3-31a6379ffb4e
ms.date: 12/05/2018
ms.keywords: GetPropertyCollection, GetPropertyCollection method [Windows Contacts], GetPropertyCollection method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],GetPropertyCollection method, IContactProperties.GetPropertyCollection, IContactProperties::GetPropertyCollection, _wincontacts_IContactProperties_GetPropertyCollection, icontact/IContactProperties::GetPropertyCollection, wincontacts._wincontacts_IContactProperties_GetPropertyCollection
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
 - IContactProperties::GetPropertyCollection
 - icontact/IContactProperties::GetPropertyCollection
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
 - IContactProperties.GetPropertyCollection
---

# IContactProperties::GetPropertyCollection


## -description

Returns an <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a> for the current contact. 
		Optionally, filters the <b>IContactPropertyCollection</b> to enumerate only some values.

## -parameters

### -param ppPropertyCollection [out]

Type: <b><a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a>**</b>

On success, points to the new <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a>.

### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT.

### -param pszMultiValueName [in]

Type: <b>LPCWSTR</b>

Specifies the name of the collection (for example: emailAddresses or [namespace]arrayNode). 
				If <b>NULL</b>, all collections are searched for <i>ppszLabels</i>.

### -param dwLabelCount [in]

Type: <b>DWORD</b>

Specifies the number of labels in <i>ppszLabels</i>. 
				If zero, all subproperties with labels are returned.

### -param ppszLabels [in]

Type: <b>LPCWSTR</b>

Specifies an array of string labels to test for. 
				All labels in the array must be set to a valid string (not <b>NULL</b>).

### -param fAnyLabelMatches [in]

Type: <b>BOOL</b>

TRUE if the presence of any label on a given property matches the property. 
				FALSE if all labels must be present to match the property.

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
Always returns success. 

</td>
</tr>
</table>

## -remarks

Caller can enumerate all child properties of a top-level property with 
		an optional label filter applied. For example: all emailAddresses where label="work". On success, 
		collection has been reset to the location before the first element (if any are present). 
		Call <a href="/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactpropertycollection-next">Next</a> to begin querying data.