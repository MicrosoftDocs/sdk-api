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

# IContact::GetContactID


## -description


Retrieves the local computer unique contact ID.


## -parameters




### -param pszContactID [in, out]

Type: <b>LPWSTR</b>

User allocated buffer to store the contact ID.


### -param cchContactID [in]

Type: <b>DWORD</b>

Specifies allocated buffer size. 


### -param pdwcchContactIDRequired [in, out]

Type: <b>DWORD*</b>

Upon failure due to insufficient buffer, contains the required size for <i>pszContactID</i>. May be <b>NULL</b>. 


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
Success. <i>pszContactID</i> contains a null-terminated ContactID. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Macro HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) returned when <i>pszContactID</i> was not large enough to store the value. The required buffer size is stored in <i>pdwcchContactIDRequired</i>. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a>



<a href="https://msdn.microsoft.com/d9addc49-72fd-4b87-bf48-a2a09b1161e9">Load</a>
 

 

