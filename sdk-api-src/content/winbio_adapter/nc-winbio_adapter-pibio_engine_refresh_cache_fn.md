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

# PIBIO_ENGINE_REFRESH_CACHE_FN callback function


## -description


Called by the Windows Biometric Framework to notify the Engine Adapter that it should discard any cached templates that it may be keeping in memory.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


## -returns



The function will return one of the following <b>HRESULT</b> values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This value is returned in all other cases.

</td>
</tr>
</table>
 




## -remarks



An Engine Adapter that maintains a private in-memory cache of templates (e.g., for performance reasons) should discard the contents of its cache when it receives this method call. The call indicates that the cache contents are no longer valid. Depending on the Engine Adapter’s cache policy, the adapter may also choose to reload its cache at this time from the template database.

The biometric service calls this method in the following situations:<ul>
<li>
Once, when the <a href="https://msdn.microsoft.com/6abded6b-12e0-4cc6-a011-0b18e8ea747b">StorageAdapterAttach</a> routine has successfully opened its connection to the template database.

</li>
<li>
Again, after performing any operation that changes the state of the template database. <ul>
<li>
Adding a new template to the database.

</li>
<li>
Deleting one or more existing templates from the database.

</li>
</ul>


</li>
</ul>




