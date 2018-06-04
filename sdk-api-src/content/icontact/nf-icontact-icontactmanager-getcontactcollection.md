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

# IContactManager::GetContactCollection


## -description


Returns an <a href="https://msdn.microsoft.com/4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897">IContactCollection</a> object that contains all known contacts. 


## -parameters




### -param ppContactCollection [out]

Type: <b><a href="https://msdn.microsoft.com/4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897">IContactCollection</a>**</b>

On success, contains an enumeration of the contact collection. 


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
Success. <i>ppContactCollection</i> contains the collection. 

</td>
</tr>
</table>
 




## -remarks



The enumerator of the new collection is set before the first contact. You must first call <a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a> before querying the collection with <a href="https://msdn.microsoft.com/e5a5d27d-121a-4755-892e-53d148facd74">GetCurrent</a>.



