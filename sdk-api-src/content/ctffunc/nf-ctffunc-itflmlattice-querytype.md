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

# ITfLMLattice::QueryType


## -description




## -parameters




### -param rguidType [in]

Specifies the lattice type identifier. This can be one of the <a href="https://msdn.microsoft.com/ce4bf11b-e7e7-4f06-b572-8ed6f0ed8d36">Lattice Type</a> values.


### -param pfSupported [out]

Pointer to a <b>BOOL</b> that receives a value that indicates if the lattice type is supported. If the lattice type is supported, this parameter receives a nonzero value and the method returns S_OK. If the lattice type is unsupported, this parameter receives zero and the method returns E_INVALIDARG.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The specified lattice type is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Either <i>pfSupported</i> is invalid or the specified lattice type is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/25ad6ef2-1d42-498a-852f-163a0efbc26a">ITfLMLattice</a>



<a href="https://msdn.microsoft.com/ce4bf11b-e7e7-4f06-b572-8ed6f0ed8d36">Lattice Types
      </a>
 

 

