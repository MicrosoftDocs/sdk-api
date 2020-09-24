---
UID: NF:icontact.IContactProperties.DeleteArrayNode
title: IContactProperties::DeleteArrayNode (icontact.h)
description: Deletes the data at a specified array entry.
helpviewer_keywords: ["DeleteArrayNode","DeleteArrayNode method [Windows Contacts]","DeleteArrayNode method [Windows Contacts]","IContactProperties interface","IContactProperties interface [Windows Contacts]","DeleteArrayNode method","IContactProperties.DeleteArrayNode","IContactProperties::DeleteArrayNode","_wincontacts_IContactProperties_DeleteArrayNode","icontact/IContactProperties::DeleteArrayNode","wincontacts._wincontacts_IContactProperties_DeleteArrayNode"]
old-location: wincontacts\_wincontacts_IContactProperties_DeleteArrayNode.htm
tech.root: wincontacts
ms.assetid: a26dc392-1dd7-4dba-9802-b45c01d97493
ms.date: 12/05/2018
ms.keywords: DeleteArrayNode, DeleteArrayNode method [Windows Contacts], DeleteArrayNode method [Windows Contacts],IContactProperties interface, IContactProperties interface [Windows Contacts],DeleteArrayNode method, IContactProperties.DeleteArrayNode, IContactProperties::DeleteArrayNode, _wincontacts_IContactProperties_DeleteArrayNode, icontact/IContactProperties::DeleteArrayNode, wincontacts._wincontacts_IContactProperties_DeleteArrayNode
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
 - IContactProperties::DeleteArrayNode
 - icontact/IContactProperties::DeleteArrayNode
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
 - IContactProperties.DeleteArrayNode
---

# IContactProperties::DeleteArrayNode


## -description

Deletes the data at a specified array entry.

## -parameters

### -param pszArrayElementName [in]

Type: <b>LPCWSTR</b>

Specifies array entry from which to remove all data.

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
Node is deleted. 

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

## -remarks

<div class="alert"><b>Note</b>  Element indexes are unchanged for the entire set. Array node element ID, 
		modification and version data can still be enumerated with <a href="/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a>.</div>
<div> </div>