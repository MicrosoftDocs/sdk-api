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
		modification and version data can still be enumerated with <a href="https://msdn.microsoft.com/dec9430d-2174-42fe-85c1-16fa7e7adc0c">IContactPropertyCollection</a>.</div>
<div> </div>


