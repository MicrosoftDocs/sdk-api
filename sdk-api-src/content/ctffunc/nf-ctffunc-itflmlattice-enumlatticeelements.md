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

# ITfLMLattice::EnumLatticeElements


## -description




## -parameters




### -param dwFrameStart [in]

Specifies the offset, in 100-nanosecond units, relative to the start of the phrase, of the first element to obtain.


### -param rguidType [in]

Specifies the lattice type identifier. This can be one of the <a href="https://msdn.microsoft.com/ce4bf11b-e7e7-4f06-b572-8ed6f0ed8d36">Lattice Type</a> values.


### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">IEnumTfLatticeElements</a> interface pointer that receives the enumerator object.


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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rguidType</i> is unsupported by the lattice property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">
        IEnumTfLatticeElements
      </a>



<a href="https://msdn.microsoft.com/25ad6ef2-1d42-498a-852f-163a0efbc26a">ITfLMLattice</a>



<a href="https://msdn.microsoft.com/ce4bf11b-e7e7-4f06-b572-8ed6f0ed8d36">Lattice Types
      </a>
 

 

