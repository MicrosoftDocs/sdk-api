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

# _DRIVEROBJ structure


## -description


The DRIVEROBJ structure is used to track a resource, allocated by a driver, that requires use GDI services. A DRIVEROBJ structure allows a display driver to request the GDI service in managing per-process resources. By creating a DRIVEROBJ structure, a display driver can ensure that resources will be released when an application terminates.


## -struct-fields




### -field pvObj

Pointer to the driver resource that will be tracked by the DRIVEROBJ structure. The resource is associated with the current client process.


### -field pFreeProc

Pointer to a driver-supplied callback function that frees the resource pointed to by <b>pvObj</b>. This callback function has the following prototype:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BOOL (CALLBACK * FREEOBJPROC) (DRIVEROBJ * pDriverObj);</pre>
</td>
</tr>
</table></span></div>
The callback function returns <b>TRUE</b> if it is able to free the resource, and <b>FALSE</b> otherwise.


### -field hdev

GDI handle to the physical device associated with the object.


### -field dhpdev

Pointer to the driver's private instance data; that is, this member identifies the driver's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


## -remarks



A DRIVEROBJ structure allows a display driver to request the GDI service in managing per-process resources. By creating a DRIVEROBJ structure, a display driver can ensure that resources will be released when an application terminates.

Some drivers, in their Escape support, allocate resources on behalf of applications. In such cases, the DRIVEROBJ structure provides a means for the application to notify the driver when it terminates. GDI will call the driver's cleanup function for each DRIVEROBJ structure allocated in an application's context that is not deleted before the application terminates.

This structure provides a locking mechanism for exclusive access to the associated resource.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564207">EngCreateDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564792">EngDeleteDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565044">EngUnlockDriverObj</a>
 

 

