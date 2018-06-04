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

# PGET_SERVICE_COUNT callback function


## -description


The 
<b>GetServiceCount</b> function returns the number of services in the table.


## -parameters




### -param Arg1








## -returns



If the function succeeds, the return value is the number of services in the table.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Operation succeeded but no services are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0 (Zero)</b></dt>
</dl>
</td>
<td width="60%">
No services are available in the table or the operation failed. Call 
<a href="_win32_getlasterror">GetLastError</a> to obtain more information.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="_win32_getlasterror">GetLastError</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

