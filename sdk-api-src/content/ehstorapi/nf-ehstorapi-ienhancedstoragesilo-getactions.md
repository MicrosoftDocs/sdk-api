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

# IEnhancedStorageSilo::GetActions


## -description


Returns an enumeration of all actions available to the silo object.


## -parameters




### -param pppIEnhancedStorageSiloActions [out]

Array of pointers to <a href="https://msdn.microsoft.com/6deb7e22-f153-45fd-98ea-53a2e5692df7">IEnhancedStorageAction</a> interface objects that represent the actions available for the silo object. This array is allocated within the API when at least one action is available to the silo.


### -param pcEnhancedStorageSiloActions [out]

Count of <a href="https://msdn.microsoft.com/6deb7e22-f153-45fd-98ea-53a2e5692df7">IEnhancedStorageAction</a> pointers returned. This value indicates the dimension of the  array represented by <i>pppIEnhancedStorageSilos</i>.


## -returns



This method can return one of these values.

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
One or more ACTs were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pppIEnhancedStorageSiloActions</i> or  <i>pcEnhancedStorageSiloActions</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The memory containing the <a href="https://msdn.microsoft.com/6deb7e22-f153-45fd-98ea-53a2e5692df7">IEnhancedStorageAction</a> interface pointers is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a>
 

 

