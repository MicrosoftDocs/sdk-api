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

# ITTerminalManager2::GetPluggableSuperclasses


## -description


The 
<b>GetPluggableSuperclasses</b> method gets the public CLSIDs for all pluggable terminal superclasses in the registry.


## -parameters




### -param pdwNumSuperclasses [in, out]

The number of superclasses retrieved. If <i>pSuperclasses</i> is <b>NULL</b>, this argument is used to get the total number of pluggable terminal superclasses registered in the registry. If <i>pSuperclasses</i> is not <b>NULL</b>, this argument is used to pass the size, in IIDs, of the <i>pSuperclasses</i> buffer, and the method returns the number of IIDs copied into buffer memory.


### -param pSuperclasses [out]

Pointer to an IID buffer allocated by the user. 




If the buffer is <b>NULL</b>, the method returns the count of superclasses in the buffer. Otherwise, the method returns the IIDs of the pluggable terminal superclasses registered on the system.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f91c8684-27f8-4db8-99ff-d5a6cb87a0c2">ITTerminalManager2</a>
 

 

