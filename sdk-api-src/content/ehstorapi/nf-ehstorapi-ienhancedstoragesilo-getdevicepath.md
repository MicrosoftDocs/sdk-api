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

# IEnhancedStorageSilo::GetDevicePath


## -description


Retrieves the path to the silo device node. The returned string is suitable for passing to <b>Windows System</b> APIs such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff552074">SetupDiOpenDeviceInterface</a>.


## -parameters




### -param ppwszSiloDevicePath [out]

A pointer to a string that represents the path to the Silo device node.


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
Device path string was retrieved successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppwszSiloDevicePath</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The memory to contain the device path string is allocated by the Enhanced Storage API and must be freed  by passing the  returned pointer to <a href="http://go.microsoft.com/fwlink/p/?linkid=134839">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a>
 

 

