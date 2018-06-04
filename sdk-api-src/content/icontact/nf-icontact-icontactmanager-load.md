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

# IContactManager::Load


## -description


Loads an <a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a> object with the data from the contact 
		referenced by the computer-local contact ID.


## -parameters




### -param pszContactID [in]

Type: <b>LPCWSTR</b>

Specifies the contact ID to load.


### -param ppContact [out]

Type: <b><a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a>**</b>

Specifies the destination <a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a> object.


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
Contact was found and loaded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Could not find this contact ID. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/25daa44f-2042-4116-b0dd-4f16857cbb0b">GetContactID</a>



<a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a>
 

 

