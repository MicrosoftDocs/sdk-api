---
UID: NF:icontact.IContactProperties.SetDate
title: IContactProperties::SetDate
author: windows-sdk-content
description: Sets the date and time value at a specified property to a given FILETIME. All times are stored and returned as Coordinated Universal Time (UTC).
old-location: wincontacts\_wincontacts_IContactProperties_SetDate.htm
tech.root: wincontacts
ms.assetid: bbe0a788-7291-48f7-a36a-88e5b6b971dc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IContactProperties interface [Windows Contacts],SetDate method, IContactProperties.SetDate, IContactProperties::SetDate, SetDate, SetDate method [Windows Contacts], SetDate method [Windows Contacts],IContactProperties interface, _wincontacts_IContactProperties_SetDate, icontact/IContactProperties::SetDate, wincontacts._wincontacts_IContactProperties_SetDate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IContactProperties.SetDate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContactProperties::SetDate


## -description


Sets the date and time value at a specified property to a given 
    <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a>. All times are stored and returned as Coordinated Universal Time (UTC).


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to set.


### -param dwFlags [in]

Type: <b>DWORD</b>

CGD_DEFAULT can be used to create or overwrite value at <i>pszPropertyName</i>. 


### -param ftDateTime [in]

Type: <b><a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a></b>


<a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a> structure to use for date. 


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
Unable to set the value for this property due to schema. 

</td>
</tr>
</table>
 



