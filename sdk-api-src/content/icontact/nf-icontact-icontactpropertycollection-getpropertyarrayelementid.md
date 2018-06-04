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

# IContactPropertyCollection::GetPropertyArrayElementID


## -description


Retrieves the unique ID for a given element in a property array.


## -parameters




### -param pszArrayElementID [in, out]

Type: <b>LPWSTR</b>

On success, contains the unique ID for the element. 


### -param cchArrayElementID [in]

Type: <b>DWORD</b>

Specifies caller-allocated buffer size in characters. 


### -param pdwcchArrayElementIDRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszArrayElementID</i>. 


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

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
Query is successful. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Array node does not have a unique array element ID. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszArrayElementID</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchArrayElementIDRequired</i>. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Valid only when <a href="https://msdn.microsoft.com/11977b0c-332a-415a-986f-7fb08246413f">IContactPropertyCollection::GetPropertyType</a> 
		returns CGD_ARRAY_NODE for the current property.</div>
<div> </div>


