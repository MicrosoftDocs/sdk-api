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

# IAssemblyCache::CreateAssemblyCacheItem


## -description


The <b>CreateAssemblyCacheItem</b> method creates an item in the assembly cache that corresponds to the side-by-side assembly being installed.


## -parameters




### -param dwFlags [in]

Reserved.


### -param pvReserved [in]

Reserved.


### -param ppAsmItem [out]

Pointer to a location containing the pointer to the instance of the <a href="https://msdn.microsoft.com/9df9ee58-0354-49f0-af9c-5b92179cfaea">IAssemblyCacheItem</a> that receives the information.


### -param pszAssemblyName [in, optional]

Pointer to a null-terminated string value containing the fully-specified strong name of the assembly that is being installed. The name provided is verified to match the name of the assembly in the manifest. Partial names return <b>FUSION_E_INVALID_NAME</b>. If this parameter is null, the name is not verified.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FUSION_E_INVALID_NAME</dt>
</dl>
</td>
<td width="60%">
The full name of the assembly must be provided by <i>pszAssemblyName</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c411ae7-5a8f-47ca-a9c1-e23000f64620">IAssemblyCache</a>
 

 

