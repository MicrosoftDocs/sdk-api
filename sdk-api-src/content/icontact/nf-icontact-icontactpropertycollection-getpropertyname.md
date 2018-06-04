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

# IContactPropertyCollection::GetPropertyName


## -description


Retrieves the name for the current property in the enumeration.


## -parameters




### -param pszPropertyName [in, out]

Type: <b>LPWSTR</b>

On success, contains the name to use for querying on <a href="https://msdn.microsoft.com/c9c0d73d-4c39-4f7c-9bc6-46d764f157bd">IContactProperties</a>. 
				EX: toplevel -or- toplevel/secondlevel[4]/thirdlevel.


### -param cchPropertyName [in]

Type: <b>DWORD</b>

Specifies caller-allocated buffer size in characters. 


### -param pdwcchPropertyNameRequired [in, out]

Type: <b>DWORD*</b>

On failure, contains the required size for <i>pszPropertyName</i>. 


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
Query is successful. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszPropertyName</i> was not large enough to store the value. 
					The required buffer size is stored in *<i>pdwcchPropertyNameRequired</i>. 

</td>
</tr>
</table>
 



