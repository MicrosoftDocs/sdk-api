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

# IEnhancedStorageACT2::GetDeviceName


## -description


The <b>IEnhancedStorageACT2::GetDeviceName</b> method returns the device name associated with the Addressable Command Target (ACT).


## -parameters




### -param ppwszDeviceName [out]

Pointer to a string that represents the device name associated with the ACT.


## -returns



This method can return one of the following values:

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
The associated volume was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppwszDeviceName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operation failed due to insufficient memory allocation.

</td>
</tr>
</table>
 




## -remarks



The memory containing the device name string is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/23f47a1a-c2d1-43ed-871a-ca80aab2eed6">IEnhancedStorageACT2</a>
 

 

