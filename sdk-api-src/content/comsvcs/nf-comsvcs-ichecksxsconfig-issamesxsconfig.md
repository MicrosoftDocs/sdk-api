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

# ICheckSxsConfig::IsSameSxsConfig


## -description


Determines whether the side-by-side assembly has the specified configuration.


## -parameters




### -param wszSxsName [in]

A text string that contains the file name of the side-by-side assembly. The proper extension is added automatically.


### -param wszSxsDirectory [in]

A text string that contains the directory of the side-by-side assembly.


### -param wszSxsAppName [in]

A text string that contains the name of the application domain.


## -returns



This method can return the standard return values E_INVALIDARG and E_OUTOFMEMORY, as well as the following values.

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
The current side-by-side assembly has the specified configuration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The current side-by-side assembly does not have the specified configuration.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/34c97d61-694e-4ee3-92ed-55b0a787b747">ICheckSxsConfig</a>
 

 

