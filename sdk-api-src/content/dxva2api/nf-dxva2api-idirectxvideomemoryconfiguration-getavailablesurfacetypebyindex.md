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

# IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex


## -description



Retrieves a supported video surface type.




## -parameters




### -param dwTypeIndex [in]

Zero-based index of the surface type to retrieve. Surface types are indexed in order of preference, starting with the most preferred type.


### -param pdwType [out]

Receives a member of the <a href="https://msdn.microsoft.com/7ede2247-7878-4b70-9a74-56b626013989">DXVA2_SurfaceType</a> enumeration that specifies the surface type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The index was out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cc2a6180-9698-460a-9a0d-1ee9e15f197f">IDirectXVideoMemoryConfiguration</a>



<a href="https://msdn.microsoft.com/40deaddb-bb17-4a34-8294-5c7dc8a8a457">Supporting DXVA 2.0 in DirectShow</a>
 

 

