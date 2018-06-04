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

# EngCreateDriverObj function


## -description


The <b>EngCreateDriverObj</b> function creates a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a> structure. 


## -parameters




### -param pvObj

Pointer to the driver resource that will be tracked by the DRIVEROBJ structure. The resource is associated with the current client process.


### -param pFreeObjProc

Pointer to a driver-supplied callback function that frees the resource pointed to by <i>pvObj</i>. The callback function should be defined as follows, where <i>pDriverObj</i> points to the DRIVEROBJ structure:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BOOL CALLBACK DrvobjFreeObjProc(DRIVEROBJ *pDriverObj);</pre>
</td>
</tr>
</table></span></div>

### -param hdev

Handle to the physical device associated with the object. This parameter is the GDI handle received by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a> function.


## -returns



The return value is a handle that identifies the newly-created DRIVEROBJ structure if the function is successful. Otherwise, it is zero.




## -remarks



This structure is used to track a device-managed resource that must be released if the resource-allocating process terminates without first cleaning it up.

The driver can explicitly delete the DRIVEROBJ structure by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564792">EngDeleteDriverObj</a>. Otherwise, the engine frees the resource by calling the function pointed to by <i>pFreeObjProc</i> when the process that created the DRIVEROBJ terminates.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564792">EngDeleteDriverObj</a>
 

 

