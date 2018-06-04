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

# ISharedPropertyGroupManager::get_Group


## -description


Retrieves a reference to an existing shared property group.


## -parameters




### -param Name [in]

The name of the shared property group to be retrieved.


### -param ppGroup [out]

A reference to the shared property group specified in the <i>Name</i> parameter, or <b>NULL</b> if the property group does not exist. 


## -returns



This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
The shared property group exists, and a reference to it is returned in the <i>ppGroup</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The shared property group with the name specified in the <i>Name</i> parameter does not exist.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/71c0a1de-5ea5-4496-b0e9-56d0cc8129a9">ISharedPropertyGroupManager</a>
 

 

