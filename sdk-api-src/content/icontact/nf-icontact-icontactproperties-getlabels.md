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

# IContactProperties::GetLabels


## -description


Retrieves the labels for a specified array element name. 


## -parameters




### -param pszArrayElementName [in]

Type: <b>LPCWSTR</b>

Specifies the array element name.


### -param dwFlags [in]

Type: <b>DWORD</b>

Must be CGD_DEFAULT. 


### -param pszLabels [in, out]

Type: <b>LPWSTR</b>

Specifies user-allocated buffer to store the labels. 


### -param cchLabels [in]

Type: <b>DWORD</b>

Specifies allocated buffer size in characters. 


### -param pdwcchLabelsRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszLabels</i>. 


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
Retrieval successful. 

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
Unable to get value 
					for this property due to schema. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszLabels</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchLabelsRequired</i>. 

</td>
</tr>
</table>
 




## -remarks



The user-allocated buffer in <i>pszLabels</i> receives a concatenated list of null-terminated strings, followed by an empty string. In other words, the last 4 bytes will be zero. For example,  L"str1\0str2\0\0". NOTE: Succeeds only for multi-value properties. Also, may return labels in a different order than they were set.



