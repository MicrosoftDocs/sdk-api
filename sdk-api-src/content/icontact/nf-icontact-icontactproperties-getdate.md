---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IContactProperties::GetDate


## -description


Retrieves the date and time value at a specified property into a caller's 
    <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a> structure. All times are stored 
    and returned as Coordinated Universal Time (UTC).


## -parameters




### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

Specifies the property to retrieve.


### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT. 


### -param pftDateTime [in, out]

Type: <b><a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a>*</b>

Specifies caller-allocated <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a> structure. 


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
<i>pftDateTime</i> contains a valid <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a>. 

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
					The <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a> has been zero'ed. 

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



