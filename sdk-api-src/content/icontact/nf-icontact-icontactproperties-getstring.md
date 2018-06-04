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



