---
UID: NF:icontact.IContactProperties.SetString
title: IContactProperties::SetString
author: windows-sdk-content
description: Sets the string value of a specified property to that of a specified null-terminated string.
old-location: wincontacts\_wincontacts_IContactProperties_SetString.htm
old-project: wincontacts
ms.assetid: 6e8379cc-a5dd-4ffd-b478-a14e649f5f0b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IContactProperties interface [Windows Contacts],SetString method, IContactProperties.SetString, IContactProperties::SetString, SetString, SetString method [Windows Contacts], SetString method [Windows Contacts],IContactProperties interface, _wincontacts_IContactProperties_SetString, icontact/IContactProperties::SetString, wincontacts._wincontacts_IContactProperties_SetString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactProperties.SetString
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactProperties::SetString


## -description


Sets the string value of a specified property to that of a specified null-terminated string. 


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to set.


### -param dwFlags [in]

Type: <b>DWORD</b>

CGD_DEFAULT can be used to create or overwrite value at <i>pszPropertyName</i>. 


### -param pszValue [in]

Type: <b>LPWSTR</b>

Specifies null-terminated string to store. 


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
Value is set at this property. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Property name invalid for set. 

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
 




## -remarks



To set a single-level property, set <i>pszPropertyName</i> to the property name. 

To set a property from a multi-value property, set <i>pszPropertyName</i> to the form: 
		toplevel/secondlevel[4]/thirdlevel.



